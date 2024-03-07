
## Principais Conceitos
### Inventário
O Ansible gerencia hosts através de um arquivo de inventário, que lista os servidores que serão alvo das operações de automação. Esse inventário pode ser estático ou dinâmico, permitindo a inclusão de hosts de forma flexível.
### Playbooks
Os Playbooks são o coração do Ansible. Eles são escritos em YAML e descrevem uma série de tarefas a serem executadas em hosts específicos. Os Playbooks são altamente legíveis e permitem a automação de processos complexos de forma intuitiva.
### Módulos
O Ansible possui uma vasta biblioteca de módulos que fornecem funcionalidades para interagir com sistemas, serviços e aplicativos. Esses módulos abrangem desde a execução de comandos simples até a configuração avançada de recursos.
### Roles
As Roles permitem organizar e reutilizar Playbooks de forma modular. Elas encapsulam funcionalidades específicas e promovem a reutilização de código, facilitando a manutenção e o compartilhamento de automações.

## Vantagens do Ansible
### Simplicidade
O Ansible adota uma abordagem "apenas YAML", eliminando a necessidade de linguagens de programação complexas. Isso torna a criação e manutenção de automações acessíveis mesmo para iniciantes.
### Agentless
Ao contrário de algumas ferramentas de automação, o Ansible é agentless, o que significa que não requer a instalação de software adicional nos hosts alvo. Isso simplifica o processo de gerenciamento e reduz o impacto no desempenho dos sistemas.
### Escalabilidade
Com sua arquitetura modular e flexível, o Ansible é altamente escalável, permitindo automatizar desde pequenos ambientes locais até infraestruturas complexas distribuídas em nuvem.