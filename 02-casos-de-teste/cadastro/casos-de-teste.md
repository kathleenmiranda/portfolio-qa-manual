# 👤 Casos de Teste — Cadastro

## 1. Objetivo

Validar a funcionalidade de criação de conta, verificando o comportamento da aplicação diante de dados válidos e inválidos, de campos obrigatórios e de diferentes condições de validação.

## 2. Pré-condições

- A aplicação deve estar disponível.
- O usuário deve estar na tela **Criar Conta**.
- Para os cenários de cadastro válido, exibir um e-mail que ainda não esteja cadastrado.

---

## 3. Casos de teste

### CT-CAD-001 — Cadastro com dados válidos

**Objetivo:** Validar a criação de uma nova conta exibindo dados válidos.

**Pré-condição:** E-mail utilizado ainda não cadastrado.

**Dados de teste:**
- Nome: `João Silva`
- E-mail: utilizar um e-mail válido e não cadastrado
- Senha: `SenhaForte@123`
- Confirmação: `SenhaForte@123`

**Passos:**
1. Acessar a tela Criar Conta.
2. Informar um nome válido.
3. Informar um e-mail válido e não cadastrado.
4. Informar uma senha que atenda a todos os requisitos.
5. Repetir a senha no campo de confirmação.
6. Clicar em **Cadastrar**.

**Resultado esperado:**
A conta deve ser criada com sucesso e a aplicação deve apresentar o comportamento esperado após o cadastro.

**Status:** Não executado

---

### CT-CAD-002 — Cadastro sem informar o nome

**Objetivo:** Validar a obrigatoriedade do campo "Nome Completo".

**Dados de teste:**
- Nome: vazio
- E-mail: e-mail válido
- Senha: `SenhaForte@123`
- Confirmação: `SenhaForte@123`

**Passos:**
1. Acessar a tela Criar Conta.
2. Deixar o campo "Nome Completo" vazio.
3. Preencher os demais campos com dados válidos.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, e o sistema deve exibir uma indicação de que o campo "Nome Completo" é obrigatório.

**Status:** Não executado

---

### CT-CAD-003 — Cadastro sem informar o e-mail

**Objetivo:** Validar a obrigatoriedade do campo "e-mail".

**Dados de teste:**
- Nome: `João Silva`
- E-mail: vazio
- Senha: `SenhaForte@123`
- Confirmação: `SenhaForte@123`

**Passos:**
1. Acessar a tela Criar Conta.
2. Preencher o Nome Completo.
3. Deixar o campo E-mail vazio.
4. Preencher os campos de senha com dados válidos.
5. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, e o sistema deve exibir uma indicação de que o campo E-mail é obrigatório.

**Status:** Não executado

---

### CT-CAD-004 — Cadastro sem informar a senha

**Objetivo:** Validar a obrigatoriedade do campo "Senha".

**Dados de teste:**
- Nome: `João Silva`
- E-mail: e-mail válido
- Senha: vazio
- Confirmação: vazio

**Passos:**
1. Acessar a tela Criar Conta.
2. Preencher Nome Completo e E-mail.
3. Deixar os campos de senha em branco.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, e o sistema deve exibir uma indicação de que a senha é obrigatória.

**Status:** Não executado

---

### CT-CAD-005 — Cadastro sem confirmar a senha

**Objetivo:** Validar a obrigatoriedade do campo "Confirme a Senha".

**Dados de teste:**
- Nome: `João Silva`
- E-mail: e-mail válido
- Senha: `SenhaForte@123`
- Confirmação: vazio

**Passos:**
1. Preencher Nome Completo.
2. Informar um e-mail válido.
3. Informar uma senha válida.
4. Deixar o campo "Confirme a Senha" em branco.
5. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, e o sistema deve exibir uma indicação de que a confirmação da senha é obrigatória.

**Status:** Não executado

---

### CT-CAD-006 — Cadastro com todos os campos vazios

**Objetivo:** Validar o comportamento da aplicação quando nenhum campo é preenchido.

**Passos:**
1. Acessar a tela Criar Conta.
2. Não preencher nenhum campo.
3. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado e o sistema deve apresentar as validações correspondentes aos campos obrigatórios.

**Status:** Não executado

---

### CT-CAD-007 — E-mail com formato inválido

**Objetivo:** Validar a validação do formato do endereço de e-mail.

**Dados de teste:**
- E-mail: `usuario@`

**Passos:**
1. Preencher os campos obrigatórios com dados válidos.
2. Informar um e-mail em formato inválido.
3. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, e o sistema deve exibir uma mensagem ou indicação de que o formato de e-mail é inválido.

**Status:** Não executado

---

### CT-CAD-008 — Senha com menos de 8 caracteres

**Objetivo:** Validar o limite mínimo de caracteres da senha.

**Dados de teste:**
- Senha: `Senha@1`

**Passos:**
1. Preencher os campos obrigatórios.
2. Informar uma senha com 7 caracteres.
3. Confirmar a mesma senha.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, pois a senha deve ter no mínimo 8 caracteres.

**Status:** Não executado

