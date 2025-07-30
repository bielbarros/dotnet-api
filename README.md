#  RESTful API para Gerenciamento de Pizzas

Uma API RESTful desenvolvida em ASP.NET Core 8.0 para gerenciamento de pizzas, demonstrando boas práticas de desenvolvimento web com C#.

## 📋 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Pré-requisitos](#pré-requisitos)
- [Instalação e Execução](#instalação-e-execução)
- [Endpoints da API](#endpoints-da-api)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Sobre o Projeto

Este projeto é uma API RESTful desenvolvida como exercício prático para demonstrar o uso do ASP.NET Core 8.0 na criação de APIs web. A aplicação implementa operações CRUD (Create, Read, Update, Delete) para gerenciamento de pizzas, incluindo informações sobre ingredientes e opções sem glúten.

## Funcionalidades

- **CRUD Completo**: Criar, ler, atualizar e deletar pizzas
- **Validação de Dados**: Verificação de integridade dos dados
- **Documentação Automática**: Swagger/OpenAPI integrado
- **Respostas HTTP Padrão**: Códigos de status apropriados
- **Estrutura Modular**: Separação clara entre Controllers, Models e Services

## Tecnologias Utilizadas

- **.NET 8.0** - Framework de desenvolvimento
- **ASP.NET Core** - Framework web
- **C#** - Linguagem de programação
- **Swagger/OpenAPI** - Documentação da API
- **Visual Studio 2022** - IDE de desenvolvimento

## Pré-requisitos

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) ou [Visual Studio Code](https://code.visualstudio.com/)
- [Git](https://git-scm.com/)

## Instalação e Execução

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/pizza-api.git
cd pizza-api
```

### 2. Restaure as dependências
```bash
dotnet restore
```

### 3. Execute o projeto
```bash
dotnet run
```

### 4. Acesse a API
- **API**: https://localhost:7001
- **Swagger UI**: https://localhost:7001/swagger

## Endpoints da API

### Pizzas

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/pizza` | Lista todas as pizzas |
| `GET` | `/pizza/{id}` | Obtém uma pizza específica |
| `POST` | `/pizza` | Cria uma nova pizza |
| `PUT` | `/pizza/{id}` | Atualiza uma pizza existente |
| `DELETE` | `/pizza/{id}` | Remove uma pizza |

### Exemplo de Uso

#### Criar uma nova pizza
```bash
curl -X POST "https://localhost:7001/pizza" \
     -H "Content-Type: application/json" \
     -d '{
       "name": "Margherita",
       "isGlutenFree": false
     }'
```

#### Obter todas as pizzas
```bash
curl -X GET "https://localhost:7001/pizza"
```

## Estrutura do Projeto

```
PizzaAPI/
├── Controllers/
│   └── PizzaController.cs      # Controlador da API
├── Models/
│   └── Pizza.cs               # Modelo de dados
├── Services/
│   └── PizzaServices.cs       # Lógica de negócio
├── Program.cs                  # Configuração da aplicação
├── appsettings.json           # Configurações
└── README.md                  # Este arquivo
```

## Arquitetura

O projeto segue uma arquitetura em camadas:

- **Controllers**: Responsáveis por receber requisições HTTP e retornar respostas
- **Models**: Definem a estrutura dos dados
- **Services**: Contêm a lógica de negócio e operações de dados

## Modelo de Dados

```csharp
public class Pizza
{
    public int Id { get; set; }
    public string? Name { get; set; }
    public bool IsGlutenFree { get; set; }
}
```

## Contribuição

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Autor

**Seu Nome**
- GitHub: [@bielbarros](https://github.com/bielbarros)
- LinkedIn: [Seu LinkedIn](https://linkedin.com/in/gabriel-sbarros)

## Agradecimentos

- Microsoft pela documentação do ASP.NET Core
- Comunidade .NET por compartilhar conhecimento
- Swagger pela ferramenta de documentação

---

Se este projeto foi útil para você, considere dar uma estrela no repositório! 