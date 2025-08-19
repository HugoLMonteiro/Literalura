# Literalura
O LiterAlura é uma aplicação de linha de comando desenvolvida em Java com Spring Boot, projetada para interagir com a API Gutendex e gerenciar um catálogo de livros e autores. 
A aplicação permite buscar livros por título, listar livros e autores registrados no banco de dados, e filtrar autores e livros com base em critérios como ano de nascimento, ano de falecimento e idioma.

# Funcionalidades
A aplicação oferece as seguintes funcionalidades por meio de um menu interativo:
Buscar livros pelo título: Busca e armazena livros do catálogo Gutendex no banco de dados local.
Listar livros registrados: Exibe todos os livros que foram salvos no banco de dados local.
Listar autores registrados: Exibe todos os autores de livros que foram salvos no banco de dados.
Listar autores vivos em um determinado ano: Filtra e lista autores que estavam vivos no ano especificado.
Listar autores nascidos em determinado ano: Lista autores que nasceram no ano especificado.
Listar autores por ano de sua morte: Filtra e lista autores que faleceram no ano especificado.
Listar livros em um determinado idioma: Exibe livros cadastrados no banco de dados de acordo com o idioma selecionado.

# Tecnologias Utilizadas
Java: Linguagem de programação.
Spring Boot: Framework para simplificar o desenvolvimento de aplicações Java.
Spring Data JPA: Para a persistência de dados e interação com o banco de dados.
Hibernate: Implementação da especificação JPA.
PostgreSQL: Banco de dados relacional.
Jackson: Para serialização e desserialização de JSON.
API Gutendex: API pública utilizada para obter os dados dos livros.

# Estrutura do Projeto
O projeto segue uma estrutura de pacotes organizada para separar as responsabilidades:
br.com.alura.literalura: Pacote raiz da aplicação.
model: Contém as classes de modelo (Autor.java, Livro.java), os Data Transfer Objects (AutorDTO.java, LivroDTO.java) e o record utilizado para mapeamento da API.
principal: Contém a classe Principal.java, responsável pelo menu de interação com o usuário e a lógica principal da aplicação.
repository: Contém a interface LivroRepository.java, que estende JpaRepository para operações de banco de dados.
service: Contém as classes de serviço (ConsumoAPI.java, ConverteDados.java), que lidam com a comunicação com a API e a conversão de dados JSON, respectivamente.

# Como Executar o Projeto
Pré-requisitos: Certifique-se de ter o Java 17 ou superior e um banco de dados PostgreSQL instalados.

# Configuração do Banco de Dados:
Crie um banco de dados com o nome literalura.
No arquivo application.properties (ou application.yml), configure as credenciais do seu banco de dados.

# Execução:
Execute a classe LiteraluraApplication.java como uma aplicação Spring Boot.
O menu interativo será exibido no console.
