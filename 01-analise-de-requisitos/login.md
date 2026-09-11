# 🔐 Análise de Requisitos — Login

## 1. Objetivo

Analisar a funcionalidade de autenticação da aplicação, identificando os elementos disponíveis na tela, regras de validação, mensagens apresentadas ao usuário e comportamentos que deverão ser considerados durante a elaboração dos casos de teste.

---

## 2. Funcionalidade analisada

**Módulo:** Login

**Objetivo:** Permitir que um usuário autenticado acesse a aplicação por meio de suas credenciais.

---

## 3. Elementos identificados

### Campos

- E-mail
- Senha

### Botões

- Entrar

### Links

- Cadastre-se

### Credenciais disponibilizadas para teste

A aplicação disponibiliza credenciais destinadas à realização dos testes de autenticação.

> Observação: por se tratar de um ambiente público de estudo, as credenciais exibidas pela própria aplicação não representam dados reais de usuários.

---

## 4. Regras e validações identificadas

Durante a análise da tela de login, foram identificadas as seguintes validações:

### 4.1 Campos obrigatórios

O sistema deve validar o preenchimento dos campos de e-mail e senha.

Mensagem identificada:

`Email e senha são obrigatórios`

### 4.2 Formato do e-mail

O sistema deve validar se o valor informado no campo de e-mail possui um formato válido.

Mensagem identificada:

`Formato de email inválido. Use: nome@dominio.com`

### 4.3 Tamanho mínimo da senha

O sistema deve validar se a senha possui pelo menos 6 caracteres.

Mensagem identificada:

`Senha deve ter pelo menos 6 caracteres`

### 4.4 Usuário não encontrado

O sistema apresenta uma mensagem específica quando o e-mail informado não corresponde a um usuário cadastrado.

Mensagem identificada:

`Usuário não encontrado. Verifique o email ou cadastre-se.`

### 4.5 Credenciais inválidas

O sistema apresenta uma mensagem de erro quando as credenciais informadas não são válidas.

Mensagem identificada:

`Email ou senha inválidos`

---

## 5. Fluxo principal

O fluxo principal identificado para a funcionalidade é:

1. Usuário acessa a tela de login;
2. Informa um e-mail;
3. Informa uma senha;
4. Seleciona o botão **Entrar**;
5. Sistema valida as credenciais;
6. Em caso de credenciais válidas, o usuário deve ser autenticado e acessar a aplicação.

---

## 6. Fluxos alternativos

A partir das validações identificadas, devem ser considerados os seguintes fluxos:

- Usuário não informa o e-mail;
- Usuário não informa a senha;
- Usuário não informa nenhum dos campos;
- Usuário informa e-mail em formato inválido;
- Usuário informa senha com menos de 6 caracteres;
- Usuário informa e-mail de usuário inexistente;
- Usuário informa senha incorreta;
- Usuário informa credenciais inválidas;
- Usuário seleciona o link **Cadastre-se**.

---

## 7. Pontos de atenção para os testes

Durante a elaboração dos casos de teste, deverão ser consideradas:

- Validação dos campos obrigatórios;
- Validação do formato do e-mail;
- Validação do tamanho mínimo da senha;
- Diferenciação entre usuário inexistente e credenciais inválidas;
- Mensagens apresentadas ao usuário;
- Autenticação com credenciais válidas;
- Redirecionamento após login;
- Acesso ao cadastro por meio do link **Cadastre-se**;
- Comportamento da aplicação diante de diferentes combinações de dados inválidos.

---

## 8. Riscos identificados

Os principais riscos relacionados à funcionalidade são:

- Permitir autenticação com credenciais inválidas;
- Permitir acesso sem o preenchimento dos campos obrigatórios;
- Aceitar e-mails em formato inválido;
- Aceitar senhas abaixo do tamanho mínimo;
- Apresentar mensagens incorretas ou inconsistentes;
- Não realizar o redirecionamento esperado após autenticação;
- Permitir acesso à aplicação sem autenticação.

---

## 9. Cenários que serão derivados da análise

Com base nos requisitos e comportamentos identificados, serão elaborados casos de teste para validar:

- Login com credenciais válidas;
- Login com senha inválida;
- Login com e-mail inválido;
- Login com usuário inexistente;
- Login sem preenchimento dos campos;
- Login sem e-mail;
- Login sem senha;
- Login com senha abaixo do limite mínimo;
- Navegação para a tela de cadastro;
- Mensagens de validação e erro.

---

## 10. Evidência da análise

A tela analisada apresenta os campos de e-mail e senha, botão de entrada, acesso ao cadastro e credenciais destinadas aos testes.

As evidências de execução serão armazenadas no diretório:

`04-evidencias/login/`