---

### CT-CAD-009 — Senha sem letra minúscula

**Objetivo:** Validar o requisito de pelo menos uma letra minúscula.

**Dados de teste:**
- Senha: `SENHA@123`

**Passos:**
1. Preencher os campos obrigatórios.
2. Informar uma senha sem letras minúsculas.
3. Confirmar a mesma senha.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, pois a senha deve conter pelo menos uma letra minúscula.

**Status:** Não executado

---

### CT-CAD-010 — Senha sem letra maiúscula

**Objetivo:** Validar o requisito de pelo menos uma letra maiúscula.

**Dados de teste:**
- Senha: `senha@123`

**Passos:**
1. Preencher os campos obrigatórios.
2. Informar uma senha sem letras maiúsculas.
3. Confirmar a mesma senha.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, pois a senha deve conter pelo menos uma letra maiúscula.

**Status:** Não executado

---

### CT-CAD-011 — Senha sem número

**Objetivo:** Validar o requisito de pelo menos um número.

**Dados de teste:**
- Senha: `SenhaForte@`

**Passos:**
1. Preencher os campos obrigatórios.
2. Informar uma senha sem números.
3. Confirmar a mesma senha.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, pois a senha deve conter pelo menos um dígito numérico.

**Status:** Não executado

---

### CT-CAD-012 — Senha sem caractere especial

**Objetivo:** Validar o requisito de pelo menos um caractere especial.

**Dados de teste:**
- Senha: `SenhaForte123`

**Passos:**
1. Preencher os campos obrigatórios.
2. Informar uma senha sem caracteres especiais.
3. Confirmar a mesma senha.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado, pois a senha deve conter pelo menos um caractere especial.

**Status:** Não executado

---

### CT-CAD-013 — Senha e confirmação diferentes

**Objetivo:** Validar se o sistema impede o cadastro quando a senha e a confirmação são diferentes.

**Dados de teste:**
- Senha: `SenhaForte@123`
- Confirmação: `SenhaForte@124`

**Passos:**
1. Preencher os campos obrigatórios.
2. Informar uma senha válida.
3. Informar uma confirmação diferente da senha.
4. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado e o sistema deve informar que as senhas não correspondem.

**Status:** Não executado

---

### CT-CAD-014 — Cadastro com e-mail já existente

**Objetivo:** Validar o comportamento da aplicação ao tentar cadastrar um e-mail que já possui uma conta.

**Dados de teste:**
- Utilizar um e-mail previamente cadastrado.

**Passos:**
1. Preencher os campos obrigatórios com dados válidos.
2. Informar um e-mail já cadastrado.
3. Clicar em **Cadastrar**.

**Resultado esperado:**
O cadastro não deve ser realizado e o sistema deve informar que o e-mail já está cadastrado ou apresentar o comportamento definido pela aplicação.

**Status:** Não executado

---

### CT-CAD-015 — Navegação pelo botão Voltar

**Objetivo:** Validar a navegação da tela Criar Conta para a tela anterior.

**Passos:**
1. Acessar a tela Criar Conta.
2. Clicar em **Voltar**.

**Resultado esperado:**
O usuário deve retornar à tela anterior.

**Status:** Não executado

---

### CT-CAD-016 — Navegação para Login pela opção "faça login na sua conta existente"

**Objetivo:** Validar a navegação da tela Criar Conta para a tela de Login por meio da opção disponível para usuários que já possuem uma conta.

**Passos:**
1. Acessar a tela Criar Conta.
2. Clicar na opção **"faça login na sua conta existente"**.

**Resultado esperado:**
O usuário deve ser direcionado para a tela de Login.

**Status:** Não executado

---

## 4. Resumo dos casos de teste

| ID | Cenário | Tipo | Status |
|---|---|---|---|
| CT-CAD-001 | Cadastro com dados válidos | Positivo | Não executado |
| CT-CAD-002 | Nome não informado | Negativo | Não executado |
| CT-CAD-003 | E-mail não informado | Negativo | Não executado |
| CT-CAD-004 | Senha não informada | Negativo | Não executado |
| CT-CAD-005 | Confirmação não informada | Negativo | Não executado |
| CT-CAD-006 | Todos os campos vazios | Negativo | Não executado |
| CT-CAD-007 | E-mail com formato inválido | Negativo | Não executado |
| CT-CAD-008 | Senha abaixo do mínimo | Limite | Não executado |
| CT-CAD-009 | Senha sem letra minúscula | Validação | Não executado |
| CT-CAD-010 | Senha sem letra maiúscula | Validação | Não executado |
| CT-CAD-011 | Senha sem número | Validação | Não executado |
| CT-CAD-012 | Senha sem caractere especial | Validação | Não executado |
| CT-CAD-013 | Senhas diferentes | Negativo | Não executado |
| CT-CAD-014 | E-mail já cadastrado | Negativo | Não executado |
| CT-CAD-015 | Botão Voltar | Navegação | Não executado |
| CT-CAD-016 | Navegação para Login pela opção "faça login na sua conta existente" | Navegação | Não executado |
