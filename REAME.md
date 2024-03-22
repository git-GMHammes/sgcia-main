SGCIA - Serviço de Gestão de Comunicações e Informações Administrativas
markdown# 📋 SGCIA - Serviço de Gestão de Comunicações e Informações Administrativas

Sistema completo para gestão de comunicações internas, documentos administrativos e fluxo de informações corporativas.

## 🎯 Sobre o Projeto

O SGCIA é uma plataforma web moderna desenvolvida para centralizar e organizar toda a comunicação administrativa de empresas e instituições. O sistema permite o gerenciamento eficiente de memorandos, circulares, comunicados, ofícios e demais documentos administrativos, proporcionando rastreabilidade completa e controle de versões.

## 🚀 Tecnologias Utilizadas

### Backend

- **CodeIgniter 4** - Framework PHP
- **MySQL 8.0+** - Banco de dados relacional
- **JWT** - Autenticação via tokens
- **RESTful API** - Arquitetura de comunicação

### Frontend

- **React 18+** - Biblioteca JavaScript
- **React Router DOM** - Roteamento
- **Axios** - Requisições HTTP
- **React Hook Form** - Gerenciamento de formulários
- **TailwindCSS** - Estilização
- **Lucide React** - Ícones

### Ferramentas de Desenvolvimento

- **Docker & Docker Compose** - Containerização
- **Git** - Controle de versão
- **Composer** - Gerenciador de dependências PHP
- **npm/yarn** - Gerenciador de dependências JS

## ✨ Funcionalidades Principais

### Gestão de Comunicações

- ✅ Criação, edição e exclusão de comunicados
- ✅ Categorização por tipo (Memorando, Circular, Ofício, Comunicado)
- ✅ Sistema de prioridades (Baixa, Normal, Alta, Urgente)
- ✅ Controle de status (Rascunho, Publicado, Arquivado)
- ✅ Anexo de documentos (PDF, DOC, XLS, imagens)
- ✅ Histórico de versões

### Gestão de Usuários

- ✅ Autenticação segura com JWT
- ✅ Níveis de acesso (Administrador, Gestor, Usuário)
- ✅ Gerenciamento de perfis
- ✅ Logs de auditoria

### Painel Administrativo

- ✅ Dashboard com métricas e indicadores
- ✅ Relatórios de comunicações
- ✅ Pesquisa avançada com filtros
- ✅ Notificações em tempo real
- ✅ Exportação de dados (PDF, Excel)

### Workflow de Aprovação

- ✅ Fluxo de aprovação configurável
- ✅ Assinatura digital de documentos
- ✅ Notificações automáticas
- ✅ Rastreamento de status

## 📁 Estrutura do Projeto

