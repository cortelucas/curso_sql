# Lista 5

- 1 - Crie no SqliteStudio um banco de dados chamado lista5.sqlite e execute os comandos abaixo.
    
    ```powershell
    curso_sql on main ≡  +2
    ➜ sqlite3.exe "C:\Users\lcorte\OneDrive - Capgemini\Documents\Curso - SQL\curso_sql\atividades\lista_05\lista_05.sqlite"
    
    SQLite version 3.40.1 2022-12-28 14:03:47
    Enter ".help" for usage hints.
    sqlite>
    ```
    
- 2 - Crie uma tabela com o nome de livros contendo os campos codigo, titulo, codigo do autor, código da editora, código do estilo, sinopse e isbn. Sugestão de nome de campo: autor_codigo, editora_codigo
    
    ```sql
    CREATE TABLE livros (
    	id INT PRIMARY KEY,
    	titulo VARCHAR(150),
    	autor_id INT,
    	editora_id INT,
    	estilo_id INT,
    	sinopse VARCHAR(300),
    	isbn NUMBER
    )
    ```
    
- 3 - Crie uma tabela com o nome de editoras contendo o codigo, nome, cidade, estado, telefone e e-mail.
    
    ```sql
    CREATE TABLE editoras (
    	id INT PRIMARY KEY,
    	nome VARCHAR(150),
    	cidade VARCHAR(100),
    	estado VARCHAR(2),
    	telefone VARCHAR(30),
    	email VARCHAR(100)
    )
    ```
    
- 4 - Crie uma tabela com o nome de estilos contendo o código e o nome do estilo.
    
    ```sql
    CREATE TABLE estilos (
    	id INT PRIMARY KEY,
    	nome VARCHAR(150)
    )
    ```
    
- 5 - Crie uma tabela com o nome de autores contendo o codigo, nome, cidade, estado, telefone do autor.
    
    ```sql
    CREATE TABLE autores (
    	id INT PRIMARY KEY,
    	nome VARCHAR(150),
    	cidade VARCHAR(100),
    	estado VARCHAR(2),
    	telefone VARCHAR(30)
    )
    ```
    
- 6 - Insira um registro na tabela livros (todos os campos)
    
    ```sql
    INSERT INTO livros (
    	titulo, autor_id, editora_id, estilo_id, sinopse, isbn
    )
    VALUES(
    	'Harry Potter e a Pedra Filosofal', 1, 1, 6, 'Harry Potter é um garoto órfão que vive infeliz com seus tios, os Dursleys. Ele recebe uma carta contendo um convite para ingressar em Hogwarts, uma famosa escola especializada em formar jovens bruxos. Inicialmente, Harry é impedido de ler a carta por seu tio, mas logo recebe a visita de Hagrid, o guarda-caça de Hogwarts, que chega para levá-lo até a escola. Harry adentra um mundo mágico que jamais imaginara, vivendo diversas aventuras com seus novos amigos, Rony Weasley e Hermione Granger.',  9780545069670
    );
    ```
    
- 7 - Insira um registro na tabela editoras (todos os campos).
    
    ```sql
    INSERT INTO editoras (
    	nome, cidade, estado, telefone, email
    )
    VALUES(
    	'Editora Rocco', 'Rio de Janeiro', 'RJ', '(21) 3525-2000', 'rocco@rocco.com.br'
    );
    ```
    
- 8 - Insira um registro na tabela estilos (todos os campos).
    
    ```sql
    INSERT INTO estilos (
    	nome
    )
    VALUES(
    	'Fantasia'
    );
    ```
    
- 9 - Insira um registro na tabela autores (todos os campos).
    
    ```sql
    INSERT INTO autores (
    	nome, cidade, estado, telefone
    )
    VALUES (
    	'J. K. Rowling', 'Yate', 'YA', '(99) 9999-9999'
    );
    ```
    
- 10 - Altere o nome da tabela autores para autor.
    
    ```sql
    ALTER TABLE autores RENAME TO autor;
    ```
    
- 11 - Insira na tabela livros um novo registro adicionando somente os campos codigo e nome
    
    ```sql
    INSERT INTO livros (
    	titulo
    )
    VALUES(
    	'Harry Potter e a Câmara Secreta'
    );
    ```
    
- 12 - Insira 5 estilos de livros (comédia, drama, ficção, suspense, romance).
    
    ```sql
    INSERT INTO estilos
    (nome)
    VALUES('Comédia');
    INSERT INTO estilos
    (nome)
    VALUES('Drama');
    INSERT INTO estilos
    (nome)
    VALUES('Ficção');
    INSERT INTO estilos
    (nome)
    VALUES('Suspense');
    INSERT INTO estilos
    (nome)
    VALUES('Romance');
    ```
    
