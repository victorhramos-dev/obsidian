---
cards-deck: Infraestrutura
---


## Afirmações
- Kubernetes é uma plataforma de orquestração de contêineres que automatiza o provisionamento, escalonamento e gerenciamento de aplicativos em contêineres.
- Pods são a menor unidade em Kubernetes, consistindo em um ou mais contêineres que compartilham armazenamento, rede e especificações de ciclo de vida.
- Um nó (node) em Kubernetes é uma máquina física ou virtual que faz parte do cluster e pode executar pods.
- Services em Kubernetes são usados para expor aplicativos implantados dentro do cluster para outros aplicativos ou usuários.
- Deployment é um recurso em Kubernetes usado para garantir que um conjunto especificado de pods esteja sempre em execução e atualizado para a versão mais recente do aplicativo.
- O Kubectl é a principal ferramenta de linha de comando para interagir com clusters Kubernetes, permitindo o gerenciamento de recursos e a execução de comandos em pods.
- O YAML é uma linguagem usada para escrever manifestos que descrevem os recursos do Kubernetes, como pods, serviços e deployments.
- Um namespace Kubernetes é uma maneira de organizar e isolar recursos dentro de um cluster, permitindo a divisão lógica de recursos.
- Helm é um gerenciador de pacotes para Kubernetes que simplifica o processo de implantação e gerenciamento de aplicativos usando modelos pré-configurados.
- Ingress é um recurso em Kubernetes usado para controlar o acesso externo aos serviços dentro do cluster, permitindo o roteamento de solicitações HTTP e HTTPS.
- StatefulSets são usados para aplicativos que exigem identidades persistentes e únicas, como bancos de dados, garantindo a ordem e a persistência dos pods.
- Um DaemonSet em Kubernetes garante que todos (ou alguns) nós em um cluster executem uma cópia específica de um pod, como um agente de monitoramento.
- O Horizontal Pod Autoscaler (HPA) ajusta automaticamente o número de réplicas de um aplicativo com base na utilização da CPU ou outras métricas definidas pelo usuário.
- Um Secret em Kubernetes é um objeto usado para armazenar informações sensíveis, como senhas, chaves SSH ou tokens de API, de forma segura.
- O NetworkPolicy é um recurso em Kubernetes usado para especificar como os pods podem se comunicar entre si e com outros recursos de rede dentro do cluster.
- O Container Runtime Interface (CRI) é uma interface que permite a integração de runtimes de contêineres diferentes com Kubernetes, como Docker, containerd e CRI-O.
- O Job Kubernetes cria uma ou mais tarefas independentes que executam até a conclusão com sucesso, como processamento em lote ou operações de backup.
- Um Operator em Kubernetes é um método de empacotar, implantar e gerenciar um aplicativo Kubernetes, permitindo a automação de tarefas operacionais.
- O Custom Resource Definition (CRD) é uma extensão do Kubernetes que permite aos usuários definir e usar recursos personalizados além dos tipos de recursos padrão.
- Um cluster Kubernetes pode ser implantado em nuvens públicas, privadas ou híbridas, proporcionando flexibilidade de implantação.
- O Taint é uma marcação aplicada a um nó Kubernetes para repelir pods, a menos que eles tenham uma tolerância correspondente, garantindo a segregação de carga de trabalho.
- Um Label é uma chave/valor associada a recursos Kubernetes para identificação, organização e seleção de recursos.
- Um ServiceAccount em Kubernetes é uma entidade que fornece uma identidade para os processos em execução em um pod, permitindo a autenticação e a autorização.
- O Volume em Kubernetes é um mecanismo usado para fornecer armazenamento persistente para contêineres em um pod, como armazenamento em disco ou em nuvem.
- O Role-Based Access Control (RBAC) é um recurso em Kubernetes usado para definir e gerenciar políticas de acesso baseadas em funções, limitando as ações que os usuários podem realizar.
- O PersistentVolume é um recurso em Kubernetes que representa um volume de armazenamento persistente provisionado pelo administrador do cluster e disponível para os pods.
- O Admission Controller em Kubernetes é um componente que intercepta solicitações de criação ou modificação de recursos e aplica regras de validação ou mutação antes de permitir que eles sejam admitidos no cluster.
- O Service Mesh é uma abordagem em Kubernetes para gerenciar a comunicação entre serviços, oferecendo recursos como roteamento, descoberta de serviços, monitoramento e segurança.
- O ConfigMap em Kubernetes é um recurso usado para armazenar configurações de aplicativos em um formato de chave/valor, permitindo a separação de configurações do código.
- O Affinity e o anti-affinity são mecanismos em Kubernetes para influenciar o agendamento de pods em nós com base em afinidades ou aversões, permitindo controle sobre onde os pods são executados.
- O PodSecurityPolicy é um recurso em Kubernetes usado para definir políticas de segurança para pods, restringindo as ações que eles podem realizar.
- O CNI (Container Networking Interface) é uma especificação que define como contêineres se comunicam uns com os outros na mesma rede em Kubernetes, oferecendo flexibilidade na configuração da rede.
- O Descheduler é uma ferramenta em Kubernetes que ajuda a balancear a carga entre os nós no cluster, evitando a sobrecarga de alguns nós enquanto outros estão subutilizados.
- Um Static Pod em Kubernetes é um pod cuja configuração é gerenciada diretamente pelo kubelet, em vez de pelo API Server, útil para executar serviços essenciais no nó.
- O Kubelet é um agente que roda em cada nó no cluster Kubernetes e garante que os containers estejam sendo executados em pods, além de relatar o status do nó para o restante do cluster.
- O Heketi é uma interface de gerenciamento de volumes para o GlusterFS que pode ser integrado com Kubernetes para fornecer armazenamento persistente para aplicativos.
- O Kata Containers é uma tecnologia que combina as vantagens de VMs e contêineres, oferecendo isolamento de segurança semelhante ao de VMs com a eficiência dos contêineres, suportado pelo Kubernetes.
- O Multus é um plugin CNI em Kubernetes que permite que um pod tenha várias interfaces de rede, oferecendo flexibilidade na configuração da rede para aplicativos complexos.
- O PodDisruptionBudget é um recurso em Kubernetes que permite limitar o número de pods que podem ser desligados simultaneamente para garantir a alta disponibilidade de aplicativos.
- O Prometheus é uma ferramenta de monitoramento amplamente usada com Kubernetes, oferecendo métricas detalhadas sobre o desempenho e a saúde do cluster e dos aplicativos.
- O Istio é uma plataforma de serviço de malha que pode ser integrada com Kubernetes para controle de tráfego e segurança, oferecendo recursos avançados de gerenciamento de tráfego e políticas de segurança.
- O Contour é um controlador Ingress para Kubernetes projetado para desempenho e escalabilidade, oferecendo recursos avançados de roteamento de tráfego HTTP e HTTPS.
- O MetalLB é um controlador de balanceador de carga para Kubernetes que permite a atribuição de endereços IP a serviços, facilitando a exposição de serviços externamente.
- O Kube-proxy é um componente em Kubernetes que gerencia o tráfego de rede para serviços, oferecendo balanceamento de carga e encaminhamento de pacotes para os pods corretos.
- O Fluentd é uma ferramenta de coleta e encaminhamento de logs que pode ser integrada com Kubernetes para centralizar logs, oferecendo insights sobre o comportamento e o desempenho dos aplicativos.


