# Desenvolvimento de uma Tela de Login - Documento do Projeto

## Plano de Fluxo de Trabalho

### Desenvolvimento da Tela de Login

1. **Análise de Requisitos**:
   - Compreender os requisitos da tela de login.
   - Identificar os campos necessários (por exemplo, nome de usuário e senha).

2. **Design e UI**:
   - Criar um layout atraente para a tela de login.
   - Certificar-se de que os campos e botões estejam dispostos de forma clara.

3. **Implementação**:
   - Desenvolver a funcionalidade de login.
   - Validar as entradas do usuário.
   - Integrar com o sistema de autenticação.

4. **Testes**:
   - Realizar testes de unidade e integração.
   - Verificar se o login e a autenticação funcionam corretamente.

5. **Documentação**:
   - Documentar o código e o processo de desenvolvimento.

### Ciclo de Vida de um Bug

1. **Relato do Bug**:
   - O usuário ou testador encontra um bug e o relata no sistema de rastreamento de problemas.

2. **Priorização**:
   - A equipe avalia a gravidade e a prioridade do bug.

3. **Reprodução**:
   - Os desenvolvedores tentam reproduzir o bug em seu ambiente de desenvolvimento.

4. **Correção**:
   - A equipe de desenvolvimento corrige o bug.

5. **Testes de Regressão**:
   - Os testadores verificam se a correção não afetou outras partes do sistema.

6. **Validação**:
   - O testador valida se o bug foi realmente corrigido.

## User Stories

### User Story 1: Como um usuário, quero fazer login na minha conta.

**Mind Map**:
![Mind Map - User Story 1](link-para-imagem-mind-map1.png)

**Casos de Teste usando Step-by-Step**:
1. Abra a tela de login.
2. Insira um nome de usuário válido.
3. Insira uma senha válida.
4. Clique no botão de login.
5. Verifique se a tela de destino após o login é exibida.

**Casos de Teste usando BDD**:
```gherkin
Funcionalidade: Login de Usuário

  Cenário: Login com sucesso
    Dado que o usuário está na tela de login
    Quando ele insere suas credenciais corretas
    E clica no botão de login
    Então ele deve ser redirecionado para sua página principal

  Cenário: Login com falha
    Dado que o usuário está na tela de login
    Quando ele insere credenciais inválidas
    E clica no botão de login
    Então ele deve ver uma mensagem de erro


# Fluxograma da Tela de Login

```mermaid
graph TD
A[Tela de Login] --> B[Usuário insere Nome de Usuário]
B --> C[Usuário insere Senha]
C --> D[Usuário clica em "Logar"]
D --> E{Validação}

E --> |Senha vazia| F[Exibir mensagem de erro: Insira a Senha]
E --> |Nome de Usuário vazio| G[Exibir mensagem de erro: Insira o Nome de Usuário]

## Cenário 1: Usuário Inserindo Apenas a Senha

```mermaid
graph TD
A[Tela de Login] --> B[Usuário insere Nome de Usuário]
B --> C[Usuário insere Senha]
C --> D[Usuário clica em "Logar"]

D --> |Validação|
D --> |Senha vazia| E[Exibir mensagem de erro: Insira a Senha]
E --> F[Fim]


graph TD
A[Tela de Login] --> B[Usuário insere Nome de Usuário]
B --> C[Usuário insere Senha]
C --> D[Usuário clica em "Logar"]

D --> |Validação|
D --> |Nome de Usuário vazio| E[Exibir mensagens de erro: Insira o Nome de Usuário]
E --> F[Fim]




