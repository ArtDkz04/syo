# 🏢 Gerenciador Patrimonial (Syo.Patrimônio)

Sistema web para gestão de ativos corporativos, controle de estoque, termos de responsabilidade e histórico de manutenção.

> **Status:** Refatorado para arquitetura modular (Frontend/Backend separados) e containerizada.

---

## 🚀 Tecnologias Utilizadas

### Infraestrutura
* **Docker & Docker Compose:** Orquestração dos serviços.
* **Nginx:** Servidor Web e Proxy Reverso.
* **PostgreSQL 14:** Banco de dados relacional.

### Backend
* **Node.js & Express:** API RESTful.
* **JWT:** Autenticação segura.
* **Multer:** Upload de imagens e arquivos (PDFs/Notas Fiscais).

### Frontend
* **HTML5 & CSS3:** Estrutura e estilização (com variáveis CSS nativas e Tailwind via CDN).
* **JavaScript (ES6 Modules):** Arquitetura modular (`app.js`, `api.js`, `components.js`, etc.).
* **Bibliotecas:** Chart.js (Gráficos), HTML2PDF (Geração de Termos), IMask (Máscaras de input).

---

## 📂 Estrutura do Projeto

A aplicação foi refatorada para separar responsabilidades:

```text
.
├── backend/                # API Node.js
│   ├── public/             # Arquivos estáticos (uploads, avatares)
│   ├── server.js           # Ponto de entrada da API
│   ├── create-admin.js     # Script para criar primeiro admin
│   └── Dockerfile          # Configuração da imagem do Backend
├── frontend/               # Interface do Usuário
│   ├── css/                # Estilos isolados
│   ├── js/                 # Lógica modular (API, Utils, PDF, App)
│   └── index.html          # Entrypoint limpo
├── docker-compose.yml      # Orquestração dos containers
├── nginx.conf              # Configuração do Proxy
└── README.md               # Documentação
