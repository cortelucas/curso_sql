# Lista 4

- 1 - Selecione somente o nome e salário dos funcionários.
    
    ```sql
    SELECT nome, salario FROM funcionarios;
    ```
    
    | nome | salario |
    | --- | --- |
    | Lucas S. Corte | 2345.67 |
    | Andressa K. Mendes | 1234.56 |
    | Leonardo S. Silva | 1324.65 |
    | Luiz Antonio C. Santos | 1435.62 |
- 2 - Selecione somente o nome e telefone dos funcionários.
    
    ```sql
    SELECT nome, telefone FROM funcionarios;
    ```
    
    | nome | telefone |
    | --- | --- |
    | Lucas S. Corte | 99999-9898 |
    | Andressa K. Mendes | 99999-8989 |
    | Leonardo S. Silva | 99999-7878 |
    | Luiz Antonio C. Santos | 99999-6969 |
- 3 - Selecione somente o nome, rg e cpf dos funcionários.
    
    ```sql
    SELECT nome, rg, cpf FROM funcionarios;
    ```
    
    | nome | rg | cpf |
    | --- | --- | --- |
    | Lucas S. Corte | 44.444.444-44 | 555.555.555-55 |
    | Andressa K. Mendes | 55.555.555-55 | 444.444.444-44 |
    | Leonardo S. Silva | 66.664.664-66 | 777.777.777-77 |
    | Luiz Antonio C. Santos | 77.774.774-77 | 222.222.222-11 |
- 4 - Selecione somente o nome e a cidade dos funcionários.
    
    ```sql
    SELECT nome, cidade FROM funcionarios;
    ```
    
    | nome | cidade |
    | --- | --- |
    | Lucas S. Corte | Junqueirópolis |
    | Andressa K. Mendes | Junqueirópolis |
    | Leonardo S. Silva | Junqueirópolis |
    | Luiz Antonio C. Santos | Junqueirópolis |
- 5 - Insira mais um funcionário.
    
    ```sql
    INSERT INTO funcionarios (
    	codigo, nome, endereco, telefone, cidade, estado, cep, rg, cpf, salario
    )
    VALUES(
    	5, 'Sonia Maria C. Saudino', 'Rua Florianópolis, 159', '99999-9696', 'Junqueirópolis', 'São Paulo', '17.890-000', '78.784.784-78', '121.212.121-21', 4320.90
    );
    ```
    
