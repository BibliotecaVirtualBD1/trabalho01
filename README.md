# TRABALHO 01:  Título do Trabalho
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Gustavo Dutra: gdsantolin@gmail.com<br>
Marina Milagres: nafkyn@gmail.com<br>
...

### 2.INTRODUÇÃO E MOTIVAÇAO<br>
Este documento contém a especificação do projeto do banco de dados Biblioteca Virtual 
<br>e motivação da escolha realizada. <br>

> Nosso grupo se empenha em desenvolver projetos para uma sociedade melhor e mais inteligente artificialmente. Sabendo das dificuldades de manuntenção do espaço e das limitações de uma biblioteca física, pensamos em como trabalhar em cima dessas limitações e fazer uma Biblioteca Virtual de fácil acesso. O sistema tem como objetivo facilitar a comunicação entre os leitores, relacionar seus comentários e resenhas sobre os livros, entre outras atualizações. É uma rede social para leitores de vários gêneros em diferentes países que querem compartilhar suas experiências. O sistema precisa armazenar as relações entre os gêneros dos livros, comentários de leitores e escritores, datas de lançamento e encontros próximos à localização do usuário.
 

### 3.MINI-MUNDO<br>

Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.


> O sistema proposto conterá as informacões aqui detalhadas. O usuário deverá cadastrar-se, inserindo o endereço de e-mail, nome de usuário público e senha. O usuário pode optar (no cadastro) por receber ou não notificações por e-mail. 
> No sistema, serão armazenados o nome dos livros, o gênero ao qual pertencem, nome do autor, número de usuários que leram o livro, comentários, resenhas, livros de gênero parecido e indicações para o usuário.
> Haverão 5 abas: a aba "Início" contém as notícias principais da conta do usuário, como atividades recentes de amigos, notícias de autores, etc. Há a opção de favoritar ou comentar as publicações. Além disso, você pode ver os eventos perto de você, as novidades e o que está em alta.
> A aba "perfil" conterá as informações do perfil do usuário. Você pode editar seu perfil, seus livros favoritados, os autores que você segue, seus amigos e os eventos que você já participou.
> A aba "notificações" mostra especificamente qual atividade recente ocorreu e quando ocorreu, como o registro de um novo livro de um autor que você segue, alterações feitas no seu perfil, etc. 
> A aba "conversas" será usada para enviar mensagens aos usuários adicionados. Será possível enviar links de autores, livros e eventos na conversa.
> A aba "postar" exige que você especifique o nome do livro ou do autor e permite que o usuário mostre sua opinião sobre o autor ou o livro, postando publicamente.
> No perfil do usuário, serão armazenados os livros que ele já leu, os que ele tem interesse, eventos que ele confirmou presença/já foi, amizades com outros usuários, resenhas e recomendações. Além disso, cada perfil deverá ter obrigatoriamente um e-mail (que deverá ser validado), um nome e uma linguagem principal; e opcionalmente, a localização (necessária para receber atualizações de encontros e lançamentos), foto de perfil, outras linguagens, autor e livro preferido.
> No perfil de cada autor, serão armazenadas suas informações básicas, como nome, data de nascimento, idade atual (ou data da morte), os livros que ele escreveu (organizado em ordem de lançamento), autores parecidos (que serão determinados comparando os gêneros literários em comum), livro mais vendido e eventos que comparecerá. Os usuários poderão comentar no perfil dos autores e enviar resenhas dos livros.
> O usuário poderá procurar outros usuários, livros ou autores por meio de uma barra de pesquisa. Para facilitar, ao pesquisar um nome qualquer, haverão seções de "livros", "usuários" e "autores".
> 


### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser desenvolvidas. O princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas e/ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/biblioteca_comentarios.png "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Devcom](https://github.com/discipint/trabalho01/blob/master/arquivos/EmpresaDevcom.pdf?raw=true "Empresa Devcom")<br>
>Arquivo PDF do Protótipo Balsamiq feito para Biblioteca Virtual
https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/arquivos/Biblioteca%20Virtual%20(2).pdf


#### 4.1 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    e deve ser criada antes do modelo conceitual
    c) Após criada esta tabela não deve ser modificada, pois será comparada com os resultados finais na conclusão do trabalho
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/arquivos/Tabela_biblioteca.ods "Tabela de dados")
    
    
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
>A biblioteca virtual deve fornecer os seguintes relatórios:
* Relatório de cadastro que informe o e-mail, nome de usuário e a senha do usuário.
* Relatório de edição do perfil que informe o sexo do usuário, línguas, seu país, estado, cidade e opcionalmente o bairro do usuário, gênero(s) preferido de leitura, livro(s) e/ou autor(es) preferidos.
* Relatório com as informações do autor (País, estado, cidade, sexo e livros escritos).
* Relatório com a lista de amigos (usuários) adicionados pelo usuário.
* Relatório que informa os eventos próximos baseado na localização fornecida pelo usuário.
    