## Overview
O Kubernetes é uma plataforma de orquestração de contêineres que automatiza o provisionamento, escalonamento e gerenciamento de aplicativos em contêineres. A menor unidade em Kubernetes são os Pods, que consistem em um ou mais contêineres que compartilham armazenamento, rede e especificações de ciclo de vida. Cada máquina física ou virtual que faz parte do cluster e pode executar pods é chamada de nó.

Os Services em Kubernetes são usados para expor aplicativos implantados dentro do cluster para outros aplicativos ou usuários. O recurso Deployment é usado para garantir que um conjunto especificado de pods esteja sempre em execução e atualizado para a versão mais recente do aplicativo. Para interagir com clusters Kubernetes, a principal ferramenta de linha de comando é o Kubectl, que permite o gerenciamento de recursos e a execução de comandos em pods.

Os manifestos que descrevem os recursos do Kubernetes, como pods, serviços e deployments, são escritos em YAML. Dentro de um cluster, um namespace Kubernetes é uma maneira de organizar e isolar recursos, permitindo a divisão lógica de recursos. O Helm é um gerenciador de pacotes para Kubernetes que simplifica o processo de implantação e gerenciamento de aplicativos usando modelos pré-configurados.

O Ingress é um recurso em Kubernetes usado para controlar o acesso externo aos serviços dentro do cluster, permitindo o roteamento de solicitações HTTP e HTTPS. Os StatefulSets são usados para aplicativos que exigem identidades persistentes e únicas, como bancos de dados, garantindo a ordem e a persistência dos pods. Um DaemonSet em Kubernetes garante que todos (ou alguns) nós em um cluster executem uma cópia específica de um pod, como um agente de monitoramento.

O Horizontal Pod Autoscaler (HPA) ajusta automaticamente o número de réplicas de um aplicativo com base na utilização da CPU ou outras métricas definidas pelo usuário. Um Secret em Kubernetes é um objeto usado para armazenar informações sensíveis, como senhas, chaves SSH ou tokens de API, de forma segura. O NetworkPolicy é um recurso em Kubernetes usado para especificar como os pods podem se comunicar entre si e com outros recursos de rede dentro do cluster.

