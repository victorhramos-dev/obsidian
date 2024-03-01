# OWASP
- Open Web Appliction Security Project
- Lista as 10 principais ameaças de segurança. Essa lista é atualizada a cada 4 anos.
- 10 ameaças de segurança mais populares em 2024 (lista de 2021)
	1. **[[#Controle de Acesso Quebrado]]**
	2. **Falhas Criptograficas**
	3. **Injeção**
	4. **Design Inseguro**
	5. **Má Configuração de Segurança** 
	6. **Componentes vulneráveis e desatualizados**
	7. **Falha de identificação e autenticação**
	8. **Falha na integridade de software e dados**
	9. **Falha na Segurança em Logging e Monitoramento**
	10. **Falsificação de Request no lado do Servidor** 

## Controle de Acesso Quebrado
- **Ocorre quando o usuário (atacante) pode interagir com o sistema além de suas permissões mínimas. Exemplos comuns:**
	- *Recurso da organização deveria estar disponível apenas para um grupo específico de usuários mas até aberto a qualquer um (violação do princípio do acesso mínimo)*
	- *Navegação forçada alterando parametros da URL, estado interno do APP, cookies, etc...*
	- *Visualização/Edição de conta de outro usuário por fornecimento equívoco de identificador único.*
	- *Elevação de previlégio: conseguir atuar como administrador sem ser um ou conseguir atuar como um usuário sem estar cadastrado no sistema.*
	- *Adulteração de metadados ou tokens de autenticação.*
	- *Falha em configuração de CORS, permitindo requisições externas quando não permitidas.*
- **Prevenção**:
	- Implementação de políticas de controle de acesso adequadas
	- Revisão periódica das permissões de acesso a recursos protegidos
## Falhas Criptográficas
- São falhas relacionadas ao uso inadequado de algoritimos de criptografia ou implementação incorreta dos protocolos de criptografia.
- 