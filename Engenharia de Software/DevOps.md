# DevOps
- Cultura e práticas que visam integrar o desenvolvimento de software (DEV) com a operação de sistemas (OPS) para melhorar a colaboração e a entrega contínua de software com alta qualidade.

# Questões
[[ lin]]
## Cultura
- **Colaboração multidiscplinar**
	- Foco na quebra de silos entre equipes de desenvolvimento, operações e outras áreas.
	- Promoção de uma mentalidade de trabalho em equipe e comunicação transparente.
	- Incentivo à colaboração para alcançar objetivos comuns e resolver problemas de forma eficiente.
- **Automação**
	- Utilização de ferramentas e práticas para automatizar processos de desenvolvimento, teste, implantação e operações. 
	- Automação de pipelines de integração contínua (CI) e entrega contínua (CD) [[CI & CD]].
	- Automação de provisionamento de infraestrutura e configuração de ambientes. [[Ansible]] [[Kubernetes]] [[Puppet]] [[Docker]] 
- **Entrega Contínua**
	- Abordagem para entregar incrementalmente novas funcionalidades aos usuários de forma rápida e confiável.
	- Integração contínua: Automatização de compilação, teste e análise de código.
	- Implantação contínua: Automação do processo de implantação em ambientes de teste, homologação e produção.
- **Monitoramento e Feedback**
	- Monitoramento contínuo do desempenho do sistema em produção.
	- Coleta de métricas e logs para identificar problemas rapidamente e tomar ações proativas.
	- Feedback rápido dos usuários e stakeholders para orientar melhorias e ajustes no processo de desenvolvimento e operações.
	- [[Elasticsearch]] [[Logstash]] [[Grafana]] [[Kibana]] [[Prometheus]] [[Nagios]] 
- **Melhora Contínua**
	- Encorajamento à experimentação e aprendizado contínuo.
	- Adoção de práticas como retrospectivas, revisões pós-implantação e análise de incidentes para identificar oportunidades de melhoria.
	- Foco na adaptação às mudanças e na busca constante pela excelência operacional.
- **Responsabilidade Compartilhada**
	- Todos os membros da equipe são responsáveis pela qualidade, segurança e desempenho do software em produção.
	- Quebra de silos, Transparência, Feedback contínuo entre membros da equipe.
## Vantagens do DevOps
- Maior velocidade de entrega
- Melhoria na qualidade do software
- Redução de falhas e tempo de inatividade
- Maior satisfação do cliente
- Ambiente de trabalho mais colaborativo
- Redução de Riscos
- Feedback Rápido

## Responsabilidade Compartilhada 
- Todos os profissionais são responsáveis pelo produto pois podem contribuir de forma ativa em qualquer fase do processo de desenvolvimento independente de sua especialidade profissional.
	- **Qualidade**: assegura a qualidade, automação de testes, definição de métricas
	- **Segurança**: [[DevSecOps]] [[Privacidade e Segurança por padrão]]
	- **Infraestrutura**: automação de operações e implementação de práticas de segurança
	- **Software**: código de alta qualidade, facilidade de implantação e monitoramento e escalabilidade.
## Quando não utilizar
- Projetos pequenos ou Isolados: não há necessidade de uma entrega contínua ou de uma infraestrutura complexa pra ser automatizada.
## Atenção
- ==**DevOPS não é pra automatizar! A automação é importante nas práticas porém não é obrigatória em algumas situações, como por exemplo deploy. Na maioria das grandes organizações o deploy e release são humanamente ativados.**==