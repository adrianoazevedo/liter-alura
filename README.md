# 📚 LiterAlura

O LiterAlura é uma aplicação web que permite aos usuários buscar e visualizar livros em diversas categorias, autores e idiomas, via API do Gutendex. Tópicos detalhando como configurar e utilizar a aplicação.


## 📌 Configurações Iniciais

### 1. Configuração do Banco de Dados

#### 1.1. Instalação do PostgreSQL
- Tenha certeza de ter o PostgreSQL instalado em seu computador.

#### 1.2. Configuração do Banco de Dados
1. Abra seu pgAdmin.
2. Clique em Servers.
3. Em Databases, clique com o botão direito > Create > Database > No campo database insira o nome `liter_alura`.

#### 1.3. Configuração do Banco na Aplicação
1. Em `application.properties`, atualize os seguintes campos quando você configurou, ao instalar seu PostgreSQL:
   <img src="https://github.com/adrianoazevedo/liter-alura/blob/main/assets/config-banco-dadosc.png" width="500">

#### 1.4. Configuração Extra
- Para visualizar no console as queries, descomente as seguintes linhas em `application.properties`:
    ```properties
    # spring.jpa.show-sql=true
    # spring.jpa.format-sql=true
    ```

### 🖥️ 2. Utilizando a Aplicação

#### 2.1. Inicialização
- Inicie o `LiterAluraApplication` pela sua IDE.

#### 2.2. Popular o Banco de Dados
1. Acesse a URL: [http://localhost:8080/livro/popular-banco](http://localhost:8080/livro/popular-banco).
    - OBS.: Se demorar um pouco, é normal pq é a aplicação consultando a API do Gutendex e populando o banco. No console da IDE, mostra os livros sendo cadastrados e, no final, te devolverá um JSON com todos os livros cadastrados.

#### 2.3. Acessar a Aplicação
- Acesse a URL: [http://localhost:8080/livro/](http://localhost:8080/livro/).
- Utilizar os filtros.

### 📖 3. Tabela de Filtros

| Filtro  | Descrição |
|---------|-----------|
| Gênero  | Filtra os livros por gênero |
| Autor   | Filtra os livros por autor, aceita nome, sobrenome ou uma parte |
| Idioma  | Filtra os livros por idioma |
| Título  | Filtra os livros por título, aceita o título da obra inteira ou parte |

## 🔧⚙️ Verificação via Postman ou APIDog

### URLs para Verificação

- [http://localhost:8080/livro/](http://localhost:8080/livro/) - Para Listar os dados utilizando o Front e Back em conjunto.
- [http://localhost:8080/livro/popular-banco](http://localhost:8080/livro/popular-banco) - Para popular o banco ou ver os registros já salvos.
- [http://localhost:8080/livro/autor/InserirNomeDoAutor](http://localhost:8080/livro/autor/InserirNomeDoAutor) - Para listar as obras desse autor.
- [http://localhost:8080/livro/genero/InserirGenero](http://localhost:8080/livro/genero/InserirGenero) - Para listar as obras desse gênero.
- [http://localhost:8080/livro/idioma/InserirIdioma](http://localhost:8080/livro/idioma/InserirIdioma) - Para listar as obras desse idioma.
- [http://localhost:8080/livro/top5](http://localhost:8080/livro/top5) - Para listar as 5 obras mais baixadas.
- [http://localhost:8080/livro/obra/InserirNomeDoLivro](http://localhost:8080/livro/obra/InserirNomeDoLivro) - Para listar as obras com esse título.

## ⌨️ Desenvolvimento

### Passos seguidos para o Desenvolvimento

1. Desenvolvimento da arquitetura.
2. Criação do Controller.
3. Solução para o back-end com DTOs e já realizando consultas.
4. Testes via APIDog.
5. Criação do index e primeira integração do back-end com o front-end (mostrar todos os livros).
6. Criação do JavaScript para deixar dinâmico (chamando os livros e Top 5) e utilizando os filtros via controller, mostrando os livros.
7. Desenvolvimento do CSS.
8. Testes no back-end e front-end integrados.

## 📚 Tecnologias Utilizadas

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" alt="Spring" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" alt="PostgreSQL" width="50" height="50"/>
  <img src="https://cdn-icons-png.flaticon.com/512/2160/2160724.png" alt="API Gutendex" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML" width="50" height="50"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS" width="50" height="50"/>
</p>

### Versões

- **Java**: 17
- **Spring**: Spring Framework
- **PostgreSQL**: PostgreSQL
- **API**: Gutendex
- **JavaScript**: JavaScript
- **HTML**: HTML
- **CSS**: CSS

## ⚠️ Copyright

- Imagens de livros do Header por Freepik.
- Ícones por Phosphor Icons.
