
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
| RF01          | Gerenciar usuários |

|                           |                                     |
| ------------------------- | ----------------------------------- | 
| **Prioridade**            | Essencial                           | 
| **Estimativa**            | 5 h                                 | 
| **Tempo Gasto (real):**   | 2 h                                 | 
| **Tamanho Funcional**     | 8 PF                                | 
| **Analista**              | -                             | 
| **Desenvolvedor**         | Gabriel, Breno e Ricardo                                  | 
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

### User Story US02 - Gerenciar produto

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Esse processo é responsável por fazer cadastro, exclusão, edição e visualização dos produtos cadastrados no sistema. As informações constantes neste cadastro são: Nome, código de barras e o CNPJ do fornecedor |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF02          | Gerenciar produto  |

|                           |                                     |
| ------------------------- | ----------------------------------- | 
| **Prioridade**            | Essencial                           | 
| **Estimativa**            | 8 h                                 | 
| **Tempo Gasto (real):**   | 10 h                                | 
| **Tamanho Funcional**     | 7 PF                                | 
| **Analista**              | -                             | 
| **Desenvolvedor**         | Gabriel, Breno e Ricardo                                  | 
| **Revisor**               | -                               | 
| **Testador**              | -                                | 



| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA02.01** | O funcionário solicita uma amostra do produto para pode pegar suas informações|
| **TA02.01** | O funcionário recebe o produto  |
| **TA02.01** | O funcionário acessa o sistema com sua conta (include Login)|
| **TA02.01** | O funcionário preenche o cadastro com as informações descritas no produto|
| **TA02.01** | O funcionário conclui o cadastro e salva as informações (extend Gerar Log) |
| **TA02.01** | O sistema exibe uma mensagem de “Cadastro realizada com sucesso”|

--------------------------------------------------------------------------------------
| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA02.02** | O funcionário informa ao sistema o código de barras do produtor no sistema (include Login)|
| **TA02.02** | O sistema exibe na tela todas as informações do fornecedor |
-------------------------------------------------------------------------------------

| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA02.03** | O funcionário consulta o cadastro do produto no sistema (include Login)|
| **TA02.03** | O funcionário clica na opção excluir cadastro |
| **TA02.03** | O sistema abre uma caixa de confirmação perguntando se o funcionário realmente deseja excluir o produto|
| **TA02.03** | O funcionário escolhe a opção “SIM”|
| **TA02.03** | O sistema exclui o produto e as alterações são salvas no sistema (extend Gerar Log)|
| **TA02.03** | O sistema exibe uma mensagem de “Exclusão realizada com sucesso” |
------------------------------------------------------------------------------------

| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**  | **Descrição** |
| **TA02.04** | O funcionário recebe a informação que um cadastro está com problema|
| **TA02.04** | O funcionário solicita uma amostra do produto para que possa pegar os dados corretos |
| **TA02.04** | O funcionário localiza o cadastro do produto no sistema (include Login) |
| **TA02.04** | O funcionário altera as informações e salva no sistema. (extend Gerar Log) |
| **TA02.04** | O sistema exibe uma mensagem de “Alteração realizada com sucesso”|

### User Story US03 - Gerenciar fornecedor

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Esse processo é responsável por fazer cadastro, exclusão, edição e visualização dos fornecedores cadastrados no sistema. As informações constantes neste cadastro são: Razão social, nome fantasia, CNPJ, endereço, telefone e e-mail |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF06         | Gerenciar Fornecedores |


|                           |                                     |
| ------------------------- | ----------------------------------- | 
| **Prioridade**            | Essencial                           | 
| **Estimativa**            | 8 h                                 | 
| **Tempo Gasto (real):**   | 10 h                                | 
| **Tamanho Funcional**     | 7 PF                                | 
| **Analista**              | -                             | 
| **Desenvolvedor**         | Gabriel, Breno e Ricardo                                  | 
| **Revisor**               | -                               | 
| **Testador**              | -                                | 



| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA03.01** | O funcionário solicita os documentos e informações necessárias diretamente ao fornecedor |
| **TA03.01** | O fornecedor manda os documentos e o funcionário os recebe |
| **TA03.01** | O funcionário acessa o sistema com sua conta (include Login)|
| **TA03.01** | O funcionário preenche o cadastro com as informações recebidas |
| **TA03.01** | O funcionário conclui o cadastro e salva as informações (extend Gerar Log) |
| **TA03.01** | O sistema exibe uma mensagem de “Cadastro realizado com sucesso” |

