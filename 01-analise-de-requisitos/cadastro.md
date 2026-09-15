# 👤 Análise de Requisitos — Cadastro

## 1. Objetivo

Analisar a funcionalidade de criação de conta, identificando os campos disponíveis, as regras de validação, os comportamentos esperados e os possíveis cenários para a elaboração dos casos de teste.

## 2. Funcionalidade

A funcionalidade permite que um novo usuário realize o cadastro na aplicação preenchendo seus dados.

## 3. Campos identificados

| Campo | Obrigatório | Observação |
|---|---|---|
| Nome Completo | Sim | Campo destinado ao nome do usuário |
| E-mail | Sim | Campo destinado ao endereço de e-mail |
| Senha | Sim | Deve atender aos requisitos apresentados na tela |
| Confirme a Senha | Sim | Deve confirmar a senha informada |

## 4. Regras de senha identificadas

A tela apresenta os seguintes requisitos para a senha:

- Mínimo de 8 caracteres;
- Deve conter pelo menos uma letra minúscula;
- Deve conter pelo menos uma letra maiúscula;
- Deve conter pelo menos um número;
- Deve conter pelo menos um caractere especial.

## 5. Elementos de interação

### Cadastrar

Botão responsável por tentar criar a conta após o preenchimento dos campos.

### Voltar

Botão destinado ao retorno à tela anterior.

### Login na sua conta existente

Opção disponibilizada para usuários que já possuem uma conta e desejam acessar a tela de login.

## 6. Pontos a serem validados

Durante a execução dos testes, deverão ser avaliados:

- Cadastro utilizando dados válidos;
- Obrigatoriedade dos campos;
- Formato do e-mail;
- Requisitos mínimos da senha;
- Validação de cada requisito da senha;
- Correspondência entre senha e confirmação de senha;
- Cadastro utilizando e-mail já existente;
- Comportamento diante de dados inválidos;
- Limites dos campos;
- Mensagens apresentadas ao usuário;
- Comportamento do botão Cadastrar;
- Navegação pelo botão Voltar;
- Navegação para Login.

## 7. Observações

As regras e comportamentos que não estiverem explicitamente definidos nesta análise deverão ser validados durante a execução dos testes.

Um comportamento diferente do esperado não será automaticamente classificado como defeito sem que exista uma regra, requisito ou comportamento esperado que permita sua caracterização.

## 8. Próxima etapa

A partir desta análise serão elaborados os cenários e casos de teste da funcionalidade de Cadastro.