- 6 - Exiba todos os dados dos funcionários.
    
    ```sql
    SELECT * FROM funcionarios;
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 1 | Lucas S. Corte | Rua Porto Alegre, 1660 | 99999-9898 | Junqueirópolis | São Paulo | 17.890-000 | 44.444.444-44 | 555.555.555-55 | 2345.67 |
    | 2 | Andressa K. Mendes | Av Marconi, 133 | 99999-8989 | Junqueirópolis | São Paulo | 17.890-000 | 55.555.555-55 | 444.444.444-44 | 1234.56 |
    | 3 | Leonardo S. Silva | Rua Victor Junqueira, 555 | 99999-7878 | Junqueirópolis | São Paulo | 17.890-000 | 66.664.664-66 | 777.777.777-77 | 1324.65 |
    | 4 | Luiz Antonio C. Santos | Rua Porto Alegre, 1660 | 99999-6969 | Junqueirópolis | São Paulo | 17.890-000 | 77.774.774-77 | 222.222.222-11 | 1435.62 |
    | 5 | Sonia Maria C. Saudino | Rua Florianópolis, 159 | 99999-9696 | Junqueirópolis | São Paulo | 17.890-000 | 78.784.784-78 | 121.212.121-21 | 4320.9 |
- 7 - Crie a tabela fornecedores contendo os campos nome, endereço, telefone, cidade, estado, cep, cnpj e email. Coloque os tipos de dados necessários.
    
    ```sql
    CREATE TABLE fornecedores (
    	codigo INTEGER PRIMARY KEY AUTOINCREMENT,
    	nome TEXT(200),
    	endereco TEXT(200),
    	telefone TEXT(25),
    	cidade TEXT(100),
    	estado TEXT(100),
    	cep TEXT(20),
    	cnpj TEXT(50),
    	email TEXT(100)
    );
    ```
    
- 8 - Insira 2 fornecedores. Código 1 e Código 2
    
    ```sql
    INSERT INTO fornecedores (
    	nome, endereco, telefone, cidade, estado, cep, cnpj, email
    )
    VALUES(
    	'DBA SA', 'Rua José de Sá', '3333-3434', 'Junqueirópolis', 'São Paulo', '17.890-000', '04.304.168/0001-41', 'dba@sa.com'
    );
    
    INSERT INTO fornecedores (
    	nome, endereco, telefone, cidade, estado, cep, cnpj, email
    )
    VALUES(
    	'IT Comunication', 'AV Rio Brilhante', '3333-3939', 'Junqueirópolis', 'São Paulo', '17.890-000', '69.417.380/0001-60', 'diretoria@it.com'
    );
    ```
    
- 9 - Selecione o nome e o telefone dos fornecedores.
    
    ```sql
    SELECT nome, telefone FROM fornecedores;
    ```
    
    | nome | telefone |
    | --- | --- |
    | DBA SA | 3333-3434 |
    | IT Comunication | 3333-3939 |
- 10 - Agora iremos aprender uma opção do comando select. Nós podemos restringir o que vai ser exibido na tela. É moleza. Por exemplo se eu quiser listar somente o aluno de código 2 o comando fica assim: select * from alunos where codigo = 2; - Nós apenas adicionamos o WHERE e a CONDIÇÃO. Veja que mantivemos o * para exibir todos os campos, mas poderíamos também exibir somente o nome do aluno 2 assim: select nome from alunos where codigo = 2; - EXPERIMENTE AGORA ESSES 2 COMANDOS.
    
    ```sql
    SELECT * FROM alunos WHERE codigo = 2;
    ```
    
    | codigo | nome | telefone | cidade |
    | --- | --- | --- | --- |
    | 2 | Lucas | 9999-8888 | Junqueirópolis |
    
    ```sql
    SELECT nome FROM alunos WHERE codigo = 2;
    ```
    
    nome
    
    ---
    
    Lucas
    
    ---
    
- 11 - Selecione o funcionário de código 3.
    
    ```sql
    SELECT * FROM funcionarios WHERE codigo = 3;
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 3 | Leonardo S. Silva | Rua Victor Junqueira, 555 | 99999-7878 | Junqueirópolis | São Paulo | 17.890-000 | 66.664.664-66 | 777.777.777-77 | 1324.65 |
- 12 - Selecione o fornecedor de código 1.
    
    ```sql
    SELECT * FROM fornecedores WHERE codigo = 1;
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | cnpj | email |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 1 | DBA SA | Rua José de Sá | 3333-3434 | Junqueirópolis | São Paulo | 17.890-000 | 04.304.168/0001-41 | mailto:dba@sa.com |
- 13 - Selecione o aluno de código 2.
    
    ```sql
    SELECT * FROM alunos WHERE codigo = 2;
    ```
    
    | codigo | nome | telefone | cidade |
    | --- | --- | --- | --- |
    | 2 | Lucas | 9999-8888 | Junqueirópolis |
- 14 - Selecione o funcionário de código 1.
    
    ```sql
    SELECT * FROM funcionarios WHERE codigo = 1;
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 1 | Lucas S. Corte | Rua Porto Alegre, 1660 | 99999-9898 | Junqueirópolis | São Paulo | 17.890-000 | 44.444.444-44 | 555.555.555-55 | 2345.67 |
- 15 - Selecione somente o nome e salário do funcionário de código 2.
    
    ```sql
    SELECT nome, salario FROM funcionarios WHERE codigo = 2;
    ```
    
    | nome | salario |
    | --- | --- |
    | Andressa K. Mendes | 1234.56 |
- 16 - Selecione somente o nome a cidade do aluno de código 1.
    
    ```sql
    SELECT nome, cidade FROM alunos WHERE codigo = 1;
    ```
    
    | nome | cidade |
    | --- | --- |
    | Ana | Ituiutaba |
