## 2º entrega do Projeto Integrador Grupo 26 

Este projeto tem por objetivo atender as demandas do quarto semestre da disciplina de Projeto Integrador: Desenvolvimento de sistemas orientado a Dispositivos Móveis e Baseados na Web 


## Integrantes do grupo e suas equipes:
### Projeto de Banco de Dados
- DANIEL DE OLIVEIRA SOLANO LOPES

### Projeto de Back End
- EDUARDO AUGUSTO DA SILVA ROSA
- HENRIQUE BARREIRO SANTANA
- VINICIUS PEREIRA DE SOUZA 

### Projeto de Front End
- ICARO GOES MOREIRA
- MARCELLY CERDEIRINHA MARCIOTO
- MIRIAM VIEGAS DE JESUS

### Integração dos projetos
- HENRIQUE BARREIRO SANTANA
- VINICIUS PEREIRA DE SOUZA
- MIRIAM VIEGAS DE JESUS

## Apresentação do projeto

- O projeto consiste em um sistema integrado para atender um sistema de gestão voltado a pet shops de pequeno porte, com o objetivo de centralizar informações, otimizar processos internos e fortalecer o relacionamento com clientes por meio de ferramentas de comunicação automatizadas.
- Este projeto inicialmente consistiu em um sistema que contemplará funcionalidades de cadastro de clientes, fornecedores, funcionários e pets, além de módulos para controle de estoque, compras, vendas e agendamentos de serviços, integrados a lembretes automáticos via WhatsApp. O sistema busca reduzir erros manuais, aumentar a eficiência operacional e fornecer relatórios gerenciais que apoiem a tomada de decisões estratégicas. 
  
### Revisita ao projeto
- Dadas as limitações de tempo para a realização do projeto, o desenvolvimento da parte de integração entre os sistema desenvolvido e o serviço de comunicação WhatsApp foi removida, de maneira que o projeto não possui os sistemas de comunicação ou de agendamento de serviços que inicialmente foram levantados.

---
## ⚙️ Tecnologias utilizadas
### Back End
- Node.js + Express, para criação do ambiente de execução e framework web para criação da API.
- TypeScript, foi a Linguagem principal para código.

### Banco de Dados
- PostgreSQL, foi utilizado para o Banco de dados relacional.

### Front End
- Foram utilizadas HTML, CSS e JavaScrip.



📦 Estrutura do projeto

```
new-repositorio/
├── assets/
│   ├── css/        # Contém os arquivos CSS do projeto
│   ├── img/        # Contém as imagens utilizadas no projeto
│   └── js/         # Contém os arquivos JavaScript do projeto
│
├── back-end/
│   ├── .vs/        # Contém os arquivos de cache do banco de dados e utiliza Node.js
│   ├── js/         # Contém os arquivos JavaScript do projeto
│   └── src/        # Contém os arquivos do backend
│
├── .cadastro_cliente/
│   ├── clientes.html                # Página de Clientes
│   └── cadastro_cliente.html        # Página de cadastro de clientes
│
├── produtos/
│   ├── produtos.html                # Página de Produtos
│   ├── cadastro_produtos.html       # Cadastro para alimentar a tabela de produtos
│   ├── editar_produto.html          # Edição de produtos cadastrados
│   ├── editar_categoria_grupos.html # Edição da categoria de grupos
│   └── editar_categoria_setores.html# Edição da categoria de setores
│
├── header.html        # Menu principal utilizado pelas páginas
├── index.html         # Página principal do projeto
└── telainicial.html   # Página de apresentação do projeto
```

## 🧩 Pré-requisitos

- Node.js (v18+)
- MySQL (pode ser local via **XAMPP**, **MySQL Workbench** ou **Docker**)

---

## 🗄️ Banco de Dados

### 🧱 1. Criar o banco

No **MySQL Workbench**, execute o comando SQL abaixo:

```sql
CREATE DATABASE projeto_faculdade;
```

### 📤 2. Importar o arquivo .sql

- Abra o MySQL Workbench
- Vá em Server > Data Import
- Selecione Import from Self-Contained File
- Escolha o arquivo banco_inicial.sql (presente no repositório)
- Em Default Target Schema, selecione ou crie projeto_faculdade
- Clique em Start Import

Esse arquivo contém as tabelas iniciais necessárias, como usuarios.

---

## ⚙️ Variáveis de ambiente

Crie um arquivo .env na raiz do projeto com base no modelo abaixo:

```
DB_NAME=projeto_faculdade
DB_USER=root
DB_PASS=
DB_HOST=localhost
PORT=3000
SESSION_SECRET=sua_chave_aqui
```

⚠️ Se você usa o XAMPP, provavelmente o usuário é root e a senha fica vazia.
⚙️ Se você usa Docker, ajuste conforme o docker-compose.yml.

---

## 🐳 Rodando com Docker (opcional)

Se preferir usar Docker, basta ter o Docker e Docker Compose instalados.

1. Suba o container MySQL:

```
docker compose up -d
```

2. O banco projeto_faculdade será criado automaticamente.
3. Configure o .env com as mesmas credenciais do docker-compose.yml.

---

## 🚀 Rodando o servidor

1. Instale as dependências:

```
npm install
```

2. Inicie o servidor em modo desenvolvimento:

```
npm run dev
```

3. Acesse no navegador:
   http://localhost:8080/api

Se aparecer:

```
{ "message": "API funcionando!" }
```

---

## 🧑‍💻 Contribuindo

1. Faça o clone do repositório:

```
git clone https://github.com/seu-usuario/projeto-faculdade-backend.git
```

2. Crie sua branch:

```
git checkout -b feature/nome-da-feature
```

1. Faça suas alterações e commits:

```
git commit -m "Adiciona rota de login"
```

4. Envie para o GitHub:

```
git push origin feature/nome-da-feature
```

5. Crie um Pull Request.

---

## 🧾 Licença

Este projeto é apenas para fins acadêmicos (trabalho de faculdade).
Todos os direitos reservados ao grupo do projeto.