- 13 - Selecionar todos os livros do banco de dados.
    
    ```sql
    SELECT * FROM livros;
    ```
    
    | id | titulo | autor_id | editora_id | estilo_id | sinopse | isbn |
    | --- | --- | --- | --- | --- | --- | --- |
    | 1 | Harry Potter e a Pedra Filosofal | 1 | 1 | 6 | Harry Potter é um garoto órfão que vive infeliz com seus tios, os Dursleys. Ele recebe uma carta contendo um convite para ingressar em Hogwarts, uma famosa escola especializada em formar jovens bruxos. Inicialmente, Harry é impedido de ler a carta por seu tio, mas logo recebe a visita de Hagrid, o guarda-caça de Hogwarts, que chega para levá-lo até a escola. Harry adentra um mundo mágico que jamais imaginara, vivendo diversas aventuras com seus novos amigos, Rony Weasley e Hermione Granger. | 9780545069670 |
    | 2 | Harry Potter e a Câmara Secreta |  |  |  |  |  |
- 14 - Insira 2 novos livros.
    
    ```sql
    INSERT INTO livro (
    	titulo, autor_id, editora_id, estilo_id, sinopse, isbn
    )
    VALUES(
    	'Harry Potter e o Prisioneiro de Azkaban', 1, 1, 6, 'É o início do terceiro ano na escola de bruxaria Hogwarts. Harry, Ron e Hermione têm muito o que aprender. Mas uma ameaça ronda a escola e ela se chama Sirius Black. Após doze anos encarcerado na prisão de Azkaban, ele consegue escapar e volta para vingar seu mestre, Lord Voldemort. Para piorar, os Dementores, guardas supostamente enviados para proteger Hogwarts e seguir os passos de Black, parecem ser ameaças ainda mais perigosas.',  9780439554923
    );
    
    INSERT INTO livro (
    	titulo, autor_id, editora_id, estilo_id, sinopse, isbn
    )
    VALUES(
    	'Harry Potter e o Cálice de Fogo', 1, 1, 6, 'Harry retorna para seu quarto ano na Escola de Magia e Bruxaria de Hogwarts, junto com os seus amigos Ron e Hermione. Desta vez, acontece um torneio entre as três maiores escola de magia, com um participante selecionado de cada escola, pelo Cálice de Fogo. O nome de Harry aparece, mesmo não tendo se inscrito, e ele precisa competir.',  9788893819930
    );
    ```
    
- 15 - Altere o nome da tabela livros autores para livro.
    
    ```sql
    ALTER TABLE livros RENAME TO livro;
    ```
    
- 16 - DESAFIO: Selecione o nome de todos os estilos em ordem alfabética
    
    ```sql
    SELECT * FROM estilos ORDER BY nome;
    ```
    
    | id | nome |
    | --- | --- |
    | 1 | Comédia |
    | 2 | Drama |
    | 6 | Fantasia |
    | 3 | Ficção |
    | 5 | Romance |
    | 4 | Suspense |
- 17 - DESAFIO: Selecione o nome de todos os autores em ordem alfabética inversa
    
    ```sql
    SELECT * FROM  autor ORDER BY nome DESC;
    ```
    
- 18 - Selecione o nome e o telefone de todas as editoras.
    
    ```sql
    SELECT nome, telefone FROM editoras;
    ```
    
- 19 - Selecione o nome de todas as editoras
    
    ```sql
    SELECT nome FROM editoras;
    ```
    
- 20 - Selecione o nome de todas as editoras de MG
    
    ```sql
    SELECT nome FROM editoras WHERE estado = "MG";
    ```
    
- 21 - Selecione os estilos de livros em ordem alfabética.
    
    ```sql
    SELECT * FROM estilos ORDER BY nome;
    ```
    
- 22 - Selecione agora em ordem alfabética inversa.
    
    ```sql
    SELECT * FROM estilos ORDER BY nome DESC;
    ```
    
- 23 - Selecione o nome de todos os autores de SP.
    
    ```sql
    SELECT nome FROM autor WHERE estado = "SP";
    ```
    
- 24 - Selecione o estilo de código 13
    
    ```sql
    SELECT * FROM estilos WHERE codigo = 13;
    ```
    
- 25 - Selecione o autor de código 8
    
    ```sql
    SELECT * FROM autor WHERE codigo = 8;
    ```
    
- 26 - Selecione a editora de código 10
    
    ```sql
    SELECT * FROM editoras WHERE codigo = 10;
    ```
    
- 27 - Selecione o nome, a cidade e o estado de todas as editoras.
    
    ```sql
    SELECT nome, cidade, estado FROM editoras;
    ```
    
- 28 - Adicione 3 editoras.
    
    ```sql
    INSERT INTO editoras (
    	nome, cidade, estado, telefone, email
    )
    VALUES(
    	'Companhia da Letras', 'São Paulo', 'SP', '(11) 3707-3500', 'compainha@letras.com.br'
    );
    
    INSERT INTO editoras (
    	nome, cidade, estado, telefone, email
    )
    VALUES(
    	'Alef', 'São Paulo', 'SP', '(11) 3743-3202', 'editora@aleph.com.br'
    );
    
    INSERT INTO editoras (
    	nome, cidade, estado, telefone, email
    )
    VALUES(
    	'Leya', 'São Paulo', 'SP', '(11) 3333-3131', 'sac@leyabrasil.com.br'
    );
    ```
    
- 29 - Selecione o nome de todas as editoras
    
    ```sql
    SELECT nome FROM editoras;
    ```
    
- 30 - Exclua a editora de código 1
    
    ```sql
    DELETE FROM editoras WHERE codigo=1;
    ```