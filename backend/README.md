# 🧩 Backend - Projeto Fullstack UNIFACEF - Mateus dos Santos Moreira Código 24882

## 📘 Descrição do Projeto

Este repositório contém o **módulo Backend** do projeto desenvolvido para um trabalho em grupo da disciplina de Desenvolvimento Web na UNIFACEF.  
Ele é responsável por fornecer toda a **camada de lógica de negócio e persistência de dados** da aplicação, disponibilizando uma **API RESTful** que será consumida pelo módulo **Frontend**.

O backend foi desenvolvido utilizando **Node.js com TypeScript** e **Prisma ORM**, garantindo escalabilidade, segurança e facilidade de manutenção.  
O sistema realiza operações de **CRUD (Create, Read, Update, Delete)** sobre os dados armazenados no banco de dados SQLite, centralizando as regras de negócio da aplicação.

---

## 🎯 Objetivo do Código-Fonte

O código-fonte deste módulo tem como objetivo:
- Gerenciar a **camada de dados** da aplicação, utilizando o Prisma ORM para comunicação com o banco de dados.
- Implementar as **rotas de API** que permitem a integração entre o Frontend e o banco de dados.
- Centralizar toda a **lógica de controle e manipulação de entidades** (ex: cadastro, listagem e atualização de dados).
- Fornecer respostas padronizadas em formato **JSON** para o consumo via requisições HTTP.

Em resumo, o Backend é o **núcleo lógico** do sistema: ele processa as requisições enviadas pela interface Frontend, interage com o banco de dados e retorna os resultados de forma estruturada.

---

## 🧠 Integração com o Projeto Final em Grupo

No projeto final em grupo, o Backend será responsável por:
- Disponibilizar **rotas de API** (endpoints) que o Frontend irá consumir via HTTP (utilizando `fetch` ou `axios`).
- Gerenciar as **entidades do sistema** definidas no banco de dados Prisma (por exemplo: `Food`).
- Servir como **ponte entre o banco de dados e a interface do usuário**, garantindo que os dados exibidos no Frontend estejam sempre atualizados e consistentes.
- Possibilitar o **armazenamento e consulta de informações** através de operações RESTful.

Exemplo de integração:
1. O usuário interage com o Frontend (ex: envia um formulário).
2. O Frontend faz uma requisição HTTP (`POST`, `GET`, `PUT` ou `DELETE`) para uma rota do Backend.
3. O Backend processa a requisição, acessa o banco via Prisma e retorna uma resposta JSON com os dados solicitados.

---

## ⚙️ Tecnologias Utilizadas

- **Node.js** – Ambiente de execução do JavaScript no servidor  
- **TypeScript** – Superset do JavaScript que adiciona tipagem estática  
- **Express.js** – Framework para criação de rotas e APIs RESTful  
- **Prisma ORM** – Mapeamento objeto-relacional para interação com o banco de dados  
- **SQLite** – Banco de dados leve e local utilizado durante o desenvolvimento  
- **Docker** – (opcional) Containerização do ambiente de execução  

---

## 📁 Estrutura de Pastas

```

backend/
├── prisma/
│   ├── schema.prisma        # Definição do modelo de banco de dados
│   └── migrations/          # Histórico de migrações do Prisma
├── src/
│   ├── controllers/         # Controladores que contêm a lógica das rotas
│   │   └── foodController.ts
│   ├── models/              # Definição de modelos e tipos
│   │   └── food.ts
│   ├── routes/              # Definição das rotas da API
│   │   └── foodRoutes.ts
│   ├── prismaClient.ts      # Instância do Prisma para acesso ao banco
│   └── index.ts             # Ponto de entrada principal do servidor
├── package.json             # Dependências e scripts do projeto
├── tsconfig.json            # Configurações do TypeScript
└── Dockerfile               # Configuração de containerização

````

---

## 🚀 Como Executar o Projeto

### 🔧 Pré-requisitos
Certifique-se de ter instalado em sua máquina:
- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)
- (Opcional) [Docker](https://www.docker.com/)

### 📦 Instalação
1. Acesse a pasta do projeto:
   ```bash
   cd backend

2. Instale as dependências:

   ```bash
   npm install
   ```
3. Configure o banco de dados com Prisma:

   ```bash
   npx prisma migrate dev
   ```
4. Execute o servidor:

   ```bash
   npm run dev
   ```
5. A API estará disponível em:

   ```
   http://localhost:3000
   ```

---

## 🔗 Endpoints Principais

| Método | Rota        | Descrição                      |
| ------ | ----------- | ------------------------------ |
| GET    | `/food`     | Retorna todos os alimentos     |
| GET    | `/food/:id` | Retorna um alimento específico |
| POST   | `/food`     | Cria um novo alimento          |
| PUT    | `/food/:id` | Atualiza um alimento existente |
| DELETE | `/food/:id` | Remove um alimento do sistema  |

---

## 🧩 Futuras Integrações

No projeto final fullstack, este backend poderá ser expandido para incluir:

* Autenticação de usuários (JWT ou OAuth)
* Controle de permissões e papéis
* Upload de imagens
* Novas entidades (usuários, pedidos, categorias, etc.)
* Deploy em nuvem (Render, Railway, ou AWS)

---

## 📄 Licença

Este projeto é de uso acadêmico.
Todos os direitos reservados aos autores do grupo
