<p align="center">
  <a href="https://nestjs.com/" target="_blank"><img src="https://nestjs.com/img/logo-small.svg" width="100" alt="NestJS" /></a>
</p>

<h1 align="center">Projeto NestJS — Backend na Prática</h1>

<p align="center">
  Repositório-modelo das aulas de <strong>Backend com NestJS</strong> do curso de <strong>Desenvolvedor Fullstack</strong><br/>
  <strong>SENAI Digitech — Centro de Referência em TIC RJ</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white" alt="NestJS" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=swagger&logoColor=black" alt="Swagger" />
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat&logo=vitest&logoColor=white" alt="Vitest" />
</p>

---

## Sobre este repositório

Este é o projeto de referência que construo, aula a aula, junto com meus alunos na unidade curricular de Backend do curso de **Desenvolvedor Fullstack** do **SENAI Digitech — Centro de Referência em TIC RJ**.

O desenvolvimento segue a sequência das apostilas oficiais do curso. Cada conteúdo teórico vira código funcionando em sala: os alunos acompanham a implementação, reproduzem os exemplos nos próprios projetos e usam este repositório como gabarito para revisar, comparar soluções e retomar qualquer aula em que tenham faltado.

Por isso o projeto cresce de forma incremental. Ele parte da estrutura básica de uma aplicação NestJS e evolui para uma API documentada, validada, com tratamento de erros, middlewares, upload de mídia e persistência em MongoDB. O repositório acompanha a turma em tempo real e recebe novos commits a cada aula.

## Como navegar pelas aulas

Os commits são numerados de acordo com a aula correspondente. Para ver exatamente o que foi construído em uma aula, abra o [histórico de commits](../../commits/main) e consulte o commit com o número dela.

| Aula | Conteúdo |
|:---:|---|
| 07 | Estrutura e fundamentos do NestJS: módulos, controllers e providers |
| 08 | Route handlers: `GET` e `POST` |
| 09 | Route handlers: `PUT`, `PATCH` e `DELETE` |
| 10 | Rotas dinâmicas e parâmetros de rota |
| 11 | Fluxos de imagem e mídia em APIs (upload com Multer) |
| 12 | Request e Response avançados |
| 13 | Middlewares e interceptação de requisições |
| 15 | Tratamento de erros, exception filters e status codes HTTP |
| 16 | Validação de dados com schemas Zod e pipes personalizados |
| 17 | Documentação da API com Swagger (OpenAPI) |
| 18 | Integração com MongoDB (Mongoose) e segurança |

> A aula 14 foi desenvolvida em um repositório à parte, por isso não aparece nesta sequência.

> 🚧 **Curso em andamento:** novas aulas são adicionadas a este repositório, e a esta tabela, conforme o conteúdo avança.

## O que o projeto aborda

- **Arquitetura NestJS:** módulos, controllers, services, injeção de dependência e DTOs
- **API REST completa:** CRUD com os verbos HTTP e rotas dinâmicas nos recursos `livros`, `produtos`, `convidados` e `colaboradores`
- **Manipulação de mídia:** upload e entrega de arquivos com Multer
- **Middlewares:** registro de logs das requisições
- **Tratamento de erros:** filtro global de exceções HTTP com respostas padronizadas
- **Validação:** pipe personalizado com Zod para validar o corpo das requisições
- **Documentação:** Swagger/OpenAPI gerado a partir do código
- **Persistência:** MongoDB com Mongoose, local ou no Atlas
- **Configuração:** variáveis de ambiente com `@nestjs/config`
- **Qualidade:** testes automatizados com Vitest e Supertest, lint com Oxlint e formatação com Prettier

## Tecnologias

| Categoria | Ferramentas |
|---|---|
| Framework | NestJS, Express |
| Linguagem | TypeScript |
| Banco de dados | MongoDB, Mongoose |
| Validação | Zod |
| Documentação | Swagger (`@nestjs/swagger`) |
| Upload | Multer |
| Testes | Vitest, Supertest |
| Qualidade de código | Oxlint, Prettier |

## Estrutura do projeto

```
src/
├── admin/            # Rotas administrativas
├── colaboradores/    # Recurso persistido no MongoDB (schema Mongoose)
├── common/pipes/     # Pipe de validação com Zod
├── convidados/       # CRUD com DTOs, interfaces e service
├── filtros/          # Filtro global de exceções HTTP
├── livros/           # CRUD de livros
├── logger/           # Middleware de log
├── media/            # Upload e entrega de imagens/arquivos
├── produtos/         # CRUD de produtos
├── seguranca/        # Rotas de exemplo de segurança
├── app.module.ts
└── main.ts           # Bootstrap da aplicação e configuração do Swagger
```

## Como executar

**Pré-requisitos:** Node.js (LTS) e MongoDB (local ou Atlas).

```bash
# 1. Clone o repositório
git clone https://github.com/fabcurvello/projeto-nestjs.git
cd projeto-nestjs

# 2. Instale as dependências
npm install

# 3. Configure as variáveis de ambiente
cp .env.example .env
# edite o .env e informe a DATABASE_URL do seu MongoDB

# 4. Rode em modo de desenvolvimento
npm run start:dev
```

A API sobe em `http://localhost:3000` e a documentação interativa (Swagger) fica em **`http://localhost:3000/docs`**.

### Outros comandos

```bash
npm run build       # compila o projeto
npm run start:prod  # executa a versão compilada
npm run test        # executa os testes
npm run test:cov    # testes com relatório de cobertura
npm run lint        # análise estática com Oxlint
npm run format      # formata o código com Prettier
```

> **Atenção:** nunca faça commit do arquivo `.env` nem de credenciais reais do banco. Use sempre o `.env.example` como referência.

## Sobre o professor

**Fabricio Curvello** é desenvolvedor e professor de desenvolvimento de software. Leciona no SENAI-RJ desde 1997, em cursos de programação, banco de dados, web e desenvolvimento fullstack, e no Centro Universitário IBMR desde 2018, nos cursos de Análise e Desenvolvimento de Sistemas, Ciência da Computação e Gestão de TI.

No backend, trabalha com os alunos a construção de APIs profissionais com NestJS e TypeScript, sempre com foco em boas práticas de arquitetura, validação, documentação e testes, que são as competências cobradas pelo mercado.

- LinkedIn: [linkedin.com/in/fabriciocurvello](https://www.linkedin.com/in/fabriciocurvello)
- YouTube: [@fabriciocurvello](https://www.youtube.com/@fabriciocurvello)
- GitHub: [github.com/fabcurvello](https://github.com/fabcurvello)
- Currículo Lattes: [lattes.cnpq.br/2406072276749635](http://lattes.cnpq.br/2406072276749635)

---

<p align="center">
  Material de apoio às aulas do curso de Desenvolvedor Fullstack — SENAI Digitech, Centro de Referência em TIC RJ.
</p>
