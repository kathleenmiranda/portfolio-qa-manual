# 🔐 Casos de Teste — Login

## 1. Objetivo

Validar o comportamento da funcionalidade de Login, considerando os fluxos de sucesso, validações dos campos, credenciais inválidas e navegação para o cadastro de usuários.

---

## 2. Pré-condições gerais

- Aplicação disponível para acesso;
- Usuário deve estar na tela de Login;
- Para o cenário de sucesso, utilizar uma credencial válida disponibilizada pela aplicação.

---

## 3. Casos de Teste

### CT-LOGIN-001 — Login com credenciais válidas

**Objetivo:**  
Validar o acesso à aplicação utilizando credenciais válidas.

**Pré-condição:**  
Possuir credenciais válidas.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail válido.
3. Informar uma senha válida.
4. Clicar no botão **Entrar**.

**Resultado esperado:**

O sistema deve autenticar o usuário e permitir o acesso à aplicação.

**Status:** Não executado

---

### CT-LOGIN-002 — Login com senha inválida

**Objetivo:**  
Validar o comportamento do sistema quando o usuário informa uma senha incorreta.

**Pré-condição:**  
Possuir um e-mail de usuário cadastrado.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: `SenhaIncorreta123`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail cadastrado.
3. Informar uma senha incorreta.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o acesso e apresentar a mensagem:

`Email ou senha inválidos`

**Resultado:** FALHOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Bug:** BUG-001

---

### CT-LOGIN-003 — Login com e-mail inválido

**Objetivo:**  
Validar a validação do formato do e-mail informado.

**Massa de teste:**
- E-mail: `email-invalido`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail em formato inválido.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o login e apresentar a mensagem:

`Formato de email inválido. Use: nome@dominio.com`

**Status:** Não executado

---

### CT-LOGIN-004 — Login sem informar o e-mail

**Objetivo:**  
Validar o comportamento do sistema quando o campo de e-mail não é preenchido.

**Massa de teste:**
- E-mail: vazio
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Não preencher o campo de e-mail.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve informar que o campo de e-mail é obrigatório.

**Status:** Não executado

---

### CT-LOGIN-005 — Login sem informar a senha

**Objetivo:**  
Validar o comportamento do sistema quando o campo de senha não é preenchido.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: vazio

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail válido.
3. Não preencher o campo de senha.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve informar que o campo de senha é obrigatório.

**Status:** Não executado

---

### CT-LOGIN-006 — Login sem preencher os campos

**Objetivo:**  
Validar o comportamento do sistema quando nenhum campo é preenchido.

**Massa de teste:**

- E-mail: vazio
- Senha: vazio

**Passos:**

1. Acessar a tela de Login.
2. Não preencher nenhum campo.
3. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve apresentar a mensagem:

`Email e senha são obrigatórios`

**Status:** Não executado

---

### CT-LOGIN-007 — Login com senha abaixo do tamanho mínimo

**Objetivo:**  
Validar a regra de tamanho mínimo da senha.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: `12345`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail válido.
3. Informar uma senha com 5 caracteres.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o login e apresentar a mensagem:

`Senha deve ter pelo menos 6 caracteres`

**Status:** Não executado

---

### CT-LOGIN-008 — Login com usuário não cadastrado

**Objetivo:**  
Validar o comportamento do sistema quando é informado um e-mail que não pertence a um usuário cadastrado.

**Massa de teste:**
- E-mail: `usuario.inexistente@qatest.com`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail não cadastrado.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o acesso e apresentar a mensagem:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Status:** Não executado

---

### CT-LOGIN-009 — E-mail com domínio inválido

**Objetivo:**  
Validar o comportamento da aplicação para um e-mail com domínio incompleto ou inválido.

**Massa de teste:**
- E-mail: `usuario@`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail com formato inválido.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o login e apresentar a mensagem de formato de e-mail inválido.

**Status:** Não executado

---

### CT-LOGIN-010 — Acesso à tela de cadastro pelo link "Cadastre-se"

**Objetivo:**  
Validar o redirecionamento para a tela de cadastro.

**Passos:**

1. Acessar a tela de Login.
2. Clicar no link **Cadastre-se**.

**Resultado esperado:**

O sistema deve redirecionar o usuário para a tela de cadastro.

**Status:** Não executado

---

### CT-LOGIN-011 — Login utilizando e-mail com letras maiúsculas

**Objetivo:**  
Validar o comportamento do sistema quando o e-mail é informado utilizando letras maiúsculas.

**Massa de teste:**
- E-mail: `ADMIN@QATEST.COM`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Informar o e-mail utilizando letras maiúsculas.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve apresentar o comportamento definido para o tratamento de letras maiúsculas no e-mail.

**Status:** Não executado

---

### CT-LOGIN-012 — Login com espaços no e-mail

**Objetivo:**  
Validar o comportamento da aplicação quando o e-mail contém espaços antes ou depois do valor.

**Massa de teste:**
- E-mail: ` admin@qatest.com `
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de Login.
2. Informar um e-mail contendo espaços antes e/ou depois do endereço.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve tratar os espaços conforme a regra definida para o campo de e-mail.

**Status:** Não executado

---

## 4. Resumo dos casos

| ID | Cenário | Tipo | Status |
|---|---|---|---|
| CT-LOGIN-001 | Login com credenciais válidas | Positivo | ✅ PASSOU |
| CT-LOGIN-002 | Login com senha inválida | Negativo | ❌ FALHOU — BUG-001 |
| CT-LOGIN-003 | Login com e-mail inválido | Negativo | Não executado |
| CT-LOGIN-004 | Login sem e-mail | Negativo | Não executado |
| CT-LOGIN-005 | Login sem senha | Negativo | Não executado |
| CT-LOGIN-006 | Login sem campos | Negativo | Não executado |
| CT-LOGIN-007 | Senha abaixo do mínimo | Limite | Não executado |
| CT-LOGIN-008 | Usuário não cadastrado | Negativo | Não executado |
| CT-LOGIN-009 | Domínio de e-mail inválido | Negativo | Não executado |
| CT-LOGIN-010 | Acesso ao cadastro | Navegação | Não executado |
| CT-LOGIN-011 | E-mail em letras maiúsculas | Exploratório | Não executado |
| CT-LOGIN-012 | Espaços no e-mail | Exploratório | Não executado |

---

## 5. Observações

Os casos de teste poderão ser atualizados durante a execução caso sejam identificados novos comportamentos, regras ou cenários relevantes.

Novos casos de teste identificados durante testes exploratórios deverão ser documentados e adicionados ao conjunto de testes.
