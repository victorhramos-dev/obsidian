## Estrutura de Dados
### Set (conjuntos)
#### HashSet
- Armazena elementos ==sem repetição== e sem ordem específica. Utiliza uma tabela de hashes pra garantir que os dados não se repetirão.
#### TreeSet
- Armazena elementos ==sem repetição== e em ==**ordem** **crescente**==. Utiliza uma árvore binária auto-balanceada para garantir a ordenação e busca eficiente.

### Map (mapas)

#### HashMap
- Mapa hash por ==**chave-valor**== sem ordenação.
#### TreeMap
- Mapa hash por ==**chave-valor**== porém em ordem ==crescente== utilizando uma árvore vermelha preta

### List (listas)
#### ArrayList
- Armazena elementos em um array contíguo, oferecendo acesso rápido por índice, mas com inserções e remoções lentas no meio da lista.
#### LinkedList
- Implementa uma lista dinâmica com elementos encadeados, permitindo inserções e remoções eficientes em qualquer posição, mas com acesso por índice mais lento.
#### Vector
- Similar ao ArrayList, mas thread-safe, tornando-o adequado para ambientes multithread.

### Queue (filas)
#### LinkedList
- Implementa uma fila FIFO (First In First Out) utilizando uma lista ligada, permitindo enfileiramento e desenfileiramento eficientes.

### Stack (pilhas)
#### Stack
- Pilha LIFO, Last In First Out. 
- Utiliza array ou linked list
## JVM
- A saída do compilador gera um bytecode invés de executável.
- Um programa Java é executado apelas pela JVM
## Applet
- Tipo de programa Java para web, é executado por navegador compatíveis com java
- A partir de 2017 os principais browser deixaram de suportar applets Java
- A evolução das tecnologias web deixaram o uso de applets menos atrativo.

## Fachada
- Na arquitetura de três camadas em Java EE, a classe Fachada é utilizada para proporcionar um fluxo único para acesso aos serviços da camada de regras de negócio;
- Deve conter, de forma obrigatória, pelo menos um Controlador e delegar a invocação dos métodos para os repositórios.

## Stream API
- Novidade no Java 8
### Métodos
- **filter**: tem a missão de filtrar os elementos de um fluxo de acordo com alguma condição fornecida, ao final ele nos retorna um fluxo apenas com os elementos que se enquadaram na condição.
- **distinct**: tem a missão de retornar um fluxo contendo apenas elementos únicos, sem dados duplicados.
- **limit**: vamos utilizar esse método quando a intenção for limitar a quantidade de elementos em um fluxo.
- **skip**: ignora os elementos que foram passados como argumento. Por exemplo, suponha que você tenha uma lista com 20 elementos e queira ignorar os cinco primeiros, o método skip é quem irá auxiliar nesse processo.
- **sorted**: é utilizado quando a intenção é ordenar um fluxo.

## Exceptions
### java.lang.NoClassDefFoundError
- É uma exceção lançada pela Java Virtual Machine (JVM) quando ela não consegue encontrar uma classe necessária para executar o código.

## MultiThreading
- Java provê de forma nativa
- As prioridades dos processos podem ser diferentes

## Herança
### Sobreposição
- Possibilidade de **a classe filha implementar o método da classe pai**, passando a "valer" o método chamado de acordo com o tipo de objeto.
- ![[Pasted image 20240213225802.png]]
### Sobrecarga
- Ocorre quando há vários métodos **na mesma classe** que possuem o mesmo nome porém **argumentos diferentes**.