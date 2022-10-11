# session-fixation-ss
Projeto de teste para verificar assertividade do plugin spring security em tratar Session Fixation. 

Utilizado Grails 2.5.6

Spring Security Core 2.0

### Configuração do teste

- O projeto conta com 3 entidades. User, Role e UserRole.

- Na inicialização, crio um User com as seguintes credenciais: `username: "samuel.silva@asaas.com" passoword: "senha"`
- Seto sua role para `ROLE_ADMIN`

- Crio então um template auth/login.gsp e um endpoint para ele e seto a permissão desse entpoint apenas para `ROLE_ADMIN`

- Para verificação no H2 da persistencia, libero acesso total para `/dbconsole/**`

- Com isso, ao acessar `/login/auth`, é possível fazer login com as credenciais acima e verificar a renovação do cookie da sessão.
