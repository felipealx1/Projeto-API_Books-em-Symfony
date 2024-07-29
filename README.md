# Projeto API Books usando lingugaem PHP e Freamework Symfony

<body>
    <h1>API Books</h1>
    <p>Este projeto é uma aplicação web desenvolvida com PHP utilizando o framework Symfony, que fornece uma API para gerenciar livros. A aplicação usa PostgreSQL como banco de dados, que é executado em um contêiner Docker com Docker Compose, e a API é construída usando o API Platform. Além disso, o Adminer 4.8.1 foi utilizado para gerenciar o banco de dados no Docker.</p>

  <h2>Índice</h2>
    <ol>
        <li><a href="#configuração-do-ambiente">Configuração do Ambiente</a></li>
        <li><a href="#comandos-utilizados">Comandos Utilizados</a></li>
        <li><a href="#executando-a-aplicação">Executando a Aplicação</a></li>
        <li><a href="#funcionalidades-da-api">Funcionalidades da API</a></li>
        <li><a href="#api-platform">API Platform</a></li>
        <li><a href="#migrações">Migrações</a></li>
        <li><a href="#conclusão">Conclusão</a></li>
    </ol>

  <h2 id="configuração-do-ambiente">Configuração do Ambiente</h2>
    <p>Para configurar o ambiente de desenvolvimento, você precisará ter o Docker, Docker Compose e o Symfony CLI instalados em sua máquina.</p>

  <h3>Instalação do Docker e Docker Compose</h3>
    <ul>
        <li><a href="https://docs.docker.com/get-docker/">Guia de instalação do Docker</a></li>
        <li><a href="https://docs.docker.com/compose/install/">Guia de instalação do Docker Compose</a></li>
    </ul>

  <h3>Instalação do Symfony CLI</h3>
    <ul>
        <li><a href="https://symfony.com/download">Guia de instalação do Symfony CLI</a></li>
    </ul>

  <h2 id="comandos-utilizados">Comandos Utilizados</h2>

  <h3>Criando um novo projeto Symfony</h3>
    <pre><code>symfony new api-books</code></pre>

  <h3>Instalando as dependências do Composer</h3>
    <pre><code>composer install</code></pre>

  <h3>Iniciando o servidor Symfony</h3>
    <pre><code>symfony server:start -p 8000</code></pre>

   <h3>Criando uma nova entidade</h3>
    <pre><code>symfony console make:entity</code></pre>

   <h3>Criando CRUD para a entidade</h3>
    <pre><code>symfony console make:crud</code></pre>

   <h3>Requerendo o API Platform</h3>
    <pre><code>composer req api</code></pre>

   <h3>Subindo os contêineres com Docker Compose</h3>
    <pre><code>docker-compose up -d</code></pre>

   <h3>Criando uma nova migração</h3>
    <pre><code>symfony console make:migration</code></pre>

   <h3>Executando as migrações</h3>
    <pre><code>symfony console doctrine:migrations:migrate</code></pre>

  <h2 id="executando-a-aplicação">Executando a Aplicação</h2>

  <h3>Clone o repositório:</h3>
    <pre><code>git clone &lt;url-do-repositorio&gt;
cd api-books</code></pre>

  <h3>Instale as dependências do Composer:</h3>
    <pre><code>composer install</code></pre>

  <h3>Suba os contêineres do Docker:</h3>
    <pre><code>docker-compose up -d</code></pre>

  <h3>Crie a base de dados e execute as migrações:</h3>
    <pre><code>symfony console doctrine:database:create
symfony console make:migration
symfony console doctrine:migrations:migrate</code></pre>

  <h3>Inicie o servidor Symfony:</h3>
    <pre><code>symfony server:start -p 8000</code></pre>

  <h2 id="funcionalidades-da-api">Funcionalidades da API</h2>
    <p>A API fornece as seguintes funcionalidades para gerenciar livros:</p>
    <ul>
        <li><strong>POST</strong>: Adiciona um novo livro.</li>
        <li><strong>GET</strong>: Recupera informações de um ou mais livros.</li>
        <li><strong>PUT</strong>: Atualiza as informações de um livro existente.</li>
        <li><strong>DELETE</strong>: Remove um livro.</li>
    </ul>
    <p>A entidade Livro possui os seguintes campos:</p>
    <ul>
        <li><strong>id</strong>: integer</li>
        <li><strong>title</strong>: string</li>
        <li><strong>author</strong>: string</li>
        <li><strong>edition</strong>: integer (pode ser NULL)</li>
    </ul>

  <h2 id="api-platform">API Platform</h2>
    <p>O API Platform é utilizado para criar a API RESTful da aplicação. Com ele, você pode facilmente criar endpoints para as suas entidades. A configuração básica é feita no arquivo <code>config/packages/api_platform.yaml</code>.</p>

  <h2 id="migrações">Migrações</h2>
    <p>As migrações são usadas para versionar as mudanças no esquema do banco de dados. Para criar e aplicar migrações, use os seguintes comandos:</p>

  <h3>Criar uma nova migração:</h3>
    <pre><code>symfony console make:migration</code></pre>

  <h3>Executar as migrações:</h3>
    <pre><code>symfony console doctrine:migrations:migrate</code></pre>

  <h2 id="conclusão">Conclusão</h2>
    <p>Este projeto demonstra como criar uma aplicação web robusta utilizando Symfony, Docker e o API Platform. Seguindo este guia, você pode configurar seu ambiente de desenvolvimento, criar e gerenciar entidades, construir uma API e realizar migrações no banco de dados de forma eficiente.</p>
    <p>Para mais detalhes sobre cada tecnologia utilizada, consulte a documentação oficial:</p>
    <ul>
        <li><a href="https://symfony.com/doc/current/index.html">Symfony</a></li>
        <li><a href="https://docs.docker.com/">Docker</a></li>
        <li><a href="https://api-platform.com/docs/">API Platform</a></li>
    </ul>
    <p>Se tiver dúvidas ou sugestões, sinta-se à vontade para abrir uma issue ou entrar em contato.</p>
</body>
</html>
