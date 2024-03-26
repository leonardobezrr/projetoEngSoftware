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
Breno    | HTML, CSS, Javascript, React, Next, Typescript, Prisma e Figma. |
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

### Gerenciar usuários

Requisito                                 | Descrição   | Ator |
---------                                 | ----------- | ---------- |
RF001 - Cadastrar usuários     |  Funcionalidade exclusiva do administrador do sistema onde o mesmo irá realizar o cadastro de usuários | Administrador |
RF002 - Excluir usuários     |  Funcionalidade exclusiva do administrador do sistema onde o mesmo irá realizar a exclusão dos usuários | Administrador |
RF003 - Editar usuários     |  Funcionalidade exclusiva do administrador do sistema onde o mesmo irá realizar a edição dos usuários | Administrador |
RF004 - Visualizar usuários     |  Funcionalidade exclusiva do administrador do sistema onde o mesmo poderá visualizar os usuários | Administrador |

### Gerenciar produtos

Requisito                                 | Descrição   | Ator |
---------                                 | ----------- | ---------- |
RF005 - Cadastrar produtos | Funcionalidade destinada ao funcionário do sistema possibilitando o cadastro de produtos no sistema | Funcianário |
RF006 - Excluir produtos | Funcionalidade destinada ao funcionário do sistema possibilitando a exclusão de produtos do sistema. | Funcianário |
RF007 - Editar produtos | Funcionalidade destinada ao funcionário do sistema possibilitando a editação de produtos do sistema. | Funcianário |
RF008 - Visualizar produtos | Funcionalidade destinada ao funcionário do sistema possibilitando a visualização de produtos do sistema | Funcianário |

### Gerenciar fornecedores

Requisito                                 | Descrição   | Ator |
---------                                 | ----------- | ---------- |
RF009 - Cadastrar fornecedores | Possibilidade de cadastrar fornecedores, guardando seus dados para futuras compras. | Administrador |
RF010 - Excluir fornecedores | Possibilidade de excluir fornecedores do sistema. | Administrador |
RF011 - Editar fornecedores | Possibilidade de editar fornecedores do sistema. | Administrador |
RF012 - Visualizar fornecedores | Possibilidade de visualizar fornecedores do sistema. | Administrador |

Requisito                                 | Descrição   | Ator |
---------                                 | ----------- | ---------- |
RF013 - Login | Funcionalidade realizada por outros usuários, para obter acesso ao sistema, recuperar senha e alterar informações dos usuários. | Administrador |
RF014 - Registrar Nota Fiscal Eletrônica |  Registrar a Nota Fiscal recebida pelo fornecedor no momento em que for realizada uma compra, contabilizando o item no estoque e, no momento em que houver a saída de algum item, debitando o item no estoque | Administrador |
RF015 - Gerar Log | O requisito funcional de número 14 é incluído, porém, são adicionados a ele os dados do gerenciamento de produtos e do registro de entradas, a fim de criar um arquivo mais amplo que o RF014, permitindo, assim, visualizar as informações a partir de um escopo geral, diferente do requisito citado anteriormente, que é focado apenas nas entradas.
RF016 - Registrar compra |  O funcionário irá informar o gerente da falta de algum material/produto, o qual irá realizar a compra do mesmo para reabastecimento do estoque, em seguida, caberá ao funcionário dar baixa dos itens no sistema. | Funcionário |


### Modelo Conceitual

