# Food Truck - Administração

Aplicação desktop para administração de um food truck, desenvolvida com JavaFX, Hibernate/JPA e SQLite. O sistema permite cadastrar o cardápio, montar pedidos e consultar os pedidos finalizados.

## Funcionalidades

- Cadastro, edição e exclusão de categorias.
- Cadastro, edição e exclusão de produtos.
- Associação de produtos a categorias e complementos.
- Cadastro, edição e exclusão de complementos com preço adicional.
- Pesquisa de produtos por nome.
- Montagem de pedidos com quantidade e complementos.
- Cálculo automático do preço unitário e do total do pedido.
- Finalização e consulta dos pedidos realizados.
- Visualização dos itens de cada pedido salvo.

## Tecnologias

- Java 11
- JavaFX 13
- Maven
- Hibernate ORM 7
- Jakarta Persistence (JPA)
- SQLite

## Pré-requisitos

- JDK 11 ou superior
- Maven 3.6 ou superior

Confira as versões instaladas:

```bash
java -version
mvn -version
```

## Como executar

Clone o repositório e entre na pasta do projeto:

```bash
git clone https://github.com/PietroSoaresss/foodtruck_app.git
cd foodtruck_app
```

Execute a aplicação com Maven:

```bash
mvn clean javafx:run
```

Também é possível abrir o projeto em uma IDE compatível com Maven e executar a classe principal:

```text
ifrs.ibiruba.exemplo_bd.App
```

## Banco de dados

O banco SQLite é criado automaticamente no arquivo `meu_banco.sqlite`, na raiz do projeto, na primeira execução. O Hibernate utiliza `hibernate.hbm2ddl.auto=update` para atualizar a estrutura das tabelas conforme as entidades da aplicação.

Para começar com um banco vazio, encerre a aplicação e remova o arquivo `meu_banco.sqlite` antes de executá-la novamente.

## Estrutura do projeto

```text
src/main/java/ifrs/ibiruba/exemplo_bd/
├── App.java                  # Inicialização da aplicação JavaFX
├── controller/               # Controladores das telas
├── model/                    # Entidades JPA
├── persistencia/             # Configuração do EntityManager
└── repository/               # Operações de persistência

src/main/resources/
├── META-INF/persistence.xml  # Configuração do Hibernate e SQLite
└── ifrs/ibiruba/exemplo_bd/
    ├── *.fxml                # Interfaces das telas
    └── estilos.css           # Estilos da aplicação
```

## Telas principais

A aplicação possui quatro abas:

1. **Categorias** — gerenciamento das categorias do cardápio.
2. **Produtos** — gerenciamento de produtos, preços, descrições, categorias e complementos.
3. **Complementos** — gerenciamento dos adicionais e seus preços.
4. **Pedidos** — criação, finalização e consulta de pedidos.

## Licença

Este projeto não possui uma licença definida no momento.
