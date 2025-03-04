# Plano de Teste

Este projeto tem como objetivo testar o fluxo do formulário de cadastro da Petlov, garantindo que suas funcionalidades essenciais estejam funcionando corretamente.

## 1. Introdução

O objetivo deste plano de teste é verificar se as funcionalidades do fluxo de cadastro da plataforma Petlov estão operando conforme o esperado.

- Fluxo de Autenticação: cadastros válidos, inválidos e mensagens de erro.

## 2. Escopo

- Tipos de testes a serem realizados: Testes funcionais.
- Fluxo de Autenticação: cadastros válidos, inválidos e mensagens de erro.

## 3. Ambientes e Ferramentas

- **Ferramentas utilizadas:**
    - Navegador Google Chrome - Versão 133.0.6943.127 (Versão oficial) 64 bits.
    - GitHub.

## 4. Casos de Teste

| ID  | Título | Pré-requisitos | Passo a Passo | Resultado Esperado |
| --- | --- | --- | --- | --- |
| 01  | Preenchimento de Formulário de Cadastro Válido | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente.<br>3. Clicar no botão "Cadastrar". | O sistema deve validar os dados e exibir uma mensagem de sucesso, como **"Você fez a diferença!"**. |
| 02  | Validação de Campos Obrigatórios | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Deixar todos os campos obrigatórios em branco.<br>3. Clicar no botão "Cadastrar". | O sistema deve exibir mensagens de erro informando que os campos são obrigatórios. |
| 03  | Validação do Campo Obrigatório "Nome do ponto de doação" | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente, exceto o campo "Nome do ponto de doação", que deve ficar em branco.<br>3. Clicar no botão "Cadastrar". | O sistema deve exibir uma mensagem de erro informando que o campo "Nome do ponto de doação" é obrigatório. |
| 04  | Validação do Campo Obrigatório "E-mail" | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente, exceto o campo "E-mail", que deve ficar em branco.<br>3. Clicar no botão "Cadastrar". | O sistema deve exibir uma mensagem de erro informando que o campo "E-mail" é obrigatório. |
| 05  | Validação do Campo "E-mail" com um e-mail inválido | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente, exceto o campo "E-mail", que deve ser preenchido com um e-mail inválido (ex: "matheus12345.com").<br>3. Clicar no botão "Cadastrar". | O sistema deve exibir uma mensagem de erro informando que o e-mail é inválido. |
| 06  | Validação do Campo Obrigatório "CEP" | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente, exceto o campo "CEP", que deve ficar em branco.<br>3. Clicar no botão "Cadastrar". | O sistema deve exibir uma mensagem de erro informando que o campo "CEP" é obrigatório. |
| 07  | Validação do Campo "CEP" com um número inválido | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente, exceto o campo "CEP", que deve ser preenchido com um valor inválido (ex: "1234567890").<br>3. Clicar no botão "Buscar CEP".<br>4. Clicar no botão "Cadastrar". | O sistema deve exibir uma mensagem de erro informando "Informe um CEP válido" e não deve permitir a conclusão do cadastro. |
| 08  | Validação do Campo Obrigatório "Número" | O usuário deve ter acesso à página do formulário | 1. Acessar a página do formulário.<br>2. Preencher todos os campos obrigatórios corretamente, exceto o campo "Número", que deve ficar em branco.<br>3. Clicar no botão "Cadastrar". | O sistema deve exibir uma mensagem de erro informando que o campo "Número" é obrigatório. |
| 09  | Validação dos Campos Rua, Bairro e Cidade/UF | O usuário deve inserir um CEP válido no campo correspondente | 1. Preencher o campo "CEP" com um valor válido.<br>2. Clicar no botão "Buscar CEP". | O sistema deve preencher automaticamente os campos "Rua", "Bairro" e "Cidade/UF" com as informações corretas. |

## 5. Critérios de Aceitação

- **Funcionalidade de Cadastro:**
    - O formulário deve validar todos os campos obrigatórios.
    - Mensagens de erro devem ser claras e informativas.
    - O sistema deve permitir apenas e-mails válidos.

## 6. Gerenciamento de Defeitos (Bugs)

| **Severidade** | **Descrição** |
| --- | --- |
| Crítico | Sistema inoperante ou falha de segurança. |
| Alto | Funcionalidade principal comprometida. |
| Médio | Funcionalidade secundária afetada. |
| Baixo | Problemas visuais ou melhorias. |

## 7. Riscos e Dependências

- **Riscos:** Ambiente inoperante, falhas na API que busca o CEP.
- **Dependência:** O site da Petlov deve estar no ar, funcionando corretamente.