O Container Runtime Interface (CRI) é uma interface que permite a integração de runtimes de contêineres diferentes com Kubernetes, como Docker, containerd e CRI-O. O Job Kubernetes cria uma ou mais tarefas independentes que executam até a conclusão com sucesso, como processamento em lote ou operações de backup. Um Operator em Kubernetes é um método de empacotar, implantar e gerenciar um aplicativo Kubernetes, permitindo a automação de tarefas operacionais.

O Custom Resource Definition (CRD) é uma extensão do Kubernetes que permite aos usuários definir e usar recursos personalizados além dos tipos de recursos padrão. Um cluster Kubernetes pode ser implantado em nuvens públicas, privadas ou híbridas, proporcionando flexibilidade de implantação. O Taint é uma marcação aplicada a um nó Kubernetes para repelir pods, a menos que eles tenham uma tolerância correspondente, garantindo a segregação de carga de trabalho.

Um Label é uma chave/valor associada a recursos Kubernetes para identificação, organização e seleção de recursos. Um ServiceAccount em Kubernetes é uma entidade que fornece uma identidade para os processos em execução em um pod, permitindo a autenticação e a autorização. O Volume em Kubernetes é um mecanismo usado para fornecer armazenamento persistente para contêineres em um pod, como armazenamento em disco ou em nuvem.

O Role-Based Access Control (RBAC) é um recurso em Kubernetes usado para definir e gerenciar políticas de acesso baseadas em funções, limitando as ações que os usuários podem realizar. O PersistentVolume é um recurso em Kubernetes que representa um volume de armazenamento persistente provisionado pelo administrador do cluster e disponível para os pods. O Admission Controller em Kubernetes é um componente que intercepta solicitações de criação ou modificação de recursos e aplica regras de validação ou mutação antes de permitir que eles sejam admitidos no cluster.

O Service Mesh é uma abordagem em Kubernetes para gerenciar a comunicação entre serviços, oferecendo recursos como roteamento, descoberta de serviços, monitoramento e segurança. O ConfigMap em Kubernetes é um recurso usado para armazenar configurações de aplicativos em um formato de chave/valor, permitindo a separação de configurações do código. O Affinity e o anti-affinity são mecanismos em Kubernetes para influenciar o agendamento de pods em nós com base em afinidades ou aversões, permitindo controle sobre onde os pods são executados.

O PodSecurityPolicy é um recurso em Kubernetes usado para definir políticas de segurança para pods, restringindo as ações que eles podem realizar. O CNI (Container Networking Interface) é uma especificação que define como contêineres se comunicam uns com os outros na mesma rede em Kubernetes, oferecendo flexibilidade na configuração da rede. O Descheduler é uma ferramenta em Kubernetes que ajuda a balancear a carga entre os nós no cluster, evitando a sobrecarga de alguns nós enquanto outros estão subutilizados.

Um Static Pod em Kubernetes é um pod cuja configuração é gerenciada diretamente pelo kubelet, em vez de pelo API Server, útil para executar serviços essenciais no nó. O Kubelet é um agente que roda em cada nó no cluster Kubernetes e garante que os containers estejam sendo executados em pods, além de relatar o status do nó para o restante do cluster. O Heketi é uma interface de gerenciamento de volumes para o GlusterFS que pode ser integrado com Kubernetes para fornecer armazenamento persistente para aplicativos.

O Kata Containers é uma tecnologia que combina as vantagens de VMs e contêineres, oferecendo isolamento de segurança semelhante ao de VMs com a eficiência dos contêineres, suportado pelo Kubernetes. O Multus é um plugin CNI em Kubernetes que permite que um pod tenha várias interfaces de rede, oferecendo flexibilidade na configuração da rede para aplicativos complexos. O PodDisruptionBudget é um recurso em Kubernetes que permite limitar o número de pods que podem ser desligados simultaneamente para garantir a alta disponibilidade de aplicativos.

O Prometheus é uma ferramenta de monitoramento amplamente usada com Kubernetes, oferecendo métricas detalhadas sobre o desempenho e a saúde do cluster e dos aplicativos. O Istio é uma plataforma de serviço de malha que pode ser integrada com Kubernetes para controle de tráfego e segurança, oferecendo recursos avançados de gerenciamento de tráfego e políticas de segurança. O Contour é um controlador Ingress para Kubernetes projetado para desempenho e escalabilidade, oferecendo recursos avançados de roteamento de tráfego HTTP e HTTPS.

O MetalLB é um controlador de balanceador de carga para Kubernetes que permite a atribuição de endereços IP a serviços, facilitando a exposição de serviços externamente. O Kube-proxy é um componente em Kubernetes que gerencia o tráfego de rede para serviços, oferecendo balanceamento de carga e encaminhamento de pacotes para os pods corretos. O Fluentd é uma ferramenta de coleta e encaminhamento de logs que pode ser integrada com Kubernetes para centralizar logs, oferecendo insights sobre o comportamento e o desempenho dos aplicativos.

