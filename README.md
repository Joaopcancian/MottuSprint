# MottuPatio

API RESTful desenvolvida com ASP.NET Core para gerenciamento de pátios de motos da Mottu, incluindo controle de entrada, triagem, monitoramento e gestão de colaboradores.

## Tecnologias Utilizadas

- ASP.NET Core 7.0
- Entity Framework Core
- Oracle Database
- Swagger
- Oracle.ManagedDataAccess
- Oracle.EntityFrameworkCore

---

## Funcionalidades

A API oferece um CRUD completo para as seguintes entidades:

- Cadastro, listagem, atualização e remoção de:
  - Motos
  - Triagens
  - Monitoramentos
  - Áreas do Pátio
  - Colaboradores
- Relacionamento entre motos e suas áreas, status e histórico de triagens
- Documentação da API com Swagger (OpenAPI)

---

## Estrutura de Endpoints

Cada entidade possui rotas para:

- `GET /[entidade]` – Listar todos os registros
- `GET /[entidade]/{id}` – Obter registro por ID
- `POST /[entidade]` – Criar novo registro
- `PUT /[entidade]/{id}` – Atualizar registro existente
- `DELETE /[entidade]/{id}` – Remover registro

---

## Como Executar o Projeto

### Requisitos

- [.NET 7.0 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)
- Oracle Database
- Oracle SQL Developer
- VS Code ou Visual Studio

### Passos

1. Clone o repositório:

git clone https://github.com/Joaopcancian/MottuSprint.git
cd MottuPatio

2. Configure a connection string Oracle no appsettings.json:

"ConnectionStrings": {
  "OracleConnection": "User Id=SEU_USUARIO;Password=SUA_SENHA;Data Source=oracle.fiap.com.br:1521/orcl"
}
--- Substituições do código
SEU_USUARIO = rm555341
SUA_SENHA = 070705

3. Execute a aplicação no seu VS Code ou Visual Studio
4. Acesse a documentação Swagger:
Copie e cole o link no seu navegador: http://localhost:5178/swagger/index.html

Autores
João Pedro Cancian Corrêa – RM: 555341
Giulia Camillo - RM: 554473
Caroline de Oliveira - RM: 559123
Desenvolvido como parte da Sprint 1 - 3º Semestre
