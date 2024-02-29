# Documento de Visão

Documento construído a partido do **Modelo BSI - Doc 001 - Documento de Visão** que pode ser encontrado no
link: https://docs.google.com/document/d/1LD2UdvKGtWbAQlUB5AsO4twpdm0RM9nq7wqs_CvkjOc/edit

## Equipe e Definição de Papéis

Membro     |     Papel   |   E-mail   |
---------  | ----------- | ---------- |
Breno    | Desenvolvedor  | breno.porfirio.079@ufrn.edu.br
Leonardo     | Cliente | Leonardobezerra05@gmail.com
Ricardo         | Desenvolvedor  | ricardo.alencar.122@ufrn.edu.br
Luís      | Gerente | Luisf311220@gmail.com
Gabriel      | Desenvolvedor | gabriel.lima.112@ufrn.edu.br
Charles      | Desenvolvedor | charleseduardofaria@gmail.com

### Matriz de Competências

Membro     |     Competências   |
---------  | ----------- |
Breno    | Python , C, HTML, CSS e Javascript, React, Next, Typescript e Figma. |
Leonardo     | HTML, CSS, JavaScript, React, Next, Golang, PostgreSQL, Python. |
Ricardo        | HTML, CSS, JavaScript, React, Golang, MySQL, PostgreSQL, PHP, WordPress, curso ténico em informática. |
Luís       | HTML, CSS, Javascript , C, C++, QT creator, QT designer. |
Gabriel       | HTML, CSS, JavaScript, React, Next, Vue.js, UI/UX design, Figma, MariaDB, python, C, Angular, TypeScript. |
Charles      | Java, Spring Boot, Laravel, HTML, CSS, JQuery, Postgres, MySQL, Figma, Modelagem de Dados |


## Perfis dos Usuários

O sistema poderá ser utilizado por diversos usuários. Temos os seguintes perfis/atores:

Perfil                                 | Descrição   |
---------                              | ----------- |
Gerente | Este usuário utiliza o sistema para gerenciar usuários. Fazer cadastro, exclusão, edição e visualização de usuários. Compra de produtos.
Funcionário | Este usuário utiliza o sistema para gerenciar produtos. Fazer cadastro, exclusão, edição, visualização dos produtos no sistema e pesquisa. Receber produtos e dar baixa no sistema nas entradas e saídas. Cadastrar fornecedores.

## Lista de Requisitos Funcionais

Requisito                                 | Descrição   | Ator |
---------                                 | ----------- | ---------- |
RF001 - Gerenciar usuários     |  Funcionalidade exclusiva do administrador do sistema. Fazer cadastro, exclusão, edição e visualização de usuários. | Administrador |
RF002 - Gerenciar produtos | Funcionalidade destinada ao funcionário do sistema. Fazer cadastro, exclusão, edição, visualização dos produtos no sistema e pesquisa. | Administrador |
RF003 - Login | Funcionalidade realizada por outros usuários, para obter acesso ao sistema, recuperar senha e alterar informações dos usuários. | Administrador |
RF004 - Registrar Nota Fiscal Eletrônica de entrada |  Registrar a Nota Fiscal recebida pelo fornecedor no momento que for realizada uma compra, contabilizando o item no estoque. | Administrador |
RF005 - Gerar Nota Fiscal Eletrônica de Saída |  Registrar a Nota Fiscal no momento que houver a saída de algum item, debitando o item no estoque. | Administrador |
RF006 - Gerenciar Fornecedores | Possibilidade de cadastrar fornecedores, guardando seus dados para futuras compras. | Administrador |
RF007 - Gerar Log | Inclui o Requisito Funcional de número 5, mas adiciona a ele os dados do gerenciamento de produtos e do registro de entradas, a fim de criar um arquivo mais amplo que o RF005, assim, permitindo ver as coisas a parti de um escopo geral, diferente que requisito citado anteriormente, que é focado nas somente nas entradas.
 | Chefes e Coordenadores |
RF008 - Registrar compra |  o gerente será informado da falta de algum material/produto, e poderá realizar a compra do mesmo para reabastecimento do estoque, logo em seguida o caberá ao funcionário dar baixa na entrada do itens no sistema. | Administrador |

### Modelo Conceitual

Abaixo apresentamos o modelo conceitual usando o **YUML**.

 ![Modelo UML](yuml/monitoria-modelo.png)

O código que gera o diagrama está [Aqui!](yuml/monitoria-yuml.md). O detalhamento dos modelos conceitual e de dados do projeto estão no [Documento de Modelos](doc-modelos.md).

#### Descrição das Entidades

## Lista de Requisitos Não-Funcionais

Requisito                                 | Descrição   |
---------                                 | ----------- |
RNF001 - Disponibilidade | Utilização do módulo de informações cadastrais em modo offline. |
RNF002 - Segurança |  Encripta os dados e informações para que apenas aqueles logados no sistema possam visualizá-los |
DEP001 - Sistema de vendas | Existe a necessidade de que haja um sistema de vendas, para que suas notas sirvam de entrada para o sistema de estoque. |
DEP002 - Sistema de apoio a decisão |  Existe a necessidade de que haja um sistema de apoio a decisão, para que possa converter os dados do Gerar Log em um dashboard |

## Riscos

Tabela com o mapeamento dos riscos do projeto, as possíveis soluções e os responsáveis.

Data | Risco | Prioridade | Responsável | Status | Providência/Solução |
------ | ------ | ------ | ------ | ------ | ------ |
04/12/2023 | Não aprendizado das ferramentas utilizadas pelos componentes do grupo | Alta | Gerente | Vigente | Reforçar estudos sobre as ferramentas e aulas com a integrante que conhece a ferramenta |
04/12/2023 |Máquinas incapazes de fornecer os recursos necessários para o funcionamento do sistema | Média | Todos | Vigente | Recomendar a compra de novos dispositivos capazes de fornecer os recursos necessários para o funcionamento pleno do sistema. |
10/03/2018 | Divisão de tarefas mal sucedida | Baixa | Gerente | Vigente | Acompanhar de perto o desenvolvimento de cada membro da equipe |
10/03/2018 | Implementação de protótipo com as tecnologias | Alto | Todos | Resolvido | Encontrar tutorial com a maioria da tecnologia e implementar um caso base do sistema |

### Referências
