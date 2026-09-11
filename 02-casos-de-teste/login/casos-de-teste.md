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
Validar o acesso à aplicação com credenciais válidas.

**Pré-condição:**  
Possuir credenciais válidas.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de login.
2. Informar um e-mail válido.
3. Informar uma senha válida.
4. Clicar no botão **Entrar**.

**Resultado esperado:**

O sistema deve autenticar o usuário e permitir o acesso à aplicação.

**Status:** PASSOU

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

1. Acessar a tela de login.
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

1. Acessar a tela de login.
2. Informar um e-mail em formato inválido.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o login e apresentar a mensagem:

`Formato de email inválido. Use: nome@dominio.com`

**Status:** PASSOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Formato de email inválido. Use: nome@dominio.com`

---

### CT-LOGIN-004 — Login sem informar o e-mail

**Objetivo:**  
Validar o comportamento do sistema quando o campo de e-mail não for preenchido.

**Massa de teste:**
- E-mail: vazio
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de login.
2. Não preencher o campo de e-mail.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve informar que o campo de e-mail é obrigatório.

**Status:** PASSOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Email e senha são obrigatórios`

**Observação:**

Embora apenas o campo de e-mail tenha sido deixado vazio, a aplicação exibe uma mensagem genérica informando que ambos os campos são obrigatórios.

---

### CT-LOGIN-005 — Login sem informar a senha

**Objetivo:**  
Validar o comportamento do sistema quando o campo de senha não é preenchido.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: vazio

**Passos:**

1. Acessar a tela de login.
2. Informar um e-mail válido.
3. Não preencher o campo de senha.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve informar que o campo de senha é obrigatório.

**Status:** PASSOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Email e senha são obrigatórios`

**Observação:**

Embora apenas o campo de senha tenha sido deixado vazio, a aplicação exibe uma mensagem genérica informando que ambos os campos são obrigatórios.

---

### CT-LOGIN-006 — Login sem preencher os campos

**Objetivo:**  
Validar o comportamento do sistema quando nenhum campo estiver preenchido.

**Massa de teste:**

- E-mail: vazio
- Senha: vazio

**Passos:**

1. Acessar a tela de login.
2. Não preencher nenhum campo.
3. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve apresentar a mensagem:

`Email e senha são obrigatórios`

**Status:** PASSOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Email e senha são obrigatórios`

---

### CT-LOGIN-007 — Login com senha abaixo do tamanho mínimo

**Objetivo:**  
Validar a regra de tamanho mínimo da senha.

**Massa de teste:**
- E-mail: `admin@qatest.com`
- Senha: `12345`

**Passos:**

1. Acessar a tela de login.
2. Informar um e-mail válido.
3. Informar uma senha com 5 caracteres.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o login e apresentar a mensagem:

`Senha deve ter pelo menos 6 caracteres`

**Status:** PASSOU

---

### CT-LOGIN-008 — Login com usuário não cadastrado

**Objetivo:**  
Validar o comportamento do sistema quando for informado um e-mail que não pertence a um usuário cadastrado.

**Massa de teste:**
- E-mail: `usuario.inexistente@qatest.com`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de login.
2. Informar um e-mail não cadastrado.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o acesso e apresentar a mensagem:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Status:** PASSOU

---

### CT-LOGIN-009 — E-mail com formato inválido

**Objetivo:**  
Validar o comportamento da aplicação para um e-mail que não possui um domínio válido.

**Massa de teste:**
- E-mail: `usuario@`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de login.
2. Informar um e-mail com formato inválido.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve impedir o login e apresentar a mensagem em formato de e-mail inválido.

**Status:** PASSOU

---

### CT-LOGIN-010 — Acesso à tela de cadastro pelo link "Cadastre-se"

**Objetivo:**  
Validar o redirecionamento para a tela de cadastro.

**Passos:**

1. Acessar a tela de login.
2. Clicar no link **Cadastre-se**.

**Resultado esperado:**

O sistema deve redirecionar o usuário para a tela de cadastro.

**Status:** PASSOU

---

### CT-LOGIN-011 — Login utilizando e-mail com letras maiúsculas

**Objetivo:**  
Validar o comportamento do sistema quando o e-mail for informado em letras maiúsculas.

**Massa de teste:**
- E-mail: `ADMIN@QATEST.COM`
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de login.
2. Informar o e-mail em letras maiúsculas.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

**Resultado esperado:**

O sistema deve tratar o endereço de e-mail de acordo com a regra definida pela aplicação, não devendo impedir o acesso exclusivamente pela utilização de letras maiúsculas no endereço.

**Status:** NÃO PASSOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Observação:**

O usuário cadastrado com o endereço `admin@qatest.com` não foi reconhecido quando o mesmo endereço foi informado como `ADMIN@QATEST.COM`.

---

### CT-LOGIN-012 — Login com espaços no e-mail

**Objetivo:**  
Validar o comportamento da aplicação quando o e-mail contiver espaços antes ou depois do valor.

**Massa de teste:**
- E-mail: ` admin@qatest.com `
- Senha: `Teste@123`

**Passos:**

1. Acessar a tela de login.
2. Informar um e-mail que contenha espaços antes e/ou depois do endereço.
3. Informar uma senha válida.
4. Clicar em **Entrar**.

**Resultado esperado:**

O sistema deve tratar espaços em branco no início ou no final do endereço de e-mail conforme a regra definida para o campo, evitando que espaços excedentes impeçam a autenticação de um endereço válido.

**Status:** NÃO PASSOU

**Resultado obtido:**

O sistema apresentou a mensagem:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Observação:**

O sistema não realizou o tratamento dos espaços antes e depois do endereço de e-mail, resultando na não identificação do usuário cadastrado.

---

## 4. Resumo dos casos

| ID | Cenário | Tipo | Status |
|---|---|---|---|
| CT-LOGIN-001 | Login com credenciais válidas | Positivo | ✅ PASSOU |
| CT-LOGIN-002 | Login com senha inválida | Negativo | ❌ FALHOU — BUG-001  |
| CT-LOGIN-003 | Login com e-mail inválido | Negativo | ✅ PASSOU  |
| CT-LOGIN-004 | Login sem e-mail | Negativo | ✅ PASSOU* |
| CT-LOGIN-005 | Login sem senha | Negativo | ✅ PASSOU*|
| CT-LOGIN-006 | Login sem campos | Negativo | ✅ PASSOU |
| CT-LOGIN-007 | Senha abaixo do mínimo | Limite | ✅ PASSOU |
| CT-LOGIN-008 | Usuário não cadastrado | Negativo | ✅ PASSOU |
| CT-LOGIN-009 | Domínio de e-mail inválido | Negativo | ✅ PASSOU |
| CT-LOGIN-010 | Acesso ao cadastro | Navegação | ✅ PASSOU |
| CT-LOGIN-011 | E-mail em letras maiúsculas | Exploratório | ❌ NÃO PASSOU |
| CT-LOGIN-012 | Espaços no e-mail | Exploratório | ❌ NÃO PASSOU |

---

## 5. Observações

Os casos de teste poderão ser atualizados durante a execução caso sejam identificados novos comportamentos, regras ou cenários relevantes.

Novos casos de teste identificados durante testes exploratórios deverão ser documentados e adicionados ao conjunto de testes.

\* Os CT-LOGIN-004 e CT-LOGIN-005 foram considerados aprovados porque a aplicação impediu o login e apresentou uma mensagem de obrigatoriedade. Entretanto, foi observada a utilização de uma mensagem genérica para ambos os cenários.