--------------------------------------------------------------------------------------
| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA03.02** | O funcionário informa ao sistema o CNPJ do fornecedor no sistema (include Login) |
| **TA03.02** | O sistema exibe na tela todas as informações do fornecedor |
-------------------------------------------------------------------------------------

| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA03.03** | O funcionário consulta o cadastro do fornecedor no sistema (include Login) |
| **TA03.03** | O funcionário clica na opção excluir cadastro |
| **TA03.03** | O sistema abre uma caixa de confirmação perguntando se o funcionário realmente deseja excluir o fornecedor |
| **TA03.03** | O funcionário escolhe a opção “SIM” |
| **TA03.03** | O sistema exclui o fornecedor e as alterações são salvas no sistema (extend Gerar Log) |
| **TA03.03** | O sistema exibe uma mensagem de “Exclusão realizada com sucesso” |
------------------------------------------------------------------------------------

| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA03.04** | O fornecedor solicita que o seu cadastro seja atualizado |
| **TA03.04** | O funcionário solicita ao fornecedor as informações necessárias para atualização |
| **TA03.04** | O funcionário localiza o cadastro do fornecedor no sistema (include Login) |
| **TA03.04** | O funcionário altera as informações e salva no sistema. (extend Gerar Log) |
| **TA03.04** | O sistema exibe uma mensagem de “Alteração realizada com sucesso” |

### User Story US04 - Gerar log

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Este caso de uso é capaz de gerar um histórico de todas as informações encontradas nos arquivos gerados pelos casos de uso Gerenciar Fornecedores, Gerenciar Produtos e Registrar Entradas. As informações constantes neste relatório são: Data, mudanças realizadas no Gerenciar Produtos, mudanças no Gerenciar Fornecedores e Registrar Entradas |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF02          | Gerenciar produtos  |
| RF04          | Registrar Nota Fiscal Eletrônica de entrada |
| RF05          | Gerar Nota Fiscal Eletrônica de Saída |
| RF06          | Gerenciar Fornecedores |
| RF07          | Gerar Log |

|                           |                                     |
| ------------------------- | ----------------------------------- | 
| **Prioridade**            | Essencial                           | 
| **Estimativa**            | 8 h                                 | 
| **Tempo Gasto (real):**   | 10 h                                | 
| **Tamanho Funcional**     | 7 PF                                | 
| **Analista**              | -                             | 
| **Desenvolvedor**         | Gabriel, Breno e Ricardo                                  | 
| **Revisor**               | -                               | 
| **Testador**              | -                                | 



| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA04.01** | O funcionário solicitará que o Gerar Log gere um arquivo para verificação. |
| **TA04.01** | O Gerar Log então pegará o arquivo gerado pelo caso de uso Gerenciar Fornecedores, Gerenciar Produtos e Registrar Entradas, e os justará em um único arquivo. |
| **TA04.01** | O Gerar Log então retornará um arquivo para o funcionário com as informações geradas. |

### User Story US05 - Login

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Permite que funcionários e gerentes acessem o sistema para fazer qualquer tipo de alteração que for necessária. As informações constantes são login e senha |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF01          | Gerenciar usuários  |
| RF02          | Gerenciar produtos |
| RF03          | Login |

|                           |                                     |
| ------------------------- | ----------------------------------- | 
| **Prioridade**            | Essencial                           | 
| **Estimativa**            | 8 h                                 | 
| **Tempo Gasto (real):**   | 10 h                                | 
| **Tamanho Funcional**     | 7 PF                                | 
| **Analista**              | -                             | 
| **Desenvolvedor**         | Gabriel, Breno e Ricardo                                  | 
| **Revisor**               | -                               | 
| **Testador**              | -                                | 



| Testes de Aceitação (TA) |  |
| ----------- | --------- |
| **Código**      | **Descrição** |
| **TA05.01** | Ao entrar no sistema o usuário será referido a uma tela de login, contendo dois campos: Login e Senha |
| **TA05.01** | O usuário coloca seu Login e Senha |
| **TA05.01** | O sistema exibe uma mensagem de “Login realizado com sucesso”, enquanto o sistema carrega |
| **TA05.01** | O usuário agora pode interagir com o sistema |
