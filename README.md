# Sistema de Gerenciamento de Pedidos - Boilerplate

Um sistema completo de gerenciamento de pedidos desenvolvido como boilerplate para pequenas lojas, oferecendo funcionalidades tanto para clientes quanto para vendedores.

## 🚀 Tecnologias Utilizadas

### Frontend
- **Angular 19** - Framework principal
- **Tailwind CSS** - Framework de estilização (a definir vs Bootstrap)
- **TypeScript** - Linguagem de programação

### Backend
- **NestJS** - Framework Node.js
- **TypeORM** - ORM para gerenciamento de dados
- **TypeScript** - Linguagem de programação

### Banco de Dados
- **PostgreSQL** - Sistema de gerenciamento de banco de dados

### Infraestrutura
- **Docker** - Containerização da aplicação
- **Docker Compose** - Orquestração dos containers

## 📋 Funcionalidades

### Para Clientes
- [ ] Catálogo de produtos
- [ ] Carrinho de compras
- [ ] Finalização de pedidos
- [ ] Acompanhamento de status dos pedidos
- [ ] Histórico de compras
- [ ] Perfil do usuário

### Para Vendedores
- [ ] Dashboard administrativo
- [ ] Gerenciamento de produtos
- [ ] Controle de estoque
- [ ] Gerenciamento de pedidos
- [ ] Relatórios de vendas
- [ ] Gestão de clientes

## 🏗️ Arquitetura do Projeto

```
backend/
    ├── src/
        ├── app.controller.spec.ts
        ├── app.controller.ts
        ├── app.module.ts
        ├── app.service.ts
        └── main.ts
    ├── test/
        ├── app.e2e-spec.ts
        └── jest-e2e.json
    ├── .env.example
    ├── .prettierrc
    ├── eslint.config.mjs
    ├── nest-cli.json
    ├── package-lock.json
    ├── package.json
    ├── README.md
    ├── tsconfig.build.json
    └── tsconfig.json
frontend/
    ├── .vscode/
        ├── extensions.json
        ├── launch.json
        └── tasks.json
    ├── public/
        └── favicon.ico
    ├── src/
        ├── app/
            ├── app.component.html
            ├── app.component.scss
            ├── app.component.spec.ts
            ├── app.component.ts
            ├── app.config.server.ts
            ├── app.config.ts
            └── app.routes.ts
        ├── index.html
        ├── main.server.ts
        ├── main.ts
        ├── server.ts
        └── styles.scss
    ├── .editorconfig
    ├── .gitignore
    ├── angular.json
    ├── package-lock.json
    ├── package.json
    ├── README.md
    ├── tsconfig.app.json
    ├── tsconfig.json
    └── tsconfig.spec.json
.gitignore
gerenciamento-vendas-boilerplate.code-workspace
LICENSE
README.md
```

## 🐳 Configuração com Docker

### Pré-requisitos
- Docker
- Docker Compose

### Executando o projeto

1. Clone o repositório:
```bash
git clone https://github.com/s0lturn3/gerenciamento-vendas-boilerplate.git
cd gerenciamento-vendas-boilerplate
```

2. Copie o arquivo de ambiente:
```bash
cp .env.example .env
```

3. Configure as variáveis de ambiente no arquivo `.env`:
```env
# Database
DB_HOST=postgres
DB_PORT=5432
DB_USERNAME=orderdb_user
DB_PASSWORD=orderdb_password
DB_DATABASE=orderdb

# JWT
JWT_SECRET=your-super-secret-jwt-key
JWT_EXPIRES_IN=7d

# Application
API_PORT=3000
FRONTEND_PORT=4200
```

4. Execute o projeto:
```bash
docker-compose up -d
```

### Serviços disponíveis:
- **Frontend (Angular)**: http://localhost:4200
- **Backend (NestJS)**: http://localhost:3000
- **PostgreSQL**: localhost:5432
- **Adminer** (opcional): http://localhost:8080

## 🛠️ Desenvolvimento Local

### Backend (NestJS)

```bash
cd backend
npm install
npm run start:dev
```

### Frontend (Angular)

```bash
cd frontend
npm install
npm run start
```

## 📊 Modelo de Dados (Planejado)

### Principais Entidades:
- **Users** - Usuários do sistema (clientes e vendedores)
- **Products** - Produtos disponíveis
- **Categories** - Categorias de produtos
- **Orders** - Pedidos realizados
- **OrderItems** - Itens dos pedidos
- **Cart** - Carrinho de compras
- **Inventory** - Controle de estoque

## 🔧 Scripts Disponíveis

### Backend
```bash
npm run start          # Inicia a aplicação
npm run start:dev      # Inicia em modo desenvolvimento
npm run start:debug    # Inicia em modo debug
npm run build          # Build da aplicação
npm run test           # Executa testes
npm run migration:run  # Executa migrações
npm run seed           # Executa seeds
```

### Frontend
```bash
npm run start          # Inicia o servidor de desenvolvimento
npm run build          # Build para produção
npm run test           # Executa testes unitários
npm run e2e            # Executa testes e2e
npm run lint           # Executa linter
```

## 🎯 Objetivos do Boilerplate

Este projeto serve como:
- **Template base** para projetos de e-commerce
- **Referência de arquitetura** para sistemas de pedidos
- **Demonstração de tecnologias** Angular + NestJS + PostgreSQL
- **Estudo de caso** para implementação de features comuns

## 📝 Notas de Desenvolvimento

### Decisões Arquiteturais:
- **Modularização**: Frontend e backend organizados em módulos
- **TypeORM**: Escolhido pela integração nativa com NestJS
- **JWT**: Autenticação stateless
- **Docker**: Ambiente padronizado e portável

### Próximos Passos:
- [ ] Implementar autenticação JWT
- [ ] Criar estrutura de módulos no Angular
- [ ] Definir entidades do TypeORM
- [ ] Implementar CRUD básico de produtos
- [ ] Configurar interceptors e guards

## 🤝 Como Usar Este Boilerplate

1. **Fork/Clone** este repositório
2. **Renomeie** conforme seu projeto
3. **Customize** as entidades conforme necessário
4. **Adapte** as funcionalidades ao seu domínio
5. **Implemente** features específicas do seu negócio

## 📚 Recursos Úteis

- [Angular Documentation](https://angular.io/docs)
- [NestJS Documentation](https://docs.nestjs.com/)
- [TypeORM Documentation](https://typeorm.io/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)

---

**Nota**: Este é um projeto boilerplate para fins de demonstração e estudo. Não possui deploy configurado e destina-se ao uso local para desenvolvimento e consulta.
