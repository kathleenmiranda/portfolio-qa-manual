# 🔐 Execução dos Testes — Login

## 1. Objetivo

Registrar os resultados obtidos durante a execução dos casos de teste da funcionalidade de Login, incluindo o status de cada cenário, os comportamentos observados e os defeitos identificados.

---

## 2. Informações da execução

| Informação | Detalhe |
|---|---|
| Funcionalidade | Login |
| Ambiente | Northwind Test Platform |
| Navegador | Google Chrome |
| Tipo de teste | Teste funcional |
| Responsável | Kathleen |
| Data da execução | 11/09/2026 |

---

## 3. Resumo da execução

| ID | Cenário | Resultado | Observação |
|---|---|---|---|
| CT-LOGIN-001 | Login com credenciais válidas | ✅ PASSOU | Login realizado com sucesso |
| CT-LOGIN-002 | Login com senha inválida | ❌ FALHOU | Mensagem apresentada não corresponde ao comportamento esperado. BUG-001 |
| CT-LOGIN-003 | Login com e-mail inválido | ✅ PASSOU | Validação de formato apresentada |
| CT-LOGIN-004 | Login sem e-mail | ✅ PASSOU | Mensagem genérica de obrigatoriedade |
| CT-LOGIN-005 | Login sem senha | ✅ PASSOU | Mensagem genérica de obrigatoriedade |
| CT-LOGIN-006 | Login sem campos | ✅ PASSOU | Mensagem de obrigatoriedade apresentada |
| CT-LOGIN-007 | Senha abaixo do mínimo | ✅ PASSOU | Validação de tamanho mínimo apresentada |
| CT-LOGIN-008 | Usuário não cadastrado | ✅ PASSOU | Mensagem de usuário não encontrado apresentada |
| CT-LOGIN-009 | E-mail com formato inválido | ✅ PASSOU | Validação de e-mail apresentada |
| CT-LOGIN-010 | Acesso à tela de cadastro | ✅ PASSOU | Redirecionamento realizado com sucesso |
| CT-LOGIN-011 | E-mail em letras maiúsculas | ❌ NÃO PASSOU | Usuário não foi reconhecido |
| CT-LOGIN-012 | Espaços no e-mail | ❌ NÃO PASSOU | Usuário não foi reconhecido |

---

## 4. Detalhamento dos resultados

### CT-LOGIN-001 — Login com credenciais válidas

**Resultado:** PASSOU

**Comportamento observado:**

O sistema autenticou o usuário utilizando as credenciais válidas e permitiu o acesso à aplicação.

---

### CT-LOGIN-002 — Login com senha inválida

**Resultado:** FALHOU

**Comportamento observado:**

Ao informar um e-mail de usuário cadastrado com uma senha incorreta, o sistema apresentou a mensagem:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Comportamento esperado:**

O sistema deveria impedir o acesso e apresentar:

`Email ou senha inválidos`

**Defeito identificado:** BUG-001

---

### CT-LOGIN-003 — Login com e-mail inválido

**Resultado:** PASSOU

**Comportamento observado:**

O sistema impediu o login e apresentou:

`Formato de email inválido. Use: nome@dominio.com`

---

### CT-LOGIN-004 — Login sem informar o e-mail

**Resultado:** PASSOU

**Comportamento observado:**

O sistema impediu o login e apresentou:

`Email e senha são obrigatórios`

**Observação:**

Embora apenas o campo de e-mail tenha sido deixado vazio, a aplicação apresentou uma mensagem genérica indicando que ambos os campos são obrigatórios.

---

### CT-LOGIN-005 — Login sem informar a senha

**Resultado:** PASSOU

**Comportamento observado:**

O sistema impediu o login e apresentou:

`Email e senha são obrigatórios`

**Observação:**

Embora apenas o campo de senha tenha sido deixado vazio, a aplicação apresentou uma mensagem genérica indicando que ambos os campos são obrigatórios.

---

### CT-LOGIN-006 — Login sem preencher os campos

**Resultado:** PASSOU

**Comportamento observado:**

O sistema impediu o login e apresentou:

`Email e senha são obrigatórios`

---

### CT-LOGIN-007 — Login com senha abaixo do tamanho mínimo

**Resultado:** PASSOU

**Comportamento observado:**

Ao informar uma senha com 5 caracteres, o sistema apresentou:

`Senha deve ter pelo menos 6 caracteres`

---

### CT-LOGIN-008 — Login com usuário não cadastrado

**Resultado:** PASSOU

**Comportamento observado:**

O sistema impediu o login e apresentou:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

---

### CT-LOGIN-009 — E-mail com formato inválido

**Resultado:** PASSOU

**Comportamento observado:**

O sistema identificou o formato inválido do e-mail e impediu o login.

---

### CT-LOGIN-010 — Acesso à tela de cadastro

**Resultado:** PASSOU

**Comportamento observado:**

Ao clicar no link **Cadastre-se**, o sistema redirecionou o usuário para a tela de cadastro.

---

### CT-LOGIN-011 — Login utilizando e-mail com letras maiúsculas

**Resultado:** NÃO PASSOU

**Massa utilizada:**

`ADMIN@QATEST.COM`

**Comportamento observado:**

O sistema apresentou:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Observação:**

O usuário cadastrado com o endereço `admin@qatest.com` não foi reconhecido quando o endereço foi informado utilizando letras maiúsculas.

**Classificação:**

Cenário exploratório. Necessário avaliar a regra esperada para o tratamento de maiúsculas e minúsculas no endereço de e-mail.

---

### CT-LOGIN-012 — Login com espaços no e-mail

**Resultado:** NÃO PASSOU

**Massa utilizada:**

` admin@qatest.com `

**Comportamento observado:**

O sistema apresentou:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

**Observação:**

O sistema não reconheceu o usuário quando foram adicionados espaços antes e depois do endereço de e-mail.

**Classificação:**

Cenário exploratório. Necessário avaliar a regra esperada para tratamento de espaços no campo de e-mail.

---

## 5. Defeitos identificados

Durante a execução dos testes foi identificado o seguinte defeito:

| Bug | Caso de teste | Descrição | Status |
|---|---|---|---|
| BUG-001 | CT-LOGIN-002 | Mensagem incorreta ao informar senha inválida para usuário cadastrado | Aberto |

---

## 6. Observações gerais

- Os casos de teste foram executados considerando o comportamento observado na aplicação.
- Os cenários exploratórios CT-LOGIN-011 e CT-LOGIN-012 apresentaram comportamento diferente do esperado para a análise realizada.
- Os cenários exploratórios não foram classificados automaticamente como defeitos, sendo necessária a confirmação da regra de negócio.
- As evidências visuais serão armazenadas no diretório `04-evidencias/login/`.
- O BUG-001 deverá ser retestado após a disponibilização de uma correção.

---

## 7. Conclusão

A execução dos testes de Login demonstrou que os principais fluxos de autenticação e validação estão funcionando conforme os cenários definidos.

Foi identificado um defeito relacionado à mensagem apresentada quando um usuário cadastrado informa uma senha inválida.

Também foram identificados dois comportamentos durante testes exploratórios relacionados ao tratamento de letras maiúsculas e espaços no endereço de e-mail, que deverão ser avaliados de acordo com as regras esperadas para a aplicação.