>## Marco de Entrega 01 em: (24/03/2018)<br>

### 5.MODELO CONCEITUAL<br>
    A) NOTACAO ENTIDADE RELACIONAMENTO 
        * Para nosso prótótipo limitaremos o modelo conceitual nas 5 principais entidades do escopo
        * O protótipo deve possui no mínimo duas relações N para N
        * o mínimo de entidades do modelo conceitual será igual a 5
        
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/brmodelo.png "Modelo Conceitual")
    
    B) NOTACAO UML (Caso esteja fazendo a disciplina de analise)
    C) QUALIDADE 
        Garantir que a semântica dos atributos seja clara no esquema
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]
## Marco de Entrega 01 em: (20/04/2018)<br>
#### 5.2 DECISÕES DE PROJETO
    [atributo]: [descrição da decisão]
    
    EXEMPLO:
    a) Campo endereço: em nosso projeto optamos por um campo multivalorado e composto, pois a empresa 
    pode possuir para cada departamento mais de uma localização... 
    b) justifique!

#### 5.3 DESCRIÇÃO DOS DADOS 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>

>## Marco de Entrega 01 em: (12/05/2018)<br>
### 6	MODELO LÓGICO<br>
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
   ![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/modelo_logico.png "Modelo lógico")

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..) 
        /* Lógico_1: */

CREATE TABLE PESSOA (
    nome varchar(50),
    país varchar(50),
    cidade varchar(50),
    estado varchar(50)
);

CREATE TABLE AUTOR (
    codigo int PRIMARY KEY
);

CREATE TABLE USUARIO (
    email varchar(50),
    senha varchar(50),
    PRIMARY KEY (email, senha)
);

CREATE TABLE EVENTO (
    cod_evento int PRIMARY KEY,
    localizacao varchar(50),
    data date,
    hora time
);

CREATE TABLE LIVRO (
    genero varchar(30),
    nome_livro varchar(30),
    cod_livro int PRIMARY KEY
);

CREATE TABLE Amizade (
    FK_USUARIO_email varchar(50),
    FK_USUARIO_senha varchar(50),
    FK_USUARIO_email_ varchar(50),
    FK_USUARIO_senha_ varchar(50)
);

CREATE TABLE Comparece (
    FK_EVENTO_cod_evento int,
    FK_USUARIO_email varchar(50),
    FK_USUARIO_senha varchar(50)
);

CREATE TABLE Leu (
    FK_USUARIO_email varchar(50),
    FK_USUARIO_senha varchar(50),
    FK_LIVRO_cod_livro int
);

CREATE TABLE Postagem (
    FK_USUARIO_email varchar(50),
    FK_USUARIO_senha varchar(50),
    FK_LIVRO_cod_livro int,
    curtidas int
);

CREATE TABLE Escreveu (
    FK_AUTOR_codigo int,
    FK_LIVRO_cod_livro int
);
 
ALTER TABLE Amizade ADD CONSTRAINT FK_Amizade_0
    FOREIGN KEY (FK_USUARIO_email, FK_USUARIO_senha)
    REFERENCES USUARIO (email, senha)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Amizade ADD CONSTRAINT FK_Amizade_1
    FOREIGN KEY (FK_USUARIO_email_, FK_USUARIO_senha_)
    REFERENCES USUARIO (email, senha)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Comparece ADD CONSTRAINT FK_Comparece_0
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Comparece ADD CONSTRAINT FK_Comparece_1
    FOREIGN KEY (FK_USUARIO_email, FK_USUARIO_senha)
    REFERENCES USUARIO (email, senha)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Leu ADD CONSTRAINT FK_Leu_0
    FOREIGN KEY (FK_USUARIO_email, FK_USUARIO_senha)
    REFERENCES USUARIO (email, senha)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Leu ADD CONSTRAINT FK_Leu_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Postagem ADD CONSTRAINT FK_Postagem_0
    FOREIGN KEY (FK_USUARIO_email, FK_USUARIO_senha)
    REFERENCES USUARIO (email, senha)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Postagem ADD CONSTRAINT FK_Postagem_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Escreveu ADD CONSTRAINT FK_Escreveu_0
    FOREIGN KEY (FK_AUTOR_codigo)
    REFERENCES AUTOR (codigo)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Escreveu ADD CONSTRAINT FK_Escreveu_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

## Marco de Entrega 02 em: (16/06/2018)<br>
### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (30/06/2018)
<br>

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
>## Marco de Entrega 04/Entrega Final em: (Data definida no cronograma)<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


        
        


    





