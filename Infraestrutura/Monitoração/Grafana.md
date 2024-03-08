> *O Grafana é uma ferramenta poderosa e flexível para visualizar e analisar dados. Ele pode ser usado para monitorar o desempenho de seus sistemas e aplicações, identificar problemas e tomar decisões informadas.*
## **Introdução**
O Grafana é uma **plataforma de código aberto** para **visualização e análise de dados**. Ele permite que você crie **dashboards personalizados** para monitorar o desempenho de seus **sistemas e aplicações**. O Grafana é **altamente escalável e flexível**, e pode ser usado para monitorar **qualquer tipo de dado**, desde **métricas de infraestrutura** até **logs e traces**.

## **História**
* **Criado em 2014** por **Torkel Ödegaard**, um desenvolvedor sueco.
* Motivado pela necessidade de uma ferramenta de visualização de dados **poderosa e flexível** para monitorar sistemas em escala.
* **Desenvolvido e aprimorado** por uma **comunidade ativa** de desenvolvedores e usuários.

## Software Tech Info
- **Desenvolvido** em **Go**
- **Frontend**: Typescript
- **Gráficos**: libraries javascript
- **Plugins**: [[Python]], Go, Javascript, Ruby e C#
- **Banco de Dados**: PostgreSQL (Default), mas permite MySQL, InfluxDB, [[Elasticsearch]]
## **Principais Features:**
- **Consulta de Dados:**
	- Via **PromQL**..
	- Podem ser utilizados **plugins** para consultas **SQL** em bancos de dados.
* **Visualização de dados:**
    * **Diversos tipos de painéis e gráficos** para visualizar suas métricas.
    * **Exemplos:** gráficos de linhas, gráficos de área, histogramas, mapas de calor.
* **Correlação de dados:**
    * Permite **identificar problemas** em seus sistemas.
    * **Exemplos:** correlacionar métricas de CPU com métricas de memória para identificar gargalos.
* **Alertas:**
    * **Notifica você** quando seus sistemas apresentarem problemas.
    * **Exemplos:** configurar alertas para serem enviados por email ou por chat.
* **Análise de dados:**
    * Ferramentas para **analisar seus dados e identificar tendências**.
    * **Exemplos:** calcular médias, medianas, desvios padrão e percentis.
* **Dashboards customizados:**
    * Permite criar dashboards **personalizados** para atender às suas necessidades específicas.
    * **Exemplos:** dashboards para diferentes equipes, diferentes tipos de dados, diferentes ambientes.

## **Principais integrações:**
* **[[Prometheus]]:**
    * O Grafana se integra **facilmente** com o [[Prometheus]].
    * Permite visualizar as métricas coletadas pelo [[Prometheus]] em dashboards personalizados.
* **InfluxDB:**
    * O Grafana também se integra com o InfluxDB, outro sistema de coleta e armazenamento de métricas.
* **[[Elasticsearch]]:**
    * O Grafana pode ser integrado com o [[Elasticsearch]] para visualizar logs e traces.
* **Graphite:**
    * O Grafana se integra com o Graphite, um sistema de coleta e armazenamento de métricas legado.
* **CloudWatch:**
    * O Grafana pode ser integrado com o CloudWatch, o serviço de monitoramento da AWS.
## **Exemplos de Dashboards:**
* **Dashboard de monitoramento de infraestrutura:**
    * Exibe métricas como uso de CPU, uso de memória, tráfego de rede e latência.
    * Permite identificar problemas de desempenho e gargalos.
* **Dashboard de monitoramento de aplicações:**
    * Exibe métricas como tempo de resposta, taxa de erros e solicitações por segundo.
    * Permite identificar problemas de desempenho e bugs nas aplicações.
* **Dashboard de business intelligence:**
    * Exibe métricas como vendas, clientes e leads.
    * Permite identificar tendências e oportunidades de negócios.
## Alertas
- **Características**:
	- Funcionalidade de alerta integrada ao Grafana.
	- Permite definir alertas com base em painéis e consultas do Grafana.
	- Suporta diversos canais de notificação, como email, Slack, Webhooks e Opsgenie.
	- Mais fácil de usar do que o Alert Manager do [[Prometheus]], especialmente para usuários iniciantes.
- **Recomendado para:**
    - Ambientes simples com poucos alertas.
    - Usuários que desejam uma solução fácil de usar.
    - Familiaridade com o Grafana.
## Métricas

### **Métricas de Infraestrutura:**
- **Uso da CPU:** Monitora o uso da CPU por host, processo ou container.
- **Uso da Memória:** Monitora o uso da memória por host, processo ou container.
- **Tráfego de Rede:** Monitora o tráfego de rede por interface, protocolo ou IP.
- **Latência:** Monitora a latência de rede, de aplicações ou de serviços.
- **Disco:** Monitora o uso do disco, o espaço livre e as I/Os.
- **Temperatura:** Monitora a temperatura dos componentes do sistema.
### **Métricas de Aplicações:**
- **Tempo de Resposta:** Monitora o tempo de resposta de aplicações web, APIs ou serviços.
- **Taxa de Erros:** Monitora a taxa de erros de aplicações web, APIs ou serviços.
- **Solicitações por Segundo:** Monitora o número de solicitações por segundo que uma aplicação recebe.
- **Fila de Tarefas:** Monitora o tamanho da fila de tarefas de uma aplicação.
- **[[Cache]]:** Monitora a taxa de acertos e erros do cache de uma aplicação.
### **Logs e Traces:**
- **Logs de Aplicação:** Monitora os logs de suas aplicações para identificar erros ou problemas.
- **Logs de Sistema:** Monitora os logs do sistema para identificar problemas de segurança ou desempenho.
- **Traces:** Monitora os traces de suas aplicações para identificar gargalos ou problemas de desempenho.
### **Outras Métricas:**
- **Métricas de Negócios:** Monitora métricas como vendas, clientes e leads.
- **Métricas de Segurança:** Monitora métricas como tentativas de login inválidas e ataques de segurança.
- **Métricas de Experiência do Usuário:** Monitora métricas como tempo de carregamento da página e taxa de cliques.