- 17 - Selecione todos os funcionários de MG. É assim: select * from funcionários where estado=’MG’; -Como estado é texto eu usei aspas! – Faça isso agora!
    
    ```sql
    SELECT * FROM funcionarios WHERE estado = "MG";
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 6 | Floriano Peixoto | Rua Pitú, 159 | 99999-9696 | Pitulandia | MG | 17.890-000 | 87.874.874-87 | 212.121.212-12 | 4320.9 |
- 18 - Selecione todos os funcionários de GO.
    
    ```sql
    SELECT * FROM funcionarios WHERE estado = 'GO';
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 6 | Pedro Ludovico Teixeira | Íris Rezende, 211 | 99999-9696 | Goiania | GO | 74.893-255 | 69.696.969-69 | 969.696.969-69 | 2320.9 |
- 19 - Selecione todos os funcionários de SP.
    
    ```sql
    SELECT * FROM funcionarios WHERE estado = "SP";
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 1 | Lucas S. Corte | Rua Porto Alegre, 1660 | 99999-9898 | Junqueirópolis | SP | 17.890-000 | 44.444.444-44 | 555.555.555-55 | 2345.67 |
    | 2 | Andressa K. Mendes | Av Marconi, 133 | 99999-8989 | Junqueirópolis | SP | 17.890-000 | 55.555.555-55 | 444.444.444-44 | 1234.56 |
    | 3 | Leonardo S. Silva | Rua Victor Junqueira, 555 | 99999-7878 | Junqueirópolis | SP | 17.890-000 | 66.664.664-66 | 777.777.777-77 | 1324.65 |
    | 4 | Luiz Antonio C. Santos | Rua Porto Alegre, 1660 | 99999-6969 | Junqueirópolis | SP | 17.890-000 | 77.774.774-77 | 222.222.222-11 | 1435.62 |
    | 5 | Sonia Maria C. Saudino | Rua Florianópolis, 159 | 99999-9696 | Junqueirópolis | SP | 17.890-000 | 78.784.784-78 | 121.212.121-21 | 4320.9 |
- 20 - Insira um funcionário para SP.
    
    ```sql
    INSERT INTO funcionarios (
    	codigo, nome, endereco, telefone, cidade, estado, cep, rg, cpf, salario
    )
    VALUES(
    	7, 'Kim Patroca Kataguiri', 'Av Aricanduva, 12211', '99898-9696', 'São Paulo', 'SP', '03.527-000', '24.834.802-4', '783.457.431-02', 2520.90
    );
    ```
    
- 21 - Selecione todos os funcionários de SP.
    
    ```sql
    SELECT * FROM funcionarios WHERE estado = 'SP';
    ```
    
    | codigo | nome | endereco | telefone | cidade | estado | cep | rg | cpf | salario |
    | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
    | 1 | Lucas S. Corte | Rua Porto Alegre, 1660 | 99999-9898 | Junqueirópolis | SP | 17.890-000 | 44.444.444-44 | 555.555.555-55 | 2345.67 |
    | 2 | Andressa K. Mendes | Av Marconi, 133 | 99999-8989 | Junqueirópolis | SP | 17.890-000 | 55.555.555-55 | 444.444.444-44 | 1234.56 |
    | 3 | Leonardo S. Silva | Rua Victor Junqueira, 555 | 99999-7878 | Junqueirópolis | SP | 17.890-000 | 66.664.664-66 | 777.777.777-77 | 1324.65 |
    | 4 | Luiz Antonio C. Santos | Rua Porto Alegre, 1660 | 99999-6969 | Junqueirópolis | SP | 17.890-000 | 77.774.774-77 | 222.222.222-11 | 1435.62 |
    | 5 | Sonia Maria C. Saudino | Rua Florianópolis, 159 | 99999-9696 | Junqueirópolis | SP | 17.890-000 | 78.784.784-78 | 121.212.121-21 | 4320.9 |
    | 7 | Kim Patroca Kataguiri | Av Aricanduva, 12211 | 99898-9696 | São Paulo | SP | 03.527-000 | 24.834.802-4 | 783.457.431-02 | 2520.9 |
- 22 - Crie a tabela livros contendo o campo código, nome, categoria, resumo, precocusto, precovenda.
    
    ```sql
    CREATE TABLE livros (
    	codigo INTEGER PRIMARY KEY AUTOINCREMENT,
    	nome TEXT(200),
    	categoria TEXT(100),
    	resumo TEXT(500),
    	preco_custo NUMBER,
    	preco_venda NUMBER
    );
    ```
    
- 23 - Verifique o esquema .schema da tabela livros.
    
    ```powershell
    sqlite> .schema livros
    CREATE TABLE livros (
            codigo INTEGER PRIMARY KEY AUTOINCREMENT,
            nome TEXT(200),
            categoria TEXT(100),
            resumo TEXT(500),
            preco_custo NUMBER,
            preco_venda NUMBER
    );
    ```
    
- 24 - Liste as tabelas existentes.
    
    ```powershell
    sqlite> .tables
    alunos        fornecedores  funcionarios  livros
    ```
    
- 25 - Insira 1 livro.
    
    ```powershell
    INSERT INTO livros (
    	nome, categoria, resumo, preco_custo, preco_venda
    )
    VALUES(
    	'Harry Potter e a Pedra Filosofal', 'Fantasia', 'Harry Potter e a Pedra Filosofal é o primeiro dos sete livros da série de fantasia Harry Potter, escrita por J. K. Rowling. O livro conta a história de Harry Potter, um órfão criado pelos tios que descobre, em seu décimo primeiro aniversário, que é um bruxo.', 12.5, 50.54
    );
    ```
    
- 26 - Selecione o nome e a categoria do livro de código 1.
    
    ```sql
    SELECT nome, categoria FROM livros WHERE codigo = 1;
    ```
    
    | nome | categoria |
    | --- | --- |
    | Harry Potter e a Pedra Filosofal | Fantasia |
- 27 - Selecione o nome e a categoria do livro de código 3.
    
    ```sql
    SELECT nome, categoria FROM livros WHERE codigo = 3;
    ```
    
    | nome | categoria |
    | --- | --- |
    | Harry Potter e a Câmara Secreta | Fantasia |
- 28 - Exclua a tabela livros.
    
    ```sql
    DROP TABLE livros;
    ```
    
- 29 - Altere o nome da tabela aluno para estudantes.
    
    ```sql
    ALTER TABLE alunos RENAME TO estudantes;
    ```
    
- 30 - Altere a tabela alunos inserindo o campo estado. Se estiver com dúvidas consulte a primeira lista de exercícios.
    
    ```sql
    ALTER TABLE estudantes ADD estado TEXT(2);
    ```