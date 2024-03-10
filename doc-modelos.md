# Documento de Modelos

Neste documento temos o modelo Conceitual (UML) ou de Dados (Entidade-Relacionamento). Temos também a descrição das entidades e o dicionário de dados.

Para a modelagem pode se usar o Astah UML ou o BrModelo. Uma ferramenta interessante para modelos UML é a [YUML](http://yuml.me), no link temos um exemplo de [Modelo UML com YUML](yuml/monitoria-yuml.md). Atualmente é possível usar a ferramenta **Mermaid** segundo o blog do GitHub [Include diagrams in your Markdown files with Mermaid](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/). A documentação do **Mermaid** pode ser encontrada em [Mermaid in GitHub](https://mermaid-js.github.io/mermaid).

## Modelo Conceitual

### Diagrama de Classes usando Mermaid

```mermaid
classDiagram
    Pessoa "1" *-- "1..*" Contato
    Pessoa "1" *-- "1" Endereco
    Pessoa "1" -- "*" PessoaFisica
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
```

### Descrição das Entidades

Descrição sucinta das entidades presentes no sistema.

| Entidade | Descrição   |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pessoa   | |
| Endereco | |
| Contato  | Entidade que representa um Contato tem as informações: Email, Telefone, +setEmail(char Email), +setTelefone(char Telefone), +getEmail(), +IncluirContato(cont Contato), +ExcluirContato(cont Contato),  +AlterarContato(cont Contato),+ConsultarContato(char Email, char Telefone), +ConsultarContato().|
| PessoaFisica | Entidade que representa uma Pessoa Fisica tem as informações: CPF, Pessoa, +setCNPJ(char CNPJ), +getCNPJ(), +ValidarCNPJ(char CNPJ), +IncluirPessoaFisica(PessoaFisica pessf), +ExcluirPessoaFisica(PessoaFisica pessf), +AlterarPessoaFisica(PessoaFisica pessf), +ConsultarPessoaFisica(char CPF, Pessoa pessoa), +ConsultarPessoaFisica().|

## Modelo de Dados (Entidade-Relacionamento)

Para criar modelos ER é possível usar o BrModelo e gerar uma imagem. Contudo, atualmente é possível criar modelos ER usando a ferramenta **Mermaid**, escrevendo o modelo diretamente em markdown. Acesse a documentação para escrever modelos [ER Diagram Mermaid](https://mermaid-js.github.io/mermaid/#/entityRelationshipDiagram).

```mermaid
erDiagram
    Departamento ||--o{ Laboratorio : labs
    Departamento ||--|{ Docente : docentes
    Docente ||--o| Laboratorio : coordenador
    Docente ||--o| Laboratorio : vice-coordenador
    Laboratorio ||--o{ Membro_Docente : membros
    Docente ||--|{ Membro_Docente : ""
    Laboratorio ||--o{ Membro_Discente : membros
    Membro_Discente }|--|| Discente: ""
```

### Dicionário de Dados

|   Tabela   | Laboratório |
| ---------- | ----------- |
| Descrição  | Armazena as informações de um laboratório acadêmico. |
| Observação | Laboratórios acadêmicos podem ser de Ensino, Pesquisa, Extensão, P&D, etc. |

|  Nome         | Descrição                        | Tipo de Dado | Tamanho | Restrições de Domínio |
| ------------- | -------------------------------- | ------------ | ------- | --------------------- |
| codigo        | identificador gerado pelo SGBD   | SERIAL       | ---     | PK / Identity |
| sigla         | representação em sigla do lab    | VARCHAR      | 15      | Unique / Not Null |
| nome          | nome do laboratório              | VARCHAR      | 150     | Not Null |
| descricao     | detalhes sobre o laboratório     | VARCHAR      | 250     | --- |
| endereco      | endereço e localização do lab    | VARCHAR      | 150     | --- |
| data_criacao  | data de criação do lab           | DATE         | ---     | Not Null |
| portaria      | portaria de criação do lab       | VARCHAR      | 50      | --- |
| link_portaria | URL para a portaria (PDF)        | VARCHAR      | 150     | --- |
| site          | URL para o site do laboratório   | VARCHAR      | 150     | --- |
| e-mail        | e-mail de contato do laboratório | VARCHAR      | 150     | --- |
| departamento  | departamento vinculado ao lab    | SERIAL       | ---     | FK / Not Null |
