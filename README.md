# ProntoJá

**O que você precisa, quando você precisa.**

ProntoJá é uma plataforma full-stack projetada para conectar clientes que precisam de serviços com profissionais qualificados. Os usuários podem postar vagas para diversos tipos de trabalho (como eventos, reformas e reparos automotivos) e os profissionais podem se candidatar a elas.

## Tecnologias Utilizadas

*   **Frontend:** React, Vite, React Router
*   **Backend:** Python, Flask, Flask-SQLAlchemy, Flask-JWT-Extended, Flask-Bcrypt
*   **Banco de Dados:** SQLite
*   **Utilitários:** `concurrently` para gerenciamento de processos de desenvolvimento.

## Pré-requisitos

*   Node.js (versão 18 ou superior) e npm
*   Python (versão 3.8 ou superior) e pip

## Instalação

Siga os passos abaixo para configurar o ambiente de desenvolvimento.

### 1. Clone o Repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd ProntoJa-complete
```

### 2. Configure o Backend

O backend precisa de um arquivo `requirements.txt` para instalar as dependências Python.

Crie um arquivo chamado `requirements.txt` dentro da pasta `backend` com o seguinte conteúdo:

```txt
# backend/requirements.txt
Flask
Flask-Cors
Flask-SQLAlchemy
Flask-JWT-Extended
Flask-Bcrypt
```

### 3. Instale as Dependências

Agora que o frontend e o backend estão desacoplados, você deve instalar as dependências de cada um separadamente.

**Para o Frontend:**
```bash
cd frontend
npm install
cd ..
```

Em seguida, execute o script de instalação para as duas partes do projeto:
```bash
npm run install:all
```

Este comando irá executar `npm install` na pasta `frontend` e `pip install -r backend/requirements.txt` na pasta `backend` simultaneamente.

> **Nota:** É uma boa prática de desenvolvimento Python usar um ambiente virtual (`virtualenv`) para isolar as dependências do projeto. Se desejar, crie e ative um antes de rodar o comando `npm run install:all`.

## Rodando em Desenvolvimento

Com as dependências instaladas, você pode rodar ambos os servidores (frontend e backend) com um único comando a partir da pasta raiz do projeto (`ProntoJa-complete`).

```bash
npm run dev
```

Isso iniciará o frontend (geralmente em `http://localhost:5173`) e o backend (em `http://localhost:3001`) simultaneamente no mesmo terminal.