Abaixo apresentamos o modelo conceitual usando o **YUML**.

 ```mermaid
classDiagram    
    Pessoa "1" *-- "1..*" Contato
    Pessoa "1" *-- "1" Endereco
    Pessoa "1" -- "*" PessoaJuridica
    Pessoa "1" -- "*" PessoaFisica
    PessoaFisica "" -- "" Saida
    PessoaJuridica "*" -- "1" Entradas
    Movimentacao "*" -- "1" Saida
    Movimentacao "*" -- "1" Entradas
    Movimentacao "*" -- "1" Produto
    Produto "*" -- "1" ItensNFE
    ItensNFE "*" -- "1" NFE
    NFE "1" -- "1" Entradas
    class Contato {
        -char Email
        -char Telefone
        +setEmail(char Email) void
        +setTelefone(char Telefone) void
        +getEmail() char
        +IncluirContato(cont Contato) void
        +ExcluirContato(cont Contato) void
        +AlterarContato(cont Contato) void
        +ConsultarContato(char Email, char Telefone) Contato
        +ConsultarContato() Contato
    }
    class Endereco {
        -char Rua
        -char Bairro
        -char Cidade
        -int CEP
        -char Estado
        -char EstadoSigla
        +atualizarEndereco() void
        +setRua(string Rua) void
        +setBairro(string Bairro) void
        +setCidade(string Cidade) void
        +setCEP(int CEP) void
        +setEstado(string Estado) void
        +setEstadoSigla(string Sigla) void
        +getRua() string
        +getBairro() string
        +getCidade() string
        +getCEP() int
        +getEstadoSigla() string
        +getEstado() string
        +IncluirEndereco(ende Endereco) void
        +ExcluirEndereco(ende Endereco) void
        +AlterarEndereco(ende Endereco) void
        +ConsultarEndereço(char Rua, int CEP, char EstadoSigla) Endereco
        +ConsultarEndereco() Endereco        
    }
    class Pessoa {
        -char Nome
        -Contato contato
        -bool Gerente
        -double Salario
        -char Login
        -char Senha
        -Endereco endereco
        +ValidarCPF(char CPF) bool
        +CriarLogin(bool Gerente, char Login, char Senha) void
        +ValidarLogin(char Login, char Senha) bool 
        +setNome(char Nome) void
        +setCPF(char CPF) void
        +setContato(Contato contato) void
        +setGerente(bool Gerente) void
        +setSalario(double Salario) void
        +setLogin(char Login) void
        +setSenha(char Senha) void
        +getNome() char
        +getCPF() char
        +getContato() Contato
        +getGerente() bool
        +getSalario() double
        +getLogin() char
        +getSenha() char
        +IncluirPessoa(Pessoa pess) void
        +ExcluirPessoa(Pessoa pess) void
        +AlterarPessoa(Pessoa pess) void
        +ConsultarPessoa(char Nome, char Login) Pessoa
        +ConsultarPessoa() Pessoa
    }
    class PessoaFisica {
        -char CPF
        -Pessoa Pessoa
        +setCNPJ(char CNPJ) void
        +getCNPJ() char
        +ValidarCNPJ(char CNPJ) bool
        +IncluirPessoaFisica(PessoaFisica pessf) void
        +ExcluirPessoaFisica(PessoaFisica pessf) void
        +AlterarPessoaFisica(PessoaFisica pessf) void
        +ConsultarPessoaFisica(char CPF, Pessoa pessoa) PessoaFisica
        +ConsultarPessoaFisica() PessoaFisica
    }
    class Produto {
        -char Nome
        -int CodigoBarras
        -PessoaJuridica Fornecedor
        +consultarProduto(int codigoBarras) void
        +setNome(char Nome) void
        +setCodigoBarras(int codigoBarras) void
        +getNome() char
        +getCodigoBarras() int
        +IncluirProduto(Produto prod) void 
        +ExcluirProduto(Produto prod) void
        +AlterarProduto(Produto prod) void
        +ConsultarProduto(char Nome, char CodigoBarras) Produto
        +ConsultarProduto() Produto
    }
    class PessoaJuridica {
        -char CNPJ
        -Pessoa Pessoa
        +setCNPJ(char CNPJ) void
        +getCNPJ() char
        +ValidarCNPJ(char CNPJ) bool
        +IncluirPessoaJuridica(PessoaJuridica pessf) void
        +ExcluirPessoaJuridica(PessoaJuridica pessf) void
        +AlterarPessoaJuridica(PessoaJuridica pessf) void
        +ConsultarPessoaJuridica(char CPF, Pessoa pessoa) PessoaJuridica
        +ConsultarPessoaJuridica() PessoaJuridica
    }
    class Movimentacao {
        -int ID
        -Produto Produtos
        -int Quantidade
        -float ValorTotal
        +setID(int ID) void
        +setData(char Data) void
        +setProdutos(Produto Produtos) void
        +setQuantidade(int Quantidade) void
        +setValorTotal(float Valor) void
        +getID() int
        +getData() char
        +getProdutos() Produto
        +getQuantidade() int
        +getValorTotal() float
        +calcularValorTotal() float
        +IncluirMovimentacao(Movimentacao movi) void
        +ExcluirMovimentacao(Movimentacao movi) void
        +AlterarMovimentacao(Movimentacao movi) void
        +ConsultarMovimentacao(int ID, Produto Produtos) Movimentacao
        +ConsultarMovimentacao() Movimentacao
    }
    class ItensNFE {
        -Produto Produtos
        -int Quantidade
        -float ValorUnitario
        -float ValorLote
        +setQuantidade(int Quantidade) void
        +setValorUnitario(float ValorUnitario) void
        +setValorLote(float ValorLote) void
        +getQuantidade() int
        +getValorUnitario() float
        +getValorLote() float
        +IncluirItensNFE(ItensNFE itensNFE) void
        +ExcluirItensNFE(ItensNFE itensNFE) void
        +AlterarItensNFE(ItensNFE itensNFE) void
        +ConsultarItensNFE(Produto Produtos) NFE
        +ConsultarItensNFE() ItensNFE
    }
    class NFE {
        -char NumeroNFE
        -char DataEmissao
        -float ValorTotal
        -Cliente Cliente
        -PessoaJuridica Vendedor
        -char FormaPagamento
        -char Status
        -ItensNFE ItensNFe
        +calcularValorTotal() void
        +calcularImpostos() void
        +gerarNumeroNFE() void
        +cancelarNFE() void
        +gerarPDF() void
        +enviarPorEmail() void
        +consultarStatus() void
        +emitirNFE() void
        +setNumeroNFE(char NumeroNFE) void
        +setDataEmissao(char DataEmissao) void
        +setValorTotal(char ValorTotal) void
        +setFormaPagamento(char FormaPagamento) void
        +setStatus(char Status) void
        +getNumeroNFE() char
        +getDataEmissao() char
        +getValorTotal() float
        +getFormaPagamento() char
        +getStatus() char
        +IncluirGerarNFE(NFE nfe) void
        +ExcluirGerarNFE(NFE nfe) void
        +AlterarGerarNFE(NFE nfe) void
        +ConsultarGerarNFE(char NumeroNFE, char DataEmissao, PessoaJuridica Vendedor) NFE
        +ConsultarGerarNFE() NFE
    }
    class Saida {
        -PessoaFisica DestinoCliente
        -char Data
        +setdestinoCliente(Cliente cliente) void
        +getdestinoCliente() cliente
        +retiradaProdutos() void
        +gerarLog() void
        +incluirSaida(Saida saida) void
        +consultarSaida(char Nome) void
        +listarSaidas() ArraySaida
        +IncluirSaida(Saida saida) void
        +ExcluirSaida(Saida saida) void
        +AlterarSaida(Saida saida) void
        +ConsultarSaida(char Data, PessoaFisica DestinoCliente) Saida
        +ConsultarSaida() Saida
    }
    class Entradas {
        -PessoaJuridica OrigemFornecedor
        -char Data
        +setOrigemFornecedor(PessoaJuridica fornecedor) void
        +getOrigemFornecedor() PessoaJuridica
        +receberProdutos() void
        +gerarLog() void
        +incluirEntrada(Entrada entrada) void
        +consultarEntrada(char Nome) Entrada
        +listarEntradas() ArrayEntradas
        +IncluirEntradas(Entrada entr) void
        +ExcluirEntradas(Entrada entr) void
        +AlterarEntradas(Entrada entr) void
        +ConsultarEntradas(char Data, PessoaJuridica OrigemFornecedor) Entradas
        +ConsultarEntradas() Entradas
    }
```

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
19/03/2024 | Não aprendizado das ferramentas utilizadas pelos componentes do grupo | Alta | Gerente | Vigente | Reforçar estudos sobre as ferramentas e aulas com a integrante que conhece a ferramenta |
19/03/2024 |Máquinas incapazes de fornecer os recursos necessários para o funcionamento do sistema | Média | Todos | Vigente | Recomendar a compra de novos dispositivos capazes de fornecer os recursos necessários para o funcionamento pleno do sistema. |
19/03/2024 | Divisão de tarefas mal sucedida | Baixa | Gerente | Vigente | Acompanhar de perto o desenvolvimento de cada membro da equipe |
19/03/2024 | Implementação de protótipo com as tecnologias | Alto | Todos | Resolvido | Encontrar tutorial com a maioria da tecnologia e implementar um caso base do sistema |
19/03/2024 | Atrasos no cronograma | Média | Todos | Em Processo | Este risco pode ser causado por uma série de fatores, como a falta de recursos, a falta de planejamento ou a falta de comunicação entre os membros da equipe. Para mitigar este risco, é importante ter um cronograma realista e flexível, e garantir que todos os membros da equipe estejam alinhados com os objetivos do projeto.|
19/03/2024 | Risco de qualidade do produto | Alto | Todos | Em Processo | Este risco pode ser causado por uma série de fatores, como a falta de atenção aos detalhes ou a falta de testes adequados. Para mitigar este risco, é importante ter uma equipe experiente, garantir que os membros da equipe estejam focados na qualidade do produto e realizar testes rigorosos. |
19/03/2024 | Insatisfação do cliente | Alto | Todos | Em Processo | Este risco pode ser causado por uma série de fatores, como a falta de comunicação com o cliente, a entrega de um produto que não atende às expectativas do cliente ou a falta de suporte pós-venda. Para mitigar este risco, é importante manter uma comunicação aberta com o cliente, garantir que o produto atenda às expectativas do cliente e oferecer um bom suporte pós-venda. |

### Referências
