# Desafio Frontend

Para esse desafio, sesrá avaliado os conhcimentos para resolução dos problemas, a organização dos códigos, organização do projeto. Após a conclusão deste, enviar o projeto para a equipe de recrutamento para avaliação do código.

Deve-se ter um commit para cada recursos implementado e se fazer uso das tags para controle de versão.

## Requisitos do projeto

### Tecnologias

Para esse projeto é indispensável a utilização das tecnologias abaixo, vamos estar avaliando a forma como é aplicado o conhecimento em cada uma delas para solução dos casos de uso.

1. Next - react
2. Zod
3. React-Hook-Forms
4. React-Query
5. Material-UI
7. Typescript
8. Zustand

### Conceitos

Esses são conceitos desejáveis e não obrigatórios.

1. SOLID
2. Clean Archtecture


## Gestão de Profissionais

```
COMO: um adminstrador do sistema,
QUERO: poder registrar, atualizar e listar profissionais,
PARA: que eu possa gerenciar quem pode oferecer serviços através da plataforma
```

## Contexto Geral

```
DADO: que estou autenticado como administrador
```

### Cenário: Registrar um novo profissional

```
DADOS: que nenhum profissional está atualmente registrado com o email "joao@exemplo.com"
QUANDO: eu registro um profissional com os seguintes detalhes:
| nome | email | qualificações |
| João Silva | joao@exemplo.com | Dentista, MSc |
ENTÃO: um novo profissional deve ser criado
E: ele deve estar associado às qualificações "Dentista" e "MSc"
```

### Cenário: Atualizar qualificações de um profissional

```
DADO: que o profissional "Carlos Mendes" está registrado com a qualificação "Pediatra"
QUANDO: eu atualizo as qualificações de Carlos para "Pediatra, PhD em Medicina"
ENTÃO: as qualificações de Carlos no sistema devem ser "Pediatra, PhD em Medicina"
```

### Cenário: Listar profissionais

```
QUANDO: eu solicito a lista de todos os profissionais
ENTÃO: eu devo receber uma lista contendo todos os profissionais registrados
E: cada profissional deve ter detalhes de suas qualificações associadas
```

# Caso de uso 1: Registrar Profissional

```
ID: UC01
Ator Principal: Administrador
```
## Pré condições

1. O usuário deve estar autenticado e autorizado como administrador.

## Fluxo Principal

1. O administrador acessa a página de registro de profissionais.
2. O administrador preenche o formulário com nome, email e qualificações do profissional.
3. O sistema valida os dados para garantir que não há registros duplicados.
4. O sistema registra o profissional no banco de dados.
5. O sistema exibe uma mensagem de sucesso ao administrador.

## Fluxo Alternativo: Registro duplicado

1. No passo 3 do fluxo principal, se o email já estiver registrado, o sistema interrompe o fluxo principal.
2. O sistema exibe uma mensagem de erro indicando que o email já está em uso.

## Pós condições

1. Um novo profissional é adicionado ao sistema, ou uma mensagem de erro é exibida.

# Caso de uso 2: Atualizar Qualificações do Profissional

```
ID: UC02
Ator Principal: Administrador
```

## Pré condições

1. O usuário deve estar autenticado e autorizado como administrador.

## Fluxo Principal

1. O administrador acessa a lista de profissionais.
2. O administrador seleciona um profissional para atualizar.
3. O administrador altera as qualificações do profissional no formulário de edição.
4. O sistema valida as alterações.
5. O sistema atualiza as informações do profissional no banco de  dados.
6. O sistema exibe uma mensagem de sucesso ao administrador.

## Pós condições

1. As qualificações do profissional são atualizadas no sistema.

# Caso de uso 1: Listar Profissional

```
ID: UC03
Ator Principal: Administrador
```
## Pré condições

1. O usuário deve estar autenticado e autorizado como administrador.

## Fluxo Principal

1. O administrador acessa a página de listagem de profissionais.
2. O sistema recupera todos os profissionais do banco de dados.
3. O sistema exibe os profissionais com seus detalhes, incluindo qualificações.

## Pós condições

1. Os profissionais são listados para o administrador.
