- Ferramenta de monitoração e alertas
- Desenvolvido no ==**SoundCloud**==
- ==**Não confundir: NÃO MONITORA INFRAESTRUTURA! MONITORA APENAS SISTEMAS E SERVIÇOS.**==
- Monitora em Tempo Real
- Prometheus trabalha com banco de dados [[Modelagem de Dados Multidimensional|multidimensional]] com série de dados temporal
- É um sistema distribuído em que cada servidor é independente, ou sejá não depende do armazenamento de rede ou de outros serviços
- Utiliza a linguagem PromQL para consultas (Prometheys Query Language)
- **NÃO TEM SUPORTE A SQL!**
- Trabalha coletando métricas em intervalos programados avaliando expressões de regras
- Pode disparar alertas baseado em regras definidas
- Os componentes do Prometheus são escritos em **Go** e distribuidos como binarios estáticos.
- Componentes do [[Prometheus]] :
	- **Servidor principal ** Prometheus Server
	- **Bibliotecas Cliente**: bibliotecas para softwares interagirem com o [[Prometheus]] 
	- **PushGateway**: permite que aplicativos enviem métricas para o Prometheus 
	- **Exportadores**: coletam métricas de diferentes fontes, como servidores, bancos de dados e outros sistemas.
	- [[#Gerenciador de Alertas]]

## Funcionalidades
- modelo **multidimensional** de dados identificado por **chave-valor**
- PromQL, linguagem de consulta flexível, para suportar a dimensionalidade dos dados.
- Não depende do armazenamento distribuído, cada nó é **independente**.
- A **coleta de dados** temporais é realizado por meio de **pulls HTTP**
- O envio de séries temporais é realizado por um gateway intermediário
- Possui um sistema de descoberta de serviços mas também poder ser configurados estáticamente.

## Quando usar o Prometheus?
- Funciona bem pra guardar qualquer série temporal que seja puramente numérica.
- Pode ser usado quando monitoramento for centrado na maquina e também quando for em sistemas orientados a serviço.
- Quando usado em sistemas orientados a serviço seu ponto forte é sua consulta de dados multidimensional.

## Quando não usar o Prometheus
- Ele é um sistema de monitoração focado em alta confiabilidade mesmo em condições extremas de falha. Seus dados são númericos e não provem dados dealhados como os dados de clientes ou de pagamentos, etc... Nesses casos é melhor utilizar outro sistema para esses dados e o Prometheus para monitorar seus serviços.
- Monitoramento de Logs
- Monitoramento de Rede
- Monitoramento de UX

## Fluxo da operação
1. **Coleta**: Prometheus coleta métricas temporais ou recebe de intermediários por gateway.
2. **Armazenamento**: Armazena os dados localmente
3. **Agregação**: Aplica regras sobre os dados pra realizar a agregação
4. **Alertas**: Gera alertas sobre esses dados caso se aplique à determinadas condições.
5. **Visualização**: Os dados ficam disponíveis para exibição via Prometheus WebUI, [[Grafana]] ou outros dashboards que se integrem via API.

## Linha de Comando
- prometheus: prometheus server
- promtool: ferramentas adicionais
	- [`promtool help`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-help): mostra a ajuda
	- [`promtool check`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-check): verifica a integridade dos recursos
	- [`promtool query`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-query): executa uma consulta no prometheus server
	- [`promtool debug`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-debug): coleta informações de depuração (debug)
	- [`promtool push`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-push): faz um push ao prom server
	- [`promtool test`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-test): teste unitário
	- [`promtool tsdb`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-tsdb): executa comandos tsdb (time series database)
	- [`promtool promql`](https://prometheus.io/docs/prometheus/latest/command-line/promtool/#promtool-promql): formatação e edição de comandos promql, é necessário habilitar a flag --experimental

## Visualização
- Expression Browser:
	- acessível pelo /graph no prometheus server
	- permite receber expressões e entrega o resultado via tabela ou gráficos temporais
- [[Grafana]]
	- ferramenta popular de visualização de dados que pode ser usada com o Prometheus.
- Console Templates:
	- Permite criar consoles utilizando a linguagem Go
	- Possui uma curva de aprendizado acentuada.
	- Os gráficos são renderizados com a javascript library RickShaw
	- faz uso de operadores de templating como {{ }}

## Métricas
- **Counter** 
	- métrica cumulativa ideal para situações em que há uma contagem crescente, medir quantidade de ocorrencia em um intervalor de tempo
	- não deve ser usado quando há possíbilidade do valor diminuir
	- as operações deve ser apenas: incremento, zero ou reinicio.
- **Gauge**
	- valores instantaneos de um sistemas, como uso de cpu, memoria
	- ideal para valores que alteram frequentemente e precisam ser exibidos em tempo real. 
	- analogo ao velocimetro do carro
- **Histrogram**
	- como os dados são distribuidos em um intervalo
	- excelente pra visualizar dados que possam ser agrupados em diferentes distribuições
	- gráfico de barras
	- ex: tamanho de arquivos, tempo de reposta
- **Summary**
	- semelhante ao histrogram porém com estatisticas em percentil e quantil
	- grafico de pizza
	- ex: tempo de resposta de uma api em percentil p50, p90

## Gerenciador de Alertas
- Toma conta da deduplicação (remoção de alertas duplicados)
- Faz agrupamento de notificações
	- Realizado por meio de similaridade na natureza das notificações juntamente com um subgrupo de horário das ocorrências.
	- Esse agrupamento é feito antes de enviar os alertas, assim enviando um alerta apenas contendo uma informação resumida sobre todos os alertas agrupados.
- Gerencia o silenciamento de notificações e pausas de recebimento (inibição)
	- É feito sobre uma natureza de alerta
	- A inibição de alerta é configurada no arquivo de config do gerenciador de alertas (alertmanager.yml)
	- O silenciamento é feito na interface web do gerenciador de alertas 
- Direciona os alertas para os serviços corretos, configurados na seção de routing do alertmanager.yml 
	- E-mail
	- PagerDuty
	- OpsGenie
	- Webhooks: configurado na seção **alerting** do **prometheus.yml** ou na seção de **receivers** do **alertmanager.yml** 
- Command Line:
	- alertmanager
		- -h : mostra a ajuda
		- --config.file: especifica qual arquivo de configuração carregar.