# Visão CEBRASPE
- Um aplicativo _conteinerizado_ pode ser testado como uma unidade e implantado como instância de uma imagem de contêiner no sistema operacional hospedeiro.
- **Kubernetes** é uma plataforma utilizada para manter e implantar um grupo de contêineres em tempo de execução, além de ser comumente utilizada junto com a ferramenta **Docker**, para melhor controle e implementação de aplicativos em contêineres.
- Um **contêiner** é um conjunto de processos organizados isoladamente do sistema; todos os arquivos necessários para executá-los são disponibilizados por uma imagem distinta.
- **Contêineres Docker** encapsulam em um mesmo objeto a aplicação e o seu ambiente de execução (sistema operacional e demais dependências), aproximando os times de desenvolvimento e de operação.
- Um contêiner deve fornecer um ambiente de hospedagem do lado do servidor gerenciado e um _middleware_ que intercepte as chamadas recebidas e, em seguida, execute as ações apropriadas para garantir que as propriedades desejadas do aplicativo distribuído sejam mantidas.
- 😱 O **Kubernetes** faz o escalonamento e a recuperação no caso de falha de uma aplicação.
- Ao conteinerizar uma aplicação, ela passa a ser executada de forma independente do sistema operacional e isolada de outras aplicações, o que aumenta a sua eficiência.
- Os _containers_ oferecem um mecanismo de empacotamento lógico em que os aplicativos podem ser abstraídos pelo ambiente em que são efetivamente executados, mesmo se esse ambiente for uma nuvem pública.
- Caso seja necessário informar ao **Docker** que um container deve escutar na porta de rede 80 do TCP, o comando correto no _DockerFile_ é o seguinte: `EXPOSE 80/tcp`
- Em _containers_, a decomposição de funções de uma aplicação resulta em microsserviços, independentes entre si e com fraco acoplamento.
- 😱 Com a implantação do **Kubernetes**, é obtido um cluster com pelo menos um nó de trabalho (_worker node_); os nós de trabalho, por sua vez, hospedam vários componentes da carga de trabalho do aplicativo.
- No **Kubernetes**, _kubelet_ é uma pequena aplicação localizada em um nó que se comunica com o plano de controle, assegurando que os _containers_ estejam em execução em um _pod_, que consiste no menor e mais simples objeto do **Kubernetes**.

#cards 
1. O que é um aplicativo conteinerizado?::Um aplicativo que pode ser testado como uma unidade e implantado como instância de uma imagem de contêiner no sistema operacional hospedeiro.
^1709919743727
2. O que é Kubernetes?::Uma plataforma para manter e implantar um grupo de contêineres em tempo de execução.
^1709919743736
3. Kubernetes é comumente usado com qual ferramenta?::Docker.
^1709919743749
4. O que é um contêiner?::Um conjunto de processos organizados isoladamente do sistema, com todos os arquivos necessários fornecidos por uma imagem distinta.
^1709919743755
5. O que os contêineres Docker encapsulam?::A aplicação e o seu ambiente de execução.
^1709919743763
6. O que um contêiner deve fornecer?::Um ambiente de hospedagem do lado do servidor gerenciado e um middleware que intercepte as chamadas recebidas.
^1709919743770
7. O que o Kubernetes faz no caso de falha de uma aplicação?::Faz o escalonamento e a recuperação.
^1709919743778
8. O que acontece ao conteinerizar uma aplicação?::Ela passa a ser executada de forma independente do sistema operacional e isolada de outras aplicações.
^1709919743784
9. O que os containers oferecem?::Um mecanismo de empacotamento lógico onde os aplicativos podem ser abstraídos pelo ambiente em que são executados.
^1709919743789
10. Como informar ao Docker que um contêiner deve escutar na porta de rede 80 do TCP?::Usando o comando "EXPOSE 80/tcp" no DockerFile.
11. O que resulta da decomposição de funções de uma aplicação em containers?::Microsserviços, independentes entre si e com fraco acoplamento.
^1709919743795
12. O que se obtém com a implantação do Kubernetes?::Um cluster com pelo menos um nó de trabalho (worker node).
^1709919743799
13. O que os nós de trabalho hospedam no Kubernetes?::Vários componentes da carga de trabalho do aplicativo.
^1709919743805
14. O que é kubelet no Kubernetes?::Uma pequena aplicação em um nó que se comunica com o plano de controle.
^1709919743809
15. O que o kubelet assegura no Kubernetes?::Que os containers estejam em execução em um pod.
^1709919743814
16. O que é um pod no Kubernetes?::O menor e mais simples objeto do Kubernetes.
^1709919743819
