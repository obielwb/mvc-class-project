# Boilerplate MVC em Node.js com PostgreSQL

## Resposta as perguntas propostas em aula

```
Perguntas
1. Explique com suas palavras o funcionamento do models, controller e fale sobre endpoints no projeto
Os models definem o que cada entidade do projeto pode fazer. Nos models de aluno, professor e curso por exemplo, é definido as funções de CRUD para cada um, com os métodos de create, update, read e delete.
Os controllers expões as operações definidas nos models junto com a lógica de negócios necessária, tais funções são utilizadas no arquivo de routes e expostas em certo endpoint específico.
Cada endpoint é acompanhado com seu respectivo método HTTP, e a definição de qual url estará disponível cada função do controller.

2. Como ocorre o envio e o recebimento de dados no formato JSON neste projeto? Cite uma rota que responde em JSON e explique seu funcionamento.
O envio e o recebimento de dados no formato JSON ocorrem por meio de requisições HTTP entre o cliente e o servidor. No projeto, o backend  utiliza res.json() para enviar respostas em JSON ao cliente, o que permite a troca de dados estruturados de forma padronizada e fácil de interpretar tanto por humanos quanto por sistemas.

Um exemplo disso é a rota GET "/alunos/curso/:curso_id". Essa rota recebe o curso_id como parâmetro na URL, realiza uma consulta no banco de dados para obter os alunos de certo curso e então retorna esses dados no formato JSON. Esse retorno pode ser consumido pelo frontend facilitando a renderização dinâmica das informações na interface do usuário.


3. Qual a importância de usar HTML básico com formulários e tabelas para organizar e manipular dados no navegador? Por que esse tipo de estrutura ainda é útil em projetos back-end com Node.js?
O uso de HTML básico com formulários e tabelas continua sendo extremamente relevante, mesmo em projetos modernos com backend em Node.js. Formulários permitem a coleta de dados do usuário de forma simples e direta — como cadastros, pesquisas e atualizações de registros — e são enviados ao backend via requisições HTTP (geralmente POST). Já as tabelas são ideais para exibir informações estruturadas, como listas de usuários, cursos ou relatórios.

Além disso, em aplicações back-end com Node.js, é comum o uso de templates (como EJS) para renderizar HTML dinâmico com dados vindos do servidor — e tabelas e formulários são parte essencial dessas views.
```

Este projeto é um boilerplate básico para uma aplicação Node.js seguindo o padrão MVC (Model-View-Controller), utilizando PostgreSQL como banco de dados.

## Requisitos

- Node.js (versão X.X.X)
- PostgreSQL (versão X.X.X)

## Instalação

1. **Clonar o repositório:**

```bash
   git clone https://github.com/seu-usuario/seu-projeto.git
   cd seu-projeto
```

2. **Instalar as dependências:**

```bash
npm install
```

3. **Configurar o arquivo `.env`:**

Renomeie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente necessárias, como as configurações do banco de dados PostgreSQL.

## Configuração do Banco de Dados

1. **Criar banco de dados:**

   Crie um banco de dados PostgreSQL com o nome especificado no seu arquivo `.env`.

2. **Executar o script SQL de inicialização:**

```bash
npm run init-db
```

Isso criará a tabela `users` no seu banco de dados PostgreSQL com UUID como chave primária e inserirá alguns registros de exemplo.

## Funcionalidades

- **Padrão MVC:** Estrutura organizada em Model, View e Controller.
- **PostgreSQL:** Banco de dados relacional utilizado para persistência dos dados.
- **UUID:** Utilização de UUID como chave primária na tabela `users`.
- **Scripts com `nodemon`:** Utilização do `nodemon` para reiniciar automaticamente o servidor após alterações no código.
- **Testes:** Inclui estrutura básica para testes automatizados.

## Scripts Disponíveis

- `npm start`: Inicia o servidor Node.js.
- `npm run dev`: Inicia o servidor com `nodemon`, reiniciando automaticamente após alterações no código.
- `npm run test`: Executa os testes automatizados.
- `npm run test:coverage`: Executa os testes e gera um relatório de cobertura de código.

## Estrutura de Diretórios

- **`config/`**: Configurações do banco de dados e outras configurações do projeto.
- **`controllers/`**: Controladores da aplicação (lógica de negócio).
- **`models/`**: Modelos da aplicação (definições de dados e interações com o banco de dados).
- **`routes/`**: Rotas da aplicação.
- **`tests/`**: Testes automatizados.
- **`views/`**: Views da aplicação (se aplicável).

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir um issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a Licença MIT.

Este README.md fornece uma visão geral clara do boilerplate, incluindo instruções de instalação, configuração do banco de dados, funcionalidades principais, scripts disponíveis, estrutura de diretórios, como contribuir e informações de licença. Certifique-se de personalizar as seções com detalhes específicos do seu projeto conforme necessário.
