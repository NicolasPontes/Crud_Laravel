# CRUD Laravel — Gerenciamento de Clientes/Usuários

Aplicação web desenvolvida com o **Laravel Framework** para gerenciamento de clientes/usuários, implementando as quatro operações fundamentais: **Create, Read, Update e Delete (CRUD)**.

Projeto criado com fins de estudo e portfólio, aplicando os conceitos de arquitetura MVC, Eloquent ORM e boas práticas de desenvolvimento com Laravel.

## 📋 Funcionalidades

- ✅ Cadastrar novos clientes/usuários
- ✅ Listar todos os clientes/usuários cadastrados
- ✅ Visualizar detalhes de um cliente/usuário específico
- ✅ Editar informações de um cliente/usuário existente
- ✅ Excluir cliente/usuário
- ✅ Validação de formulários
- ✅ Interface responsiva com Bootstrap

## 🛠️ Tecnologias utilizadas

- [PHP](https://www.php.net/)
- [Laravel](https://laravel.com/) — Framework PHP
- [MySQL](https://www.mysql.com/) — Banco de dados
- [Bootstrap](https://getbootstrap.com/) — Estilização do front-end
- [Blade](https://laravel.com/docs/blade) — Motor de templates do Laravel
- [Composer](https://getcomposer.org/) — Gerenciador de dependências PHP

## 📦 Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina:

- PHP >= 8.1
- Composer
- MySQL (ou outro banco de dados compatível)
- Node.js e NPM (para compilar os assets, caso necessário)

## 🚀 Instalação e configuração

Clone o repositório:

```bash
git clone https://github.com/NicolasPontes/Crud_Laravel.git
cd Crud_Laravel
```

Instale as dependências do PHP:

```bash
composer install
```

Copie o arquivo de variáveis de ambiente e gere a chave da aplicação:

```bash
cp .env.example .env
php artisan key:generate
```

Configure as credenciais do banco de dados MySQL no arquivo `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nome_do_banco
DB_USERNAME=seu_usuario
DB_PASSWORD=sua_senha
```

Execute as migrations para criar as tabelas no banco de dados:

```bash
php artisan migrate
```

(Opcional) Instale as dependências de front-end e compile os assets:

```bash
npm install
npm run dev
```

Inicie o servidor de desenvolvimento:

```bash
php artisan serve
```

A aplicação estará disponível em `http://localhost:8000`.

## 📁 Estrutura do projeto

```
Crud_Laravel/
├── app/
│   ├── Http/Controllers/   # Controllers responsáveis pelas operações CRUD
│   └── Models/             # Models (Eloquent) representando as entidades
├── database/
│   └── migrations/         # Migrations das tabelas do banco
├── resources/
│   └── views/               # Views Blade (formulários e listagens)
├── routes/
│   └── web.php              # Definição das rotas da aplicação
└── public/                  # Arquivos públicos (CSS, JS, imagens)
```

## 🗺️ Rotas principais

| Método   | Rota                | Ação                          |
|----------|----------------------|--------------------------------|
| GET      | `/clientes`           | Lista todos os clientes        |
| GET      | `/clientes/create`    | Formulário de cadastro         |
| POST     | `/clientes`           | Salva um novo cliente          |
| GET      | `/clientes/{id}`      | Exibe detalhes de um cliente   |
| GET      | `/clientes/{id}/edit` | Formulário de edição           |
| PUT      | `/clientes/{id}`      | Atualiza um cliente existente  |
| DELETE   | `/clientes/{id}`      | Remove um cliente               |

> As rotas seguem o padrão de resource routes do Laravel (`Route::resource`).

## 🧑‍💻 Autor

Desenvolvido por **[Nicolas Pontes](https://github.com/NicolasPontes)**.

## 📄 Licença

Este projeto está sob a licença MIT.
