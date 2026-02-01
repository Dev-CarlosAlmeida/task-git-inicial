# 📌 Guia de Tarefas do Repositório

## 🤝 Contexto do Projeto

Este repositório faz parte de um **trabalho colaborativo entre amigos**, com foco em **aprendizado prático de Git e GitHub em um ambiente que simula o contexto real de uma empresa**.

O objetivo principal é **preparar para o mercado de trabalho**, aprendendo na prática como:

* Trabalhar em equipe com outros desenvolvedores
* Seguir um fluxo profissional de versionamento
* Utilizar branches, Pull Requests e revisões de código
* Evitar erros comuns em ambientes corporativos

Todo o processo aqui descrito simula o dia a dia de um time de desenvolvimento, como ocorre em empresas de tecnologia.

Este documento descreve **todas as tasks solicitadas**, com **passo a passo detalhado**, incluindo **onde executar cada ação** (GitHub Web, terminal ou VS Code) e **boas práticas de commits**.

---

## 🧩 Visão Geral das Tasks

1. Criar repositório privado, branch e Pull Request inicial *(Pull Request: solicitação para revisar e integrar código de uma branch em outra)*
2. Bloquear commits diretos na `main` *(proteção da branch principal para evitar alterações diretas)*
3. Criar branch `develop` *(branch usada para desenvolvimento contínuo antes de ir para produção)*
4. Criar padrão de Pull Request (`pull_request.md` — arquivo que define o modelo obrigatório ao abrir um Pull Request)*
5. Iniciar projeto com estrutura básica HTML, CSS e JavaScript *(base inicial do projeto front-end)*

---

## 🛠️ Task 01 — Repositório, Branch e Pull Request

### 🎯 Objetivo

Criar o fluxo básico de trabalho com branch e Pull Request.

### ✅ Passo a passo

#### 1️⃣ Criar repositório privado

**Onde:** GitHub (navegador)

* Acesse o GitHub
* Clique em **New repository**
* Nomeie o repositório
* Marque como **Private**
* Não marque README automático
* Crie o repositório

---

#### 2️⃣ Convidar colaborador

**Onde:** GitHub

* Entre no repositório
* Vá em **Settings > Collaborators**
* Clique em **Add people**
* Convide o usuário solicitado

---

#### 3️⃣ Clonar o repositório

**Onde:** Terminal (Git Bash ou PowerShell)

```bash
git clone URL_DO_REPOSITORIO
cd nome-do-repositorio
```

---

#### 4️⃣ Criar nova branch

**Onde:** Terminal

```bash
git checkout -b feat/init-repository
```

---

#### 5️⃣ Criar README.md

**Onde:** VS Code

* Crie o arquivo `README.md`
* Escreva qualquer conteúdo inicial

Exemplo:

```md
# Projeto Inicial

Repositório criado para fins de estudo e prática de Git.
```

---

#### 6️⃣ Commit seguindo convenção

**Onde:** Terminal

```bash
git add README.md
git commit -m "feat: adiciona readme inicial"
```

---

#### 7️⃣ Push da branch

```bash
git push origin feat/init-repository
```

---

#### 8️⃣ Abrir Pull Request

**Onde:** GitHub

* Vá até o repositório
* Clique em **Compare & pull request**
* Base: `main`
* Compare: `feat/init-repository`
* Crie o Pull Request
* Aguarde aprovação

---

## 🔒 Task 02 — Bloquear commits diretos na `main`

### 🎯 Objetivo

Garantir que alterações só entrem via Pull Request.

### ✅ Passo a passo

**Onde:** GitHub

1. Vá em **Settings > Branches**
2. Clique em **Add branch protection rule**
3. Em *Branch name pattern*, digite: `main`
4. Marque:

   * ✅ Require a pull request before merging
   * ✅ Require approvals
5. Salve as regras

📌 Resultado: ninguém consegue dar `push` direto na `main`.

---

## 🌱 Task 03 — Criar branch `develop`

### 🎯 Objetivo

Separar ambiente de desenvolvimento da branch principal.

### ✅ Passo a passo

**Onde:** Terminal

```bash
git checkout main
git pull origin main
git checkout -b develop
git push origin develop
```

---

## 📝 Task 04 — Padrão de Pull Request *(define um modelo padrão para todos os Pull Requests do projeto)*

### 🎯 Objetivo

Padronizar solicitações de Pull Request.

### ✅ Passo a passo

**Onde:** VS Code

1. Crie a pasta:

```bash
.github
```

2. Dentro dela, crie o arquivo:

```text
pull_request.md
```

3. Conteúdo sugerido:

```md
## 📌 Descrição
Descreva claramente o que foi feito neste Pull Request.

## 🧪 Como testar
Explique como validar as alterações.

## ✅ Checklist
- [ ] Código testado
- [ ] Sem erros de lint
- [ ] Segue padrão de commits
```

---

#### Commit

```bash
git add .
git commit -m "chore: adiciona template de pull request"
git push origin develop
```

---

## 🧱 Task 05 — Estrutura básica HTML, CSS e JS

### 🎯 Objetivo

Criar estrutura inicial do projeto front-end.

### 📂 Estrutura de pastas

```text
project-root/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── README.md
```

---

### 🧩 Conteúdo básico

#### index.html

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Projeto Base</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <h1>Hello World</h1>
  <script src="js/script.js"></script>
</body>
</html>
```

#### style.css

```css
body {
  font-family: Arial, sans-serif;
}
```

#### script.js

```js
console.log("Projeto iniciado");
```

---

#### Commit

```bash
git add .
git commit -m "feat: cria estrutura base html css js"
git push origin develop
```

---

## 📏 Convenção de Commits *(regras para padronizar mensagens de commit no Git)*

Formato:

```text
tipo: descrição curta
```

Tipos usados:

* `feat`: nova funcionalidade
* `fix`: correção de bug
* `chore`: tarefas de manutenção
* `docs`: documentação

Exemplos:

* `feat: adiciona estrutura inicial do projeto`
* `chore: configura regras da branch main`

---

## 🔄 Continuidade do Projeto

Este repositório **não possui uma conclusão final**, pois faz parte de um processo contínuo de aprendizado e evolução.

Novas tasks, melhorias de estrutura, ajustes de fluxo e boas práticas serão adicionados conforme o avanço dos estudos e das simulações de trabalho em equipe, refletindo o que ocorre em ambientes reais de desenvolvimento de software.

O objetivo é manter o projeto vivo, evolutivo e alinhado às práticas utilizadas por equipes profissionais.
