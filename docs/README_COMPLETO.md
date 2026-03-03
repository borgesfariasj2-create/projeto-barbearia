# 📁 Estrutura Completa do Projeto - SaaS Barbearia

## Visão Geral do Projeto

Este é um sistema SaaS (Software as a Service) para gerenciamento de barbearias, desenvolvido por 3 pessoas:
- **Amigo 1**: Frontend (HTML, CSS, JavaScript puro)
- **Amigo 2**: Backend (Node.js + Express)
- **Amigo 3**: Análise de Dados (Python)

---

## 📂 Estrutura de Pastas

```
projeto/
├── frontend/                    # 🎨 Frontend (Amigo 1)
│   ├── index.html              # Página inicial
│   ├── css/
│   │   └── style.css           # Estilos globais
│   ├── js/
│   │   └── main.js             # Funções JavaScript principais
│   └── pages/
│       ├── agendamento.html    # Página de agendamentos
│       ├── servicos.html       # Página de serviços
│       └── login.html          # Página de login
│
├── backend/                     # ⚙️ Backend (Amigo 2)
│   ├── package.json            # Dependências npm
│   ├── server.js               # Arquivo principal do servidor
│   ├── .env.example            # Exemplo de variáveis de ambiente
│   └── src/
│       ├── routes/
│       │   ├── usuarios.js     # Rotas de usuários
│       │   ├── servicos.js     # Rotas de serviços
│       │   └── agendamentos.js # Rotas de agendamentos
│       ├── controllers/
│       │   ├── usuariosController.js
│       │   ├── servicosController.js
│       │   └── agendamentosController.js
│       └── models/
│           ├── database.js     # Conexão com MySQL
│           ├── usuarioModel.js
│           ├── servicoModel.js
│           └── agendamentoModel.js
│
├── data-analysis/               # 📊 Análise de Dados (Amigo 3)
│   ├── main.py                 # Script principal
│   ├── requirements.txt        # Dependências Python
│   └── analises/
│       ├── relatorio_receitas.py
│       ├── analise_clientes.py
│       └── analise_servicos.py
│
├── database/                    # 💾 Scripts de Banco de Dados
│   └── schema.sql              # Schema do MySQL
│
├── docs/                        # 📝 Documentação
│   └── README_COMPLETO.md      # Este arquivo
│
└── .gitignore                   # Arquivos ignorados pelo Git
```

---

## 🎯 O que Cada Pessoa Deve Fazer

### 👤 Amigo 1 - Frontend (HTML, CSS, JS)
**Pasta:** `frontend/`

Trabalhar em:
- `index.html` - Landing page
- `pages/agendamento.html` - Página de agendamento
- `pages/servicos.html` - Lista de serviços
- `pages/login.html` - Página de login
- `css/style.css` - Todos os estilos
- `js/main.js` - Todas as funcionalidades JS

**Comunica com:** Backend via API REST

---

### 👤 Amigo 2 - Backend (Node.js + Express)
**Pasta:** `backend/`

Trabalhar em:
- `server.js` - Configuração do servidor Express
- `src/routes/` - Todas as rotas da API
- `src/controllers/` - Lógica de negócio
- `src/models/` - Conexão e queries MySQL
- `.env` - Variáveis de ambiente

**API Endpoints esperados:**
- `GET/POST /api/usuarios`
- `GET/POST /api/servicos`
- `GET/POST /api/agendamentos`

---

### 👤 Amigo 3 - Análise de Dados (Python)
**Pasta:** `data-analysis/`

Trabalhar em:
- `main.py` - Orquestrador de análises
- `analises/relatorio_receitas.py` - Relatórios financeiros
- `analises/analise_clientes.py` - Análise de clientes
- `analises/analise_servicos.py` - Análise de serviços populares

**Bibliotecas:** pandas, numpy, matplotlib, seaborn

---

## 🚀 Como Rodar o Projeto

### 1. Banco de Dados (MySQL)
```sql
-- Execute o conteúdo do arquivo database/schema.sql
mysql -u root -p < database/schema.sql
```

### 2. Backend
```bash
cd backend
npm install
# Configure o arquivo .env
cp .env.example .env
# Edite o .env com suas configurações
npm start
```

### 3. Frontend
```bash
# Abra o arquivo frontend/index.html no navegador
# Ou use um servidor local:
cd frontend
npx serve .
```

### 4. Análise de Dados
```bash
cd data-analysis
pip install -r requirements.txt
python main.py
```

---

## 📊 Modelo de Dados

### Tabelas principais:
- **usuarios**: Clientes, barbeiros e administradores
- **servicos**: Tipos de serviço (corte, barba, etc)
- **agendamentos**: Agendamentos realizados

---

## 🔗 Comunicação entre Partes

```
Frontend (Browser)
      │
      ▼ HTTP Requests
Backend (Node.js)
      │
      ▼ SQL Queries  
MySQL Database
      │
      ▼ Export Data
Python Analysis
```

---

## 📝 Observações

1. O frontend faz requisições HTTP para o backend
2. O backend conecta no MySQL e retorna JSON
3. O Python lê dados do MySQL para análises
4. Todos devem seguir o mesmo schema de banco de dados
5. Configurem as variáveis de ambiente corretamente

