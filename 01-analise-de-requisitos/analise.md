# 🔎 Análise de Requisitos

## 1. Objetivo

Analisar as funcionalidades disponibilizadas pela aplicação Northwind Test Platform, identificando regras de negócio, comportamentos esperados, possíveis riscos e pontos que deverão ser considerados durante a elaboração e execução dos testes.

## 2. Escopo

Inicialmente serão analisadas as seguintes funcionalidades:

* Login
* Cadastro de usuário
* Categorias
* Produtos
* Fornecedores

## 3. Critérios considerados

Durante a análise dos requisitos serão considerados:

* Fluxos principais;
* Fluxos alternativos;
* Regras de negócio;
* Campos obrigatórios;
* Formatos de dados;
* Limites de campos;
* Mensagens de validação;
* Comportamentos para dados inválidos;
* Permissões e autenticação;
* Integração entre funcionalidades;
* Possíveis cenários de erro.

---

# 🔐 4. Login

## Objetivo da funcionalidade

Permitir que usuários cadastrados acessem a aplicação por meio de suas credenciais.

## Pontos a serem analisados

* Existência dos campos de e-mail e senha;
* Obrigatoriedade dos campos;
* Formato válido do e-mail;
* Validação das credenciais;
* Comportamento para usuário inexistente;
* Comportamento para senha incorreta;
* Mensagens apresentadas ao usuário;
* Comportamento após autenticação;
* Possibilidade de acesso sem autenticação.

## Riscos identificados

* Usuário conseguir acessar a aplicação sem autenticação;
* Sistema aceitar credenciais inválidas;
* Mensagens de erro inconsistentes;
* Falha na validação dos campos;
* Exposição de informações sensíveis.

---

# 👤 5. Cadastro

## Objetivo da funcionalidade

Permitir o cadastro de novos usuários na aplicação.

## Pontos a serem analisados

* Campos obrigatórios;
* Formato dos dados;
* Validação do endereço de e-mail;
* Regras de senha;
* Confirmação de senha;
* E-mail já cadastrado;
* Limites dos campos;
* Mensagens de validação;
* Comportamento após cadastro realizado com sucesso.

## Riscos identificados

* Cadastro de dados inválidos;
* Cadastro duplicado;
* Senha aceita fora das regras estabelecidas;
* Falha na validação dos campos obrigatórios;
* Mensagens de erro incorretas.

---

# 🗂️ 6. Categorias

## Objetivo da funcionalidade

Permitir o gerenciamento de categorias utilizadas pela aplicação.

## Operações a serem analisadas

* Cadastro de categoria;
* Edição de categoria;
* Validação dos dados;
* Campos obrigatórios;
* Limites dos campos;
* Mensagens de sucesso;
* Mensagens de erro.

## Riscos identificados

* Cadastro de categoria sem informações obrigatórias;
* Aceitação de valores acima do limite permitido;
* Falha na edição;
* Dados não persistidos;
* Mensagens apresentadas incorretamente.

---

# 📦 7. Produtos

A análise dessa funcionalidade será realizada posteriormente, considerando as operações disponíveis na aplicação.

Pontos inicialmente considerados:

* Cadastro;
* Consulta;
* Edição;
* Exclusão;
* Campos obrigatórios;
* Validação dos dados;
* Relacionamento com categorias;
* Mensagens de sucesso e erro.

---

# 🏢 8. Fornecedores

A análise dessa funcionalidade será realizada posteriormente, considerando as operações disponibilizadas pela aplicação.

Pontos inicialmente considerados:

* Cadastro;
* Consulta;
* Edição;
* Exclusão;
* Campos obrigatórios;
* Validação dos dados;
* Mensagens de sucesso e erro.

---

# 📌 9. Próximas etapas

Após a análise inicial dos requisitos, serão elaborados:

1. Cenários de teste;
2. Casos de teste;
3. Massa de teste;
4. Execução dos testes;
5. Registro das evidências;
6. Reporte de defeitos;
7. Reteste dos defeitos corrigidos;
8. Testes de regressão;
9. Relatório final.

