# Nagios Core
## O que é?
Nagios é um sistema **opensource** (*Nagios Core*) de monitoração de infraestrutura de redes e serviços que permite indentificar problemas antes que possam afetar e comprometer processos de negócio críticos.

## Quando usar?
- **Servidores e dispositivos de rede**: É o cenário mais ideal para uso do Nagios, monitora com excelencia redes linux e windows com suporte a firewall, switches e roteadores, impressoras e discos de rede.
- **Aplicações Críticas**: Processos de negócio crítico não podem falhar pois momentos de indisponíbilidade acarretam em prejuízos expressivos e o Nagios oferece suporte de monitoramento para identificar problemas na infraestrutura com agilidade permitindo ações antes que afetem processos críticos.
- **|Infraestrutura complexa**: suporta ambientes heterogeneos com uma gama ampla de dispositivos e inclusivo em grandes quantidades.
- **Flexibilidade necessária**: Nagios é extensivel via plugins e addons. Quando um hardware não possui suporte nativo é possível desenvolver um [[#Plugins|plugin]] para embarcar o monitoramento do hardware com o Nagios. 

## Quando não usar?
- **Redes domésticas de baixa complexidade**: O Nagios suporta tranquilamente esse cenário, porém oferece um grau de complexidade para o acompanhamento que não é bem vindo nessas topologias. ==**Alternativas para essa situação**== *MRTG, Cacti, LibreNMS.*
- **Tempo Real**: embora consiga detectar problemas em dispositivos com certa agilidade o Nagios apresenta uma latencia alta devido ao seu processo de [[coleta de dados]] via [[Agentes]] ou [[SNMP]]. ==**Alternativas para essa situação**== *[[Prometheus]], [[Grafana]], InfluxDB.*
- **Empresas com baixo orçamento**: Mesmo sendo um software opensource, normalmente sua implantação requer um profissional especializado e a aquisição de um suporte mais amplos da versão comercial Nagios XI. ==**Alternativas para essa situação**== *PRTG, Zabbix, SolarWinds*.

## Componentes
### Core
- Componente principal do Nagios, é responsável pela execução da lógica de monitoramento e gerencia todos os demais componentes e [[#Plugins|plugins]].
### Plugins
- Sistema que torna o Nagios flexivel e com excelente longevidade 
- Linguagens suportadas: C, Shell, Perl
- A saúde dos plugins é monitorada pelo Core o qual aciona um hook em métodos dos plugins e obtem como resposta **OK, WARNING, CRITICAL, UNKNOWN.**
- O Core monitora os plugins com a mesma relevância que monitora a rede, enviando também alertas e notificações em casos de falhas.
- Os plugins podem ser obtidos por terceiros ou pelo repositório oficial de plugins do Nagios [https://exchange.nagios.org/](https://exchange.nagios.org/)
- Podem ser gratuitos ou pagos
- **Plugins mais utilizados**:
	- **NDOUtils**
		- Nagios Data Output Utilizados 
		- Oferece a funcionalidade de armazenamento de status de eventos em bancos de dados **MySQL (==APENAS MYSQL!!!==)**
	- **NagiosQL**
		- **Interface Web** para gerenciar o Nagios e visualizar dados. Suporta **MySQL** e **PostgreSQL**
	- **NagVis**
		-  Visualização da topologia da rede e status de serviço em forma de mapa
	- **Check_mk**
		- Plugin vital para monitoramento de sistemas e dispositivos, incluindo windows e linux.
### NRPE
- **Nagios Remote Plugin Executor**
- Através do plugin executor é possível executar plugins em hosts remotos via ssh, telnet ou rpc.
### NSCA
- **Nagios Service Check Acceptor**
- Componente que permite que hosts remotos enviem seus status para o Nagios Core, reduzindo a necessidade do core requisicionar esses dados assim aumentando a confiabilidade do monitoramento.
## Processo de coleta de dados
- **Passo a passo**:
	1. O Nagios verifica de tempo em tempo os status da rede e serviços
	2. Dispositivos e Serviços que estejam alcançaveis vão ter seus dados coletados
	3. Após a coleta, plugins com ação em host remotos serão executados pelo [[#NRPE]] 
	4. Os dados serão armazenados no servidor
	5. O Core irá executar as regras de notificação e alertas e dispará-los caso seja necessário.
- **Comunicação na coleta**:
	- **Protocolos**:
		- **SSH:** Para executar plugins em hosts remotos de forma segura.
		- **SNMP:** Para monitorar dispositivos de rede.
		- **NRPE:** Para executar plugins em hosts remotos através do SSH.
		- **PING:** Para verificar a conectividade com hosts.
		- **[[HTTP]]:** Para monitorar websites e serviços web.
		- **TCP:** Para verificar se portas específicas estão abertas.
- **Tipos de dados**:
	- **Texto simples:** Formato mais comum, geralmente usado para status e eventos.
	- **Binário:** Formato mais eficiente para dados de performance.
	- **JSON:** Formato estruturado e fácil de analisar por ferramentas externas.
	- **XML:** Formato estruturado e legível por humanos.
## Detecção de Falhas
- A detecção de falhas do Nagios ocorre por meio da analise singular ou combinadas dos seguintes fatores:
	- **Tráfego de Dados**: volume elevado ou nulo
	- **Latência**: normalmente analizada em percentil 50 ou 90, p50/p90
	- **Packet Loss**: Interferencia no barramento na topologia, hardware comprometido, ou fator desconhecido em comunicação externa com componentes distribuidos geograficamente.
	- **Erros de CRC (redundancia)**: geralmente indentificado junto ao packet loss, são falhas coexistentes.
## Alertas e Notificação
- O Nagios pode enviar notificações na forma de:
	- Email 
	- Telefone
	- SMS
	- Webhooks: torna extremamente versátil o sistema de notificação.
- O Alertas do Nagios são divididos em 4 tipos:
	- **Alerta**: emitido quando um problema é notificado
	- **Recuperação**: emitido quando um problema é solucionado
	- **Flap**: emitido quando um problema é detectado e solucionado repetidas vezes em um intervalo curto de tempo. *(ex: congestionamento de rede, mal contato em cabos de rede, etc..)*
	- **Manutenção**: emitido quando uma interrupção é programada
## Protocolos Monitorados
- **ICMP (PING):** Verifica a conectividade com hosts e dispositivos.
- **TCP:** Verifica se portas específicas estão abertas.
- **UDP:** Verifica se portas UDP específicas estão abertas.
- **SNMP:** Monitora dispositivos de rede que suportam SNMP.
- **[[HTTP]]:** Monitora websites e serviços web.
- **[[HTTPS]]:** Monitora websites e serviços web seguros.
- **FTP:** Monitora servidores FTP.
- **SSH:** Monitora servidores SSH.
- **[[SMTP]]:** Monitora servidores de email.
- **POP3:** Monitora servidores de email POP3.
- **IMAP:** Monitora servidores de email IMAP.
## Visualização
- É possível visualizar os dados de toda a topologia da rede e de serviços por meio do widgets configurados contendo gráficos, tabelas e mapas.
- Principais paineis:
	- Painéis de Status
	- Painéis de Gráficos
	- Painéis de Histórico
	- Painéis de Mapa
- Por meio desses paineis é possível gerar relatórios flexíveis sobre dipositivos e serviços em intervalos customizados e com parametros customizados.
- Por meio de painéis de configuração também é possível realizar algums configurações e gerenciamento do Nagios
## Métricas
- **Métricas de Saúde**:
	- **Status**: OK, WARNING, CRITICAL, UNKNOWN
	- **Latência**
	- **Inatividade**
	- **Última verificação**
- **Métricas de Desempenho:**
	- **CPU**
	- **Memória**
	- **Disco**
	- **Network** 
## Integrações 
- Nagios Core permite integração com outros serviços de monitoramento como Zabbix, [[Prometheus]], Icinga e com serviços de visualização e exploração de dados como [[Grafana]], [[Kibana]], e Thruk. Pode se integrar também com sistemas de logging como [[Logstash]].
- Nessas integrações o Nagios Core **opera como cliente** primariamente, pois possui uma api limitada e mais voltada ao seu próprio gerenciamente e suporte aos seus plugins.

## Configuração
- O Nagios Core possui uma setup de configuração bastante complexo de ser implantado em toda a infraestrutura e serviços. Não é uma tarefa fácil trazer o Nagios Core pra dentro da sua infra.
- A configuração do Nagios Core é feita através do **nagios.cfg**, mas também pode ser dividida em arquivos contextuais:
	- **Notificação**: notifications.cfg
	- **Escalation**: escalation.cfg
	- **Permissão**: nagios.cfg
	- **Integração**: hosts.cfg (ou cada ferramenta.cfg)
	- **Personalização**: nagios.cfg
	- **Logging**: nagios.cfg
	- **Manutenção**: nagios.cfg
	- **Monitoramento Específico**: arquivo .cfg específico
- O Core também oferece agentes para serem instalados em ambientes windows e linux que irão enviar dados por meio so [[#NSCA]]
- 
## Informações Técnicas do Sistema:
- Linguagem em que foi desenvolvido
	- Principalmente em **C**, com algumas funcionalidades em **C++**
	- **Perl** nas tarefas de automação
- **Plataforma Opensource**: **Nagios Core** apenas
- **Qual o contexto de criação?**
	- Ethan Galstad criou como projeto pessoal para monitorar a disponibilidade de seus servidores
- **Quando**: 1996 por Ethan Galstad
- **Multiplataforma**: Windows, Unix, Outros kernels via plugins.

## Família Nagios
- **Nagios Core **(**Opensource**)
- **Nagios XI:** Monitoramento completo, interface web amigável.
- **Nagios Log Server:** Centralização e análise de logs em tempo real.
- **Nagios Fusion:** Visão unificada de TI em painéis personalizáveis.
- **Nagios Network Analyzer:** Mapeamento e análise avançada de redes.
- **Nagios Library:** Biblioteca de plugins para diversos cenários de monitoramento.
