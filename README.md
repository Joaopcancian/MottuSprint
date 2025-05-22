# 🚀 MottuPatio

API RESTful desenvolvida com ASP.NET Core para o gerenciamento dos pátios de motos da Mottu, incluindo controle de entrada, triagem, monitoramento e gestão de colaboradores.

---

## 🧾 Descrição do Projeto

A Mottu enfrenta desafios na gestão de suas motos dentro do pátio, como imprecisões na localização, atrasos e ineficiência operacional. Este sistema propõe uma solução baseada em:

- **Classificação por cores**
- **Visão computacional**
- **Monitoramento em tempo real**

O objetivo é otimizar a organização e o controle das motos.

---

## 🎯 Objetivos

- Organizar as motos por categorias de prioridade
- Reduzir atrasos no atendimento e manutenção
- Aumentar a eficiência na gestão de localização
- Disponibilizar dados em tempo real sobre status e tempo de permanência

---

## 🧩 Solução

### Classificação por Cores

Cada moto recebe um adesivo com uma cor após triagem:

| Cor     | Classificação             | Descrição                             | Tempo Limite        |
|---------|---------------------------|----------------------------------------|---------------------|
| Verde   | Pronta para uso           | Moto liberada para entrega             | Sem limite          |
| Amarelo | Reparos rápidos           | Troca de pneus, óleo, ajustes leves    | 15 minutos          |
| Vermelho| Reparos graves            | Problemas críticos (motor, elétrica)   | Variável            |
| Roxo    | Administrativos           | Pendências legais, sem placa, Detran   | Até resolução       |

### Organização do Pátio

- Dividido por áreas conforme a cor de classificação
- Motos devem ser posicionadas na área correta

### Visão Computacional & Monitoramento

- Câmeras analisam adesivos e placas
- O sistema gera alertas se:
  - Moto estiver fora da área correta
  - Permanência exceder o limite
- Leitura de placa retorna:
  - Problema reportado
  - Data de entrada
  - Status
  - Dados do veículo

---

## 🔁 Fluxo de Funcionamento

1. **Triagem**: Classificação por cor
2. **Alocação**: Moto posicionada na área correspondente
3. **Monitoramento**:
   - Validação de posição via câmera
   - Geração de alerta se necessário
4. **Consulta**:
   - Leitura de placa exibe dados completos da moto

---

## 🧪 Tecnologias Utilizadas

- ASP.NET Core 7.0
- Entity Framework Core
- Oracle Database
- Oracle.ManagedDataAccess
- Oracle.EntityFrameworkCore
- Swagger (OpenAPI)

---

## ⚙️ Funcionalidades

A API oferece CRUD completo para:

- **Motos**
- **Triagens**
- **Monitoramentos**
- **Áreas do Pátio**
- **Colaboradores**

Outras funcionalidades:
- Relacionamentos entre entidades
- Validações automáticas
- Integração com Oracle
- Interface de testes via Swagger

---

## 🔗 Endpoints

Cada entidade possui os seguintes endpoints:

- `GET /[entidade]` – Lista todos os registros
- `GET /[entidade]/{id}` – Retorna um registro específico
- `POST /[entidade]` – Cria um novo registro
- `PUT /[entidade]/{id}` – Atualiza um registro
- `DELETE /[entidade]/{id}` – Remove um registro

---

## ▶️ Como Executar o Projeto

### Pré-requisitos

- [.NET 7.0 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)
- Oracle Database (FIAP ou local)
- Oracle SQL Developer
- Visual Studio ou VS Code

### Passos

1. Clone o repositório:

```bash
git clone https://github.com/Joaopcancian/MottuSprint.git
cd MottuPatio

Autores
João Pedro Cancian Corrêa – RM: 555341
Giulia Camillo - RM: 554473
Caroline de Oliveira - RM: 559123
Desenvolvido como parte da Sprint 1 - 3º Semestre
