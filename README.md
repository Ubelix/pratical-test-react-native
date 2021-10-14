# UBELIX - Avaliação Prática, React Native

_A Avaliação Prática, possui por finalidade análisar as suas competências técnicas com React Native, analisando a estrutura e boas práticas de desenvolvimento_

# Instruções

- A aplicação deve ser contruída utilzando React Native, podendo ser utilizado _Bare Workflow_ ou _Managed Workflow_.
- Tempo para a realização da atividade - 04 Horas.
- Procure utiizar as **boas práticas** de desenvolvimento e **componentização**.
- Não é necessário concluir a atividade por completa, estamos interessados em
- Procure seguir as interfaces, cores e ícones. Porém não é obrigatório, diferente da estrutura que é obrigatória.

Tenha uma boa sorte! Qualquer dúvida nos comunique.

# GitHub

- Realize um _fork_ do projeto no GitHub.
- Adicione @ubelix como um colaborador do seu _fork_.
  <br>
  _Você pode facilmente fazer isso em https://github.com/`seu-usuario`/react-native-test/settings/collaboration._
- Ao iniciar a valiação, faça um _commit_ vazio com a mensagem `release: init app` e quando finalizar, faça um _commit_ com a mensagem `release: finish app`.
- Faça vários _commits_ com o objetivo de demonstrar a construção da solução
- Não use _branches_.
- Lembre-se, procure não gastar mais do que 4 horas para finalizar o teste.

<br/>

# 🔖 Layout

O Layout da aplicação está disponível no Figma, o projeto está disponível no [link](https://www.figma.com/file/0guw67U3KwxQiY1zMzIPHX/Bookshelf?node-id=641%3A2313), e o protótipo no [link](https://www.figma.com/proto/0guw67U3KwxQiY1zMzIPHX/Bookshelf?node-id=641%3A2313&scaling=scale-down&page-id=41%3A530&starting-point-node-id=641%3A23131).

<br/>

# Avaliação Prática

### Contexto:

<br/>
<br/>

- _A aplicação possui por finalidade, através de três interfaces simples, a listagem livros disponíveis de acordo com o gênero, podendo pesquisar pelo título e autor_

<br/>
<br/>

_INFORMAÇÕES ADICIONAIS_: As resposta das requisições estão no formato JSON.
<br/>
<br/>
**1 - A Interface de Dashboard:.** Listagem de todos os gêneros disponíveis obtidos através da API da NyTimes. Informações da API no [link](https://developer.nytimes.com/docs/books-product/1/overview).
<br/>
<br/>

API:

    https://api.nytimes.com

ROTAS:

- Categorias de Livros

        https://api.nytimes.com/svc/books/v3/lists/names.json

- As coleções de livros 'Para você' e 'Os mais lidos da semana'

        https://api.nytimes.com/svc/books/v3/lists/overview.json

PARAMETROS:

- api-key:

        api-key=vi0bsV0yOCA9qYnmAaOUJV4dO0BNhUGR

CURL:

    curl -X GET https://api.nytimes.com/svc/books/v3/lists/names.json\?api-key\=vi0bsV0yOCA9qYnmAaOUJV4dO0BNhUGR

_INFORMAÇÕES ADICIONAIS_:
<br />

- Através da resposta obtida da API, renderizar cada um dos gêneros utilizando o "display_name" como nome do gênero e será necessário a informação do campo "list_name_encoded" para realizar a requisição na próxima interface, lembre-se cada um dos componentes se acionados será redirecionado para a próxima interface, onde será realizado a seleção dos livros de acordo com o gênero.

- A classificação das estrelas podem ser classificadas fixadas em 5 ou aleatórias.

- A Pesquisar deve ser realizada através dos campos:

        "author": String,
        "title": String,

<br/>
<hr/>
<br/>

**2 - Agora você deve criar uma interface com a lista de livros retornados de acordo com o gênero selecionado na primeira interface, mostrando a imagem da capa do livro, título, autor, preço e o nome da editora.**

<br />

A Listagem de todos os livros disponíveis obtidos através da API da NyTime de acordo com o gênero previamente escolido, [clique aqui](https://developer.nytimes.com/docs/books-product/1/overview).

<br />

_INFORMAÇÕES ADICIONAIS_:

- Utilize os campos do retorno da resposta da requisição:

        "publisher": String,
        "author": String,
        "title": String,
        "description": String,
        "price": String,
        "book_image": String,

- Envie as informações do livro selecionado para a próxima página:

API:

    https://api.nytimes.com

ROTA:
<br />

- kindOfBooks, no caso é a informação obtida na resposta da primeira requisição, através do campo "list_name_encoded".

        https://api.nytimes.com/svc/books/v3/lists/current/`${kindOfBooks}`.json

PARAMETROS:

- api-key:

        api-key=vi0bsV0yOCA9qYnmAaOUJV4dO0BNhUGR

<br />

CURL - Exemplo

    curl -X GET https://api.nytimes.com/svc/books/v3/lists/current/combined-print-and-e-book-fiction.json\?api-key\=vi0bsV0yOCA9qYnmAaOUJV4dO0BNhUGR

<br />

**3 - Agora você deve criar uma interface com as informações do livro de acordo com o livro selecionado na segunda interface, mostrando a imagem da capa do livro, título, autor, preço, descrição e o nome da editora.**

<br />

A Listagem de todos os livros disponíveis obtidos através da API da NyTime de acordo com o gênero previamente escolido, [clique aqui](https://developer.nytimes.com/docs/books-product/1/overview).

_INFORMAÇÕES ADICIONAIS_:

- As informações obtidas na última requisição:

        "publisher": String,
        "author": String,
        "title": String,
        "description": String,
        "price": String,
        "book_image": String,

- A classificação das estrelas podem ser classificadas fixadas em 5 ou aleatórias.
- As avaliaçxões podem ser fixadas em 36 avaliações ou aleatórias.

<br />

**_EXTRA_**
<br />
<br />

Será considerado um diferencial se você fizer tratamentos de erros, falhas de rede e indicadores de carregamento para melhorar a usabilidade do usuário.

<br />
<br />

# 🛠 Time

- Emerson Lessa &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Stackholder)
- George Lima &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Stackholder)
- Wilson Lima &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Stackholder)
- Taynan Penini &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Ux/Ui Designer)
- Everton Ferreira &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Arquiteto de Software) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [LinkedIn](https://www.linkedin.com/in/evertonferreira96/)
- Vinicius Passos &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (Especialista de Desenvolvimento) &nbsp;&nbsp;&nbsp; [LinkedIn](https://www.linkedin.com/in/vtpa/) . [GitHub](https://github.com/vtpa)

<br />
<hr />
<br />

<h4 align="center"> 
    Feito com ♥ por Everton Ferreira e Taynan Ferreira
</h4>
