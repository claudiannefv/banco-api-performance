# 🧪 Testes de Performance com JavaScript e k6

Repositório de testes de performance para a API do projeto **Banco API**, utilizando a ferramenta [k6](https://k6.io/) e scripts em JavaScript.

🔗 Repositório: [github.com/claudiannefv/banco-api-performance](https://github.com/claudiannefv/banco-api-performance)

---

## 📌 Introdução

Este projeto tem como objetivo avaliar o desempenho e a resiliência dos endpoints da API utilizando testes de carga e stress com o k6. Os testes ajudam a identificar gargalos e comportamentos inesperados sob alta demanda.

---

## 🚀 Tecnologias Utilizadas

- **k6** – Ferramenta de código aberto para testes de performance.
- **JavaScript (ES6)** – Linguagem utilizada para escrever os scripts.
- **Variáveis de ambiente** – Para configurar dinamicamente o ambiente de execução dos testes.

---

## 🗂️ Estrutura do Repositório

```
banco-api-performance/
├── config/
│   └── config.local.json
├── fixtures/
│   └── postLogin.json
├── helpers/
│   └── autenticacao.js
├── tests/
│   ├── login.test.js
│   ├── transferencias.test.js
│   └── ...
├── utils/
│   └── variaveis.js
├── .gitignore
└── README.md
```

---

## 📁 Objetivo de Cada Grupo de Arquivos

- **`config/`** – Arquivo de configuração de variáveis de ambiente
- **`fixtures/`** – Dados de entrada para os testes (ex: usuários, payloads).
- **`helpers/`** – Funções utilitárias reutilizáveis para interação com a API.
- **`tests/`** – Casos de teste organizados por módulo da API
- **`utils/`** – Funções utilitárias reutilizáveis 
- **`.gitignore`** – Arquivos e pastas ignorados no controle de versão.
- **`README.md`** – Este arquivo com instruções de uso e execução.

---

## 🛠️ Instalação

1. Instale o [k6](https://k6.io/docs/getting-started/installation/) em sua máquina.
2. Clone este repositório:

```bash
git clone https://github.com/claudiannefv/banco-api-performance.git
cd banco-api-performance
```

---

## ▶️ Execução dos Testes

Antes de executar qualquer teste, é necessário definir a variável de ambiente `BASE_URL`, que aponta para o endereço base da API que será testada.

### ✅ Execução simples:

```bash
k6 run tests/login.test.js
```

### 🌐 Definindo a variável `BASE_URL`:

**Windows (PowerShell):**

```powershell
k6 run tests/login.test.js -e BASE_URL = https://localhost:3000
```

**Linux/macOS:**

```bash
k6 run tests/login.test.js -e BASE_URL = https://localhost:3000
```

---

## 📊 Dashboard Web e Exportação de Relatório

Você pode acompanhar a execução em tempo real através de um dashboard web do k6 e exportar o resultado em HTML:

**Windows (PowerShell):**

```powershell
$env:BASE_URL=https://localhost:3000
$env:K6_WEB_DASHBOARD = "true"
$env:K6_WEB_DASHBOARD_EXPORT = "html-report.html"
k6 run tests/login.test.js -e BASE_URL=https://localhost:3000
```

**Linux/macOS:**

```bash
export BASE_URL=https://localhost:3000
export K6_WEB_DASHBOARD=true
export K6_WEB_DASHBOARD_EXPORT=html-report.html
k6 run tests/login.test.js -e BASE_URL=https://localhost:3000
```

O arquivo `html-report.html` será gerado automaticamente com o relatório visual da execução.

---

## 📬 Contato

Caso tenha dúvidas ou sugestões, sinta-se à vontade para abrir uma [issue](https://github.com/claudiannefv/banco-api-performance/issues) ou enviar uma mensagem pelo GitHub.

---
