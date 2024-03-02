- O termo caixa-preta é dado porque ao realizar os testes não devemos nos influenciar ou considerar o que tem dentro, ou seja não devemos considerar o código do software. Devemos considerar apenas as entradas e saídas do sistema.
- **Objetivo**:
	- Verificar o funcionamento do software conforme especificações
	- Encontrar erros de funcionalidade que independem de como o software foi construído.
- **Técnicas de testes caixa-preta**:
	- **Equivalência de Classes**: divide os dados em classes de equivalência e escolhe um caso de teste de cada classe. [[#Exemplo de Equivalência de Classes]]
	- **Partição de valor limite**: testa os valores limites, incluindo valores próximos aos limites das entradas. [[#Exemplo de Partição de Valor Limite]]
	- **Análise de Estado**: avalia o comportamento do sistema em diferentes estados. [[#Exemplo de Análise de Estado]]
	- **Tabela de Decisão**: testa diferentes combinações de entradas baseadas em uma tabela de decisão.
### Exemplo de Equivalência de Classes:
- Regra de restrição de cadastro para usuários com idade entre 18 e 65 anos:
	- Dividimos em classes de equivalência:
		- Classe Válida: 18 a 65
		- Classe Inválida: < 18
		- Classe Inválida: > 65
	- Criamos exemplo de testes:
		- Idade 25 (válida)
		- Idade 15 (inválida)
		- Idade 70 (inválida)
### Exemplo de Partição de Valor Limite
- Regra de restrição de cadastro para usuários com idade entre 18 e 65 anos:
	- Definimos nossos limites:
		- Limite inferior: 18 anos
		- Limite superior: 65 anos
	- Criamos exemplos de testes:
		- 18 anos (limite inferior)
		- 65 anos (limite superior)
		- 15 anos (abaixo do limite inferior)
		- 70 anos (acima do limite superior)
### Exemplo de Análise de Estado
- Vamos considerar um ecommerce e a entidade Pedido, vamos supor que essa entidade tenha 3 estados: carrinho vazio, carrinho com itens, pedido finalizado. Com os estados definidos conseguimos criar subrotinas de testes pra validar cada estado:
	- Adicionar um item ao carrinho  
	- Remover um item ao carrinho
	- Finalizar um pedido com diferentes condições de pagamento, etc...
### Tabela de Decisão
- Sistema de login com usuario e senha, podemos criar mensagens de erro com base em combinações de entrada.
```markdown
| Usuário Incorreto | Senha Incorreta | Mensagem de Erro         |
|-------------------|-----------------|--------------------------|
| Sim               | Não             | "Usuário não encontrado" |
| Não               | Sim             | "Senha Incorreta"        |
| Não               | Não             | "Logado com sucesso"     |
```
