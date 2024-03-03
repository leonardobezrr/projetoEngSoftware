
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
| **Código**     | **Descrição** |
| **TA01.01** |  |

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
| **Código**     | **Descrição** |
| **TA01.01** |  |

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
| **Código**     | **Descrição** |
| **TA01.01** |  |

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
| **Código**     | **Descrição** |
| **TA01.01** |  |

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
| **Código**     | **Descrição** |
| **TA01.01** |  |

### User Story US06 - Registrar entradas

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Faz um registro de todas as vezes que entra alguma mercadoria no sistema. As informações constantes neste registro são: data, nome do produto e CNPJ do fornecedor |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF04          | Registrar Nota Fiscal Eletrônica de entrada  |


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
| **Código**     | **Descrição** |
| **TA01.01** |  |

### User Story US07 - Registrar saídas (venda)

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Responsável por realizar as saídas/vendas de mercadorias, logo em seguida será feito um registro das mesmas. As informações constantes neste registro são: data, nome do produto e CNPJ do fornecedor |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF05          | Gerar Nota Fiscal Eletrônica de Saída  |


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
| **Código**     | **Descrição** |
| **TA01.01** |  |

### User Story US08 - Registrar Compras

|               |                                                                |
| ------------- | :------------------------------------------------------------- |
| **Descrição** | Responsável por registrar todas as compras feitas pelo gerente e após a confirmação de recebimento dos itens, o funcionário dará entrada dos mesmos no sistema. As informações constantes neste registro são: data, nome do produto e CNPJ do fornecedor, preço e quantidade |

| **Requisitos envolvidos** |                                                    |
| ------------- | :------------------------------------------------------------- |
| RF05          | Gerar Nota Fiscal Eletrônica de Saída  |


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
| **Código**     | **Descrição** |
| **TA01.01** |  |