```
sgcia/
├── backend/                    # API CodeIgniter 4
│   ├── app/
│   │   ├── Config/
│   │   │   ├── Routes.php
│   │   │   ├── Database.php
│   │   │   └── Validation.php
│   │   ├── Controllers/
│   │   │   ├── Auth/
│   │   │   │   ├── LoginController.php
│   │   │   │   └── RegisterController.php
│   │   │   ├── Api/
│   │   │   │   ├── ComunicacaoController.php
│   │   │   │   ├── UsuarioController.php
│   │   │   │   ├── DepartamentoController.php
│   │   │   │   └── RelatorioController.php
│   │   │   └── BaseController.php
│   │   ├── Models/
│   │   │   ├── ComunicacaoModel.php
│   │   │   ├── UsuarioModel.php
│   │   │   ├── DepartamentoModel.php
│   │   │   ├── AnexoModel.php
│   │   │   └── LogModel.php
│   │   ├── Filters/
│   │   │   ├── AuthFilter.php
│   │   │   └── CorsFilter.php
│   │   ├── Libraries/
│   │   │   ├── JWTLibrary.php
│   │   │   └── UploadLibrary.php
│   │   └── Database/
│   │       ├── Migrations/
│   │       └── Seeds/
│   ├── public/
│   ├── writable/
│   ├── .env
│   ├── composer.json
│   └── spark
│
├── frontend/                   # Aplicação React
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   │   ├── Header.jsx
│   │   │   │   ├── Sidebar.jsx
│   │   │   │   ├── Footer.jsx
│   │   │   │   └── Loading.jsx
│   │   │   ├── forms/
│   │   │   │   ├── ComunicacaoForm.jsx
│   │   │   │   └── UsuarioForm.jsx
│   │   │   ├── tables/
│   │   │   │   └── DataTable.jsx
│   │   │   └── modals/
│   │   │       └── ConfirmModal.jsx
│   │   ├── pages/
│   │   │   ├── Dashboard/
│   │   │   │   └── index.jsx
│   │   │   ├── Comunicacoes/
│   │   │   │   ├── List.jsx
│   │   │   │   ├── Create.jsx
│   │   │   │   ├── Edit.jsx
│   │   │   │   └── View.jsx
│   │   │   ├── Usuarios/
│   │   │   │   ├── List.jsx
│   │   │   │   └── Profile.jsx
│   │   │   ├── Relatorios/
│   │   │   │   └── index.jsx
│   │   │   └── Auth/
│   │   │       ├── Login.jsx
│   │   │       └── Register.jsx
│   │   ├── services/
│   │   │   ├── api.js
│   │   │   ├── auth.service.js
│   │   │   ├── comunicacao.service.js
│   │   │   └── usuario.service.js
│   │   ├── contexts/
│   │   │   └── AuthContext.jsx
│   │   ├── hooks/
│   │   │   ├── useAuth.js
│   │   │   └── useFetch.js
│   │   ├── utils/
│   │   │   ├── helpers.js
│   │   │   └── validators.js
│   │   ├── routes/
│   │   │   ├── PrivateRoute.jsx
│   │   │   └── index.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── .env
│   ├── package.json
│   ├── tailwind.config.js
│   └── vite.config.js
│
├── database/
│   ├── schema.sql
│   └── seed.sql
│
├── docker/
│   ├── nginx/
│   │   └── default.conf
│   ├── php/
│   │   └── Dockerfile
│   └── mysql/
│       └── my.cnf
│
├── docker-compose.yml
├── .gitignore
└── README.md
```

## 🗄️ Modelo de Banco de Dados

### Principais Tabelas

#### usuarios

```sql
CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    senha VARCHAR(255) NOT NULL,
    cpf VARCHAR(14) UNIQUE NOT NULL,
    cargo VARCHAR(50),
    departamento_id INT,
    nivel_acesso ENUM('admin', 'gestor', 'usuario') DEFAULT 'usuario',
    ativo BOOLEAN DEFAULT TRUE,
    foto_perfil VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (departamento_id) REFERENCES departamentos(id)
);
```

#### comunicacoes

```sql
CREATE TABLE comunicacoes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    numero_protocolo VARCHAR(50) UNIQUE NOT NULL,
    tipo ENUM('memorando', 'circular', 'oficio', 'comunicado') NOT NULL,
    titulo VARCHAR(200) NOT NULL,
    conteudo TEXT NOT NULL,
    prioridade ENUM('baixa', 'normal', 'alta', 'urgente') DEFAULT 'normal',
    status ENUM('rascunho', 'publicado', 'arquivado') DEFAULT 'rascunho',
    departamento_origem_id INT NOT NULL,
    departamento_destino_id INT,
    usuario_criador_id INT NOT NULL,
    data_publicacao DATETIME,
    data_validade DATE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (departamento_origem_id) REFERENCES departamentos(id),
    FOREIGN KEY (departamento_destino_id) REFERENCES departamentos(id),
    FOREIGN KEY (usuario_criador_id) REFERENCES usuarios(id)
);
```

#### departamentos

```sql
CREATE TABLE departamentos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    sigla VARCHAR(10) NOT NULL,
    responsavel_id INT,
    ativo BOOLEAN DEFAULT TRUE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    FOREIGN KEY (responsavel_id) REFERENCES usuarios(id)
);
```

#### anexos

```sql
CREATE TABLE anexos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    comunicacao_id INT NOT NULL,
    nome_arquivo VARCHAR(255) NOT NULL,
    caminho_arquivo VARCHAR(500) NOT NULL,
    tipo_arquivo VARCHAR(50),
    tamanho_bytes INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (comunicacao_id) REFERENCES comunicacoes(id) ON DELETE CASCADE
);
```

#### logs_auditoria

