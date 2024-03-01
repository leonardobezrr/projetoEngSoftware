
# Documento Lista de User Stories

Documento construído a partido do **Modelo BSI - Doc 004 - Lista de User Stories** que pode ser encontrado no
link: https://docs.google.com/document/d/15KgOK44Be65ad9GpLHBKG5SfhE8z3pzZD6Pqz2Wzu9g/edit
## Descrição

Este documento descreve os User Stories criados a partir da Lista de Requisitos no [Documento 001 - Documento de Visão](doc-visao.md). Este documento também pode ser adaptado para descrever Casos de Uso. Modelo de documento baseado nas características do processo easYProcess (YP).

## Histórico de revisões

| Data       | Versão  | Descrição                          | Autor                          |
| :--------- | :-----: | :--------------------------------: | :----------------------------- |
| 05/12/2023 | 1.0  | Documento inicial  | Todos |
| ...        | ...     | ...                                | ...     |
|  |    | Documento completo com o detalhamento de todos os User Stories |      |
|  |    | Adição das informações da equipe: Analista, Desenvolvedor, Revisor e Testador. |  |



### User Story US01 - Gerenciar usuários

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Esse processo é responsável por fazer cadastro, exclusão, edição e visualização dos funcionários cadastrados no sistema. As informações constantes neste cadastro são: nome, data de nascimento, endereço, telefone, CPF e RG. |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF01          | Cadastrar Usuário |
| RF02          | Alterar Usuário  |
| RF03          | Consultar Usuários        |
| RF04          | Excluir Usuário |
| RF05          | Vizualizar detalhes do Usuário |

|                           |                                     |
| ------------------------- | ----------------------------------- | 
| **Prioridade**            | Essencial                           | 
| **Estimativa**            | 8 h                                 | 
| **Tempo Gasto (real):**   |                                     | 
| **Tamanho Funcional**     | 7 PF                                | 
| **Analista**              | -                             | 
| **Desenvolvedor**         | -                                  | 
| **Revisor**               | -                               | 
| **Testador**              | -                                | 



| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA01.01** |  O gerente solicita ao RH os documentos do funcionário|
| **TA01.01** | O RH manda os documentos e o gerente os recebe |
| **TA01.01** | O gerente acessa o sistema com sua conta administrador (include Login)|
| **TA01.01** | O gerente preenche o cadastro com as informações recebidas|
| **TA01.01** | O gerente instrui o funcionário a escolher uma senha para seu Login|
| **TA01.01** | O gerente conclui o cadastro e salva as informações |
| **TA01.01** | O sistema exibe uma mensagem de “Cadastro realizada com sucesso”|

--------------------------------------------------------------------------------------
| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA01.02** | O gerente informa ao sistema o CPF do funcionário no sistema (include Login)|
| **TA01.02** | O sistema exibe na tela todas as informações do funcionário |
-------------------------------------------------------------------------------------

| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA01.03** | O gerente consulta o cadastro do funcionário no sistema (include Login)|
| **TA01.03** | O gerente clica na opção excluir cadastro |
| **TA01.03** | O sistema abre uma caixa de confirmação perguntando se o gerente realmente deseja excluir o funcionário|
| **TA01.03** | O gerente escolhe a opção “SIM”|
| **TA01.03** | O sistema exclui o funcionário e as alterações são salvas no sistema|
| **TA01.03** | O sistema exibe uma mensagem de “Exclusão realizada com sucesso” |
------------------------------------------------------------------------------------

| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**  | **Descrição** |
| **TA01.04** | O RH solicita que o cadastro do funcionário seja atualizado|
| **TA01.04** | O gerente solicita ao RH as informações necessárias para atualização |
| **TA01.04** | O gerente localiza o cadastro do funcionário no sistema (include Login) |
| **TA01.04** | O gerente altera as informações e salva no sistema|
| **TA01.04** | O sistema exibe uma mensagem de “Alteração realizada com sucesso” |
