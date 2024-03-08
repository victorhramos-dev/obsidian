# SOA
## SOAP
- ==Protocolo de comunicação== baseado em documentos (envelopes) ==XML==
- Define um conjunto de regras de ==comunicação entre sistemas== distribuídos.
- Elementos do SOAP:
	- **Envelope** (obrigatorio): formatação e definição da estrutura para encapsular os dados reais. Elemento Raíz.
	- **Header**: contem informações adicionais como autenticação, transações e roteamento. Metadados.
	- **Body** (obrigatorio): contém os dados reais encapsulados conforme o envelope a serem transmitidos entre os sistemas.
	- **Fault**: se der erro, o código de erro vem no campo fault.
- O Soap utiliza primariamente o protocolo **HTTP** como protocolo primário, porém pode utilizar também os protocolos **TCP** e **SMTP** dependendo das condições de implementação.
- O SOAP é stateless por padrão, as mensagem não se correlacionam e nem são coordenadas.
- O SOAP baseia-se no estilo de RPC (_remote procedure call_), determinando a necessidade de atender a outros protocolos para realizar a chamada a um serviço.
> ==- **Estrutura da Mensagem:**==
> 	==1. **Envelope (Root)**==
> 		==1. **Header**==
> 		==2. **Body**==
> 			==1. **Fault**==
<!--SR:!2000-01-01,1,250!2000-01-01,1,250!2000-01-01,1,250!2000-01-01,1,250!2000-01-01,1,250!2000-01-01,1,250!2000-01-01,1,250!2024-03-09,1,230-->


## WSDL
- Web Service Descripton Language
- O WSDL (Web Service Description Language) descreve um serviço da web que especifica e localiza um serviço e os métodos a serem utilizados.
- O WSDL não se preocupa em descrever o método de comunicação e muito menos a troca de dados, mas apenas especificar e localizar um serviço web.
- **WSDL 1.1**
	- ==Abstract Description==:
		- **types**: tipos de dados
		- **message**: informações necessárias para executar operação
		- **portTypes**: operações / msg trocada
	- ==Concrete Description==:
		- **binding**: protocolo de comunicação
		- **service**: endpoints
			- **port**: portas do endereço
- **WSDL 2.0**
	- ==Abstract Description==:
		- **types**
		- **interface**
	- ==Concrete Description==:
		- **binding**
		- **service**
			- **endpoint**
<!--SR:!2000-01-01,1,250!2024-03-12,4,270!2000-01-01,1,250!2000-01-01,1,250-->


## UDDI
- Universal Description Discovery and Integration
- **==Catalogo de metadados dos serviços==**
- Se comunica utilizando SOAP portanto utiliza um arquivo XML
- Não é um diretório global, pode haver inúmeros diretórios públicos mantidos por provedores
- <span style="background:rgba(0, 0, 0, 1)"><font color="#fff">Páginas Brancas</font></span>: descrevem a companhia: nome, endereço, contatos, etc.
- <span style="background:#fff88f">Páginas Amarelas</span>: incluem as categorias, baseada em taxonomias padrões.
- <span style="background:#d3f8b6">Páginas Verdes</span>: descrevem a interface para o serviço, em nível de detalhe suficiente para se escrever uma aplicação que use o Web service.


## REST
- Define regras pra criar webservices.
- Estimula o baixo acoplamento -> stateless -> por causa do http
- **Não é:**
	- Implementação de SOAP / WSDL
	- Biblioteca
	- Tecnologia
	- Não é Evolução do SOAP
- **REST é:**
	- ==Padrão arquitetural de integração de serviços distribuídos usando HTTP.==
	- Conjunto de princípios:
		- Recurso com Interface Uniforme (URI)
- **URI/URL**
	- Não deve ter verbos!
- **RESTful**
	- ==Se você está usando RESTful é porque está sendo **100% **STATELESS**!==
	- Pra atender ao RESTful é preciso seguir as 6 contraints (restrições):
		- Client-Server
		- Separada por Camadas
		- Dados Cacheados
		- HATEOAS: resposta contendo o recurso + links de ações sobre o recurso (navegação, etc...)
		- Versionamento (v1/v2/.../vn) -> via url ou headers
		- Content Negotiation (format=xml, json) -> via url ou header
	- Não escala bem pois é necessário reserver memória no servidor pra cada requisitante.
- Documentação:
	- Swagger