```sql
CREATE TABLE logs_auditoria (
    id INT AUTO_INCREMENT PRIMARY KEY,
    usuario_id INT NOT NULL,
    acao VARCHAR(50) NOT NULL,
    tabela_afetada VARCHAR(50),
    registro_id INT,
    dados_anteriores JSON,
    dados_novos JSON,
    ip_address VARCHAR(45),
    user_agent TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (usuario_id) REFERENCES usuarios(id)
);
```

## 🔧 Pré-requisitos

### Requisitos de Sistema

- **Docker** 20.10+
- **Docker Compose** 1.29+
- **Git** 2.0+

### Sem Docker

- **PHP** 8.1+
- **Composer** 2.0+
- **MySQL** 8.0+
- **Node.js** 18+
- **npm** ou **yarn**

## 📦 Instalação

### 1. Clone o Repositório

```bash
git clone https://github.com/seu-usuario/sgcia.git
cd sgcia
```

### 2. Configuração com Docker (Recomendado)

#### Backend

```bash
cd backend
cp .env.example .env
# Edite o arquivo .env com suas configurações
```

Arquivo `.env` do backend:

```env
CI_ENVIRONMENT = development

database.default.hostname = mysql
database.default.database = sgcia_db
database.default.username = sgcia_user
database.default.password = sgcia_password
database.default.DBDriver = MySQLi
database.default.port = 3306

app.baseURL = 'http://localhost:8080'
app.indexPage = ''

JWT_SECRET = sua_chave_secreta_muito_segura_aqui_123
JWT_ALGORITHM = HS256
JWT_EXPIRATION = 3600

# Configurações de upload
app.uploadPath = writable/uploads/
app.maxFileSize = 10485760
app.allowedTypes = pdf,doc,docx,xls,xlsx,jpg,jpeg,png
```

#### Frontend

```bash
cd ../frontend
cp .env.example .env
```

Arquivo `.env` do frontend:

```env
VITE_API_URL=http://localhost:8080/api
VITE_APP_NAME=SGCIA
VITE_APP_VERSION=1.0.0
```

#### Docker Compose

```bash
cd ..
docker-compose up -d
```

Arquivo `docker-compose.yml`:

```yaml
version: "3.8"

services:
  mysql:
    image: mysql:8.0
    container_name: sgcia_mysql
    environment:
      MYSQL_ROOT_PASSWORD: root_password
      MYSQL_DATABASE: sgcia_db
      MYSQL_USER: sgcia_user
      MYSQL_PASSWORD: sgcia_password
    ports:
      - "3306:3306"
    volumes:
      - mysql_data:/var/lib/mysql
      - ./database/schema.sql:/docker-entrypoint-initdb.d/1-schema.sql
      - ./database/seed.sql:/docker-entrypoint-initdb.d/2-seed.sql
    networks:
      - sgcia_network

  backend:
    build:
      context: ./docker/php
      dockerfile: Dockerfile
    container_name: sgcia_backend
    working_dir: /var/www/html
    volumes:
      - ./backend:/var/www/html
    ports:
      - "8080:80"
    depends_on:
      - mysql
    networks:
      - sgcia_network
    environment:
      - CI_ENVIRONMENT=development

  frontend:
    image: node:18-alpine
    container_name: sgcia_frontend
    working_dir: /app
    volumes:
      - ./frontend:/app
    ports:
      - "3000:3000"
    command: sh -c "npm install && npm run dev -- --host"
    networks:
      - sgcia_network

volumes:
  mysql_data:

networks:
  sgcia_network:
    driver: bridge
```

### 3. Instalação sem Docker

#### Backend

```bash
cd backend
composer install
cp .env.example .env
# Configure o arquivo .env
php spark migrate
php spark db:seed MainSeeder
php spark serve
```

#### Frontend

```bash
cd frontend
npm install
# ou: yarn install
cp .env.example .env
npm run dev
# ou: yarn dev
```

## 🚀 Executando o Projeto

### Com Docker

```bash
docker-compose up -d
```

Acesse:

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8080
- **MySQL**: localhost:3306

### Sem Docker

Terminal 1 (Backend):

```bash
cd backend
php spark serve
```

Terminal 2 (Frontend):

```bash
cd frontend
npm run dev
```

## 📡 Endpoints da API

### Autenticação

```
POST   /api/auth/login          # Login de usuário
POST   /api/auth/register       # Registro de novo usuário
POST   /api/auth/logout         # Logout
POST   /api/auth/refresh        # Renovar token
GET    /api/auth/me             # Dados do usuário autenticado
```

### Comunicações

```
GET    /api/comunicacoes                    # Listar todas
POST   /api/comunicacoes                    # Criar nova
GET    /api/comunicacoes/:id                # Detalhes
PUT    /api/comunicacoes/:id                # Atualizar
DELETE /api/comunicacoes/:id                # Excluir
GET    /api/comunicacoes/:id/anexos         # Listar anexos
POST   /api/comunicacoes/:id/anexos         # Upload anexo
GET    /api/comunicacoes/tipo/:tipo         # Filtrar por tipo
GET    /api/comunicacoes/status/:status     # Filtrar por status
```

### Usuários

```
GET    /api/usuarios            # Listar todos
POST   /api/usuarios            # Criar novo
GET    /api/usuarios/:id        # Detalhes
PUT    /api/usuarios/:id        # Atualizar
DELETE /api/usuarios/:id        # Excluir
PUT    /api/usuarios/:id/status # Ativar/Desativar
```

### Departamentos

```
GET    /api/departamentos       # Listar todos
POST   /api/departamentos       # Criar novo
GET    /api/departamentos/:id   # Detalhes
PUT    /api/departamentos/:id   # Atualizar
DELETE /api/departamentos/:id   # Excluir
```

### Relatórios

```
GET    /api/relatorios/comunicacoes     # Relatório de comunicações
GET    /api/relatorios/usuarios         # Relatório de usuários
GET    /api/relatorios/departamentos    # Relatório de departamentos
POST   /api/relatorios/export/pdf       # Exportar para PDF
POST   /api/relatorios/export/excel     # Exportar para Excel
```

## 🔐 Autenticação

O sistema utiliza JWT (JSON Web Tokens) para autenticação. Após o login, inclua o token no header das requisições:

```javascript
headers: {
  'Authorization': 'Bearer seu_token_aqui',
  'Content-Type': 'application/json'
}
```

### Níveis de Acesso

- **admin**: Acesso total ao sistema
- **gestor**: Gerenciamento de comunicações e usuários do departamento
- **usuario**: Visualização e criação de comunicações

## 🧪 Testes

### Backend

```bash
cd backend
composer test
```

### Frontend

```bash
cd frontend
npm run test
# ou: yarn test
```

## 📊 Dashboard - Exemplos de Métricas

- Total de comunicações (período)
- Comunicações por tipo
- Comunicações por status
- Comunicações por prioridade
- Usuários ativos
- Departamentos cadastrados
- Gráfico de comunicações por mês
- Top 5 usuários mais ativos
- Comunicações aguardando aprovação

## 🎨 Screenshots

_(Adicione screenshots do sistema aqui)_

## 🤝 Contribuindo

1. Faça um Fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

## 📝 Padrões de Código

### Backend (PHP/CodeIgniter 4)

- PSR-12 para estilo de código
- Documentação PHPDoc
- Validações em todos os inputs
- Uso de Models para acesso ao banco
- Controllers enxutos (lógica nos Models/Libraries)

### Frontend (React)

- ESLint + Prettier
- Componentes funcionais com Hooks
- Props typing com PropTypes
- Nomenclatura em camelCase
- Componentização reutilizável

## 🐛 Reportar Bugs

Encontrou um bug? Abra uma [issue](https://github.com/seu-usuario/sgcia/issues) detalhando:

- Descrição do problema
- Passos para reproduzir
- Comportamento esperado
- Screenshots (se aplicável)
- Ambiente (SO, navegador, versões)

## 📜 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👥 Autores

- **Seu Nome** - _Desenvolvimento Inicial_ - [seu-usuario](https://github.com/seu-usuario)

## 🙏 Agradecimentos

- CodeIgniter Framework
- React Team
- Comunidade Open Source

## 📞 Contato

- Email: contato@sgcia.com.br
- Website: https://sgcia.com.br
- LinkedIn: [SGCIA](https://linkedin.com/company/sgcia)

---

**SGCIA** - Sistema de Gestão de Comunicações e Informações Administrativas
Desenvolvido com ❤️ usando CodeIgniter 4, React e MySQL

✅ README.md completo e pronto para uso!
