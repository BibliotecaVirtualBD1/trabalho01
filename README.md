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
https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/arquivos/Tabela_biblioteca.ods 
    
    
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
        
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/conceitual_dezembro.png "Modelo Conceitual")
    
    B) NOTACAO UML (Caso esteja fazendo a disciplina de analise)
    C) QUALIDADE 
        Garantir que a semântica dos atributos seja clara no esquema
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas
    
        
    
#### 5.1 Validação do Modelo Conceitual
    Semaforup: Christian Lopes, Gabriel Klier
    TimeBus: Mariana Polli, Kezia de Souza, Júlia Ferreira
## Marco de Entrega 01 em: (20/04/2018)<br>
#### 5.2 DECISÕES DE PROJETO
    [atributo]: [descrição da decisão]
    
    EXEMPLO:
    a) Campo endereço: em nosso projeto optamos por um campo multivalorado e composto, pois a empresa 
    pode possuir para cada departamento mais de uma localização... 
    b) justifique!

#### 5.3 DESCRIÇÃO DOS DADOS 
    [objeto]: [descrição do objeto]
    PESSOA: Tabela que armazena as informações de cada pessoa
      cod_pessoa: armazena o código identificador de cada pessoa
      nome: armazena o nome de cada pessoa
      
    USUARIO: Tabela que armazena as informações dos usuários
      email: armazena o endereço de e-mail do usuário
      senha: armazena um hash criptografado da senha do usuário
      
    CIDADE: Tabelza que armazena as cidades cadastradas no sistema
      cod_cidade: armazena o identificador da cidade
      cidade_desc: armazena o nome da cidade
    ESTADO: Tabela que armazena os estados cadastrados no sistema
      cod_estado: armazena o identificador da cidade
      estado_desc: armazena o nome do estado
    PAÍS: Tabela que armazena os países cadastrados no sistema
      cod_pais: armazena o identificador do país
      pais_desc: armazena o nome do país
      
    EVENTO: Tabela que armazena as inforações sobre o evento
    data_evento: armazena a data (dia, mês, ano) onde ocorrerá um evento
    hora_evento: armazena o horário onde ocorrerá um evento
    cod_evento: armazena o identificador do evento
    nome_evento: armazena o nome do evento
    TIPO_EVENTO: Tabela que armazena as informações sobre os tipos de evento existentes
      cod_tipo: armazena o identificador do tipo de evento
      tipo_desc: armazena o nome do tipo de evento
    
    LIVRO: Tabela que armazena as informações de cada livro
      cod_livro: armazena o identificador do livro
      nome_livro: armazena o nome do livro
    GENERO: Tabela que armazena as informações dos gêneros dos livros
      cod_genero: armazena o identificador do gênero
      genero_desc: armazena o nome do gênero
      
    POSTAGEM: Tabela que armazena as informações das postagens
      cod_postagem: armazena o identificador da postagem
      data_postagem: armazena a data em que ocorreu a postagem
      hora_postagem: armazena a hora em que ocorreu a postagem
      

>## Marco de Entrega 01 em: (12/05/2018)<br>
### 6	MODELO LÓGICO<br>
        a) inclusão do modelo lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
   ![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/logico_dezembro.png "Modelo lógico")

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas DDL 
        (criação de tabelas, alterações, etc..) 
/* Lógico_1: */

CREATE TABLE PESSOA (
    cod_pessoa int PRIMARY KEY,
    nome varchar(50),
    FK_CIDADE_cod_cidade int
);

CREATE TABLE USUARIO (
    email varchar(50),
    senha varchar(50),
    FK_PESSOA_cod_pessoa int PRIMARY KEY
);

CREATE TABLE EVENTO (
    cod_evento int PRIMARY KEY,
    nome_evento varchar(50)
);

CREATE TABLE POSTAGEM_Posta_comentario (
    cod_postagem int PRIMARY KEY,
    data_postagem date,
    hora_postagem time,
    FK_LIVRO_cod_livro int,
    FK_USUARIO_FK_PESSOA_cod_pessoa int
);

CREATE TABLE LIVRO (
    cod_livro int PRIMARY KEY,
    nome_livro varchar(50)
);

CREATE TABLE ESTADO (
    cod_estado int PRIMARY KEY,
    estado_desc varchar(50),
    FK_PAIS_cod_pais int
);

CREATE TABLE CIDADE (
    cod_cidade int PRIMARY KEY,
    cidade_desc varchar(50),
    FK_ESTADO_cod_estado int
);

CREATE TABLE PAIS (
    cod_pais int PRIMARY KEY,
    pais_desc varchar(50)
);

CREATE TABLE GENERO (
    cod_genero int PRIMARY KEY,
    genero_desc varchar(50)
);

CREATE TABLE TIPO_EVENTO (
    tipo_desc varchar(50),
    cod_tipo int PRIMARY KEY
);

CREATE TABLE Amizade (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_USUARIO_FK_PESSOA_cod_pessoa_ int
);

CREATE TABLE Comparece_evento (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_EVENTO_cod_evento int
);

CREATE TABLE Leu (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_LIVRO_cod_livro int
);

CREATE TABLE Curte (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_POSTAGEM_Posta_comentario_cod_postagem int
);

CREATE TABLE Evento_acontece (
    FK_CIDADE_cod_cidade int,
    FK_EVENTO_cod_evento int,
    data_evento date,
    hora_evento time
);

CREATE TABLE Livro_genero (
    FK_LIVRO_cod_livro int,
    FK_GENERO_cod_genero int
);

CREATE TABLE Escreve_livro (
    FK_PESSOA_cod_pessoa int,
    FK_LIVRO_cod_livro int
);

CREATE TABLE Evento_possui_tipo (
    FK_TIPO_EVENTO_cod_tipo int,
    FK_EVENTO_cod_evento int
);
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_1
    FOREIGN KEY (FK_CIDADE_cod_cidade)
    REFERENCES CIDADE (cod_cidade)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE USUARIO ADD CONSTRAINT FK_USUARIO_1
    FOREIGN KEY (FK_PESSOA_cod_pessoa)
    REFERENCES PESSOA (cod_pessoa)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE POSTAGEM_Posta_comentario ADD CONSTRAINT FK_POSTAGEM_Posta_comentario_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro);
 
ALTER TABLE POSTAGEM_Posta_comentario ADD CONSTRAINT FK_POSTAGEM_Posta_comentario_2
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa);
 
ALTER TABLE ESTADO ADD CONSTRAINT FK_ESTADO_1
    FOREIGN KEY (FK_PAIS_cod_pais)
    REFERENCES PAIS (cod_pais)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE CIDADE ADD CONSTRAINT FK_CIDADE_1
    FOREIGN KEY (FK_ESTADO_cod_estado)
    REFERENCES ESTADO (cod_estado)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Amizade ADD CONSTRAINT FK_Amizade_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Amizade ADD CONSTRAINT FK_Amizade_1
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa_)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Comparece_evento ADD CONSTRAINT FK_Comparece_evento_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Comparece_evento ADD CONSTRAINT FK_Comparece_evento_1
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Leu ADD CONSTRAINT FK_Leu_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Leu ADD CONSTRAINT FK_Leu_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Curte ADD CONSTRAINT FK_Curte_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Curte ADD CONSTRAINT FK_Curte_1
    FOREIGN KEY (FK_POSTAGEM_Posta_comentario_cod_postagem)
    REFERENCES POSTAGEM_Posta_comentario (cod_postagem)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Evento_acontece ADD CONSTRAINT FK_Evento_acontece_0
    FOREIGN KEY (FK_CIDADE_cod_cidade)
    REFERENCES CIDADE (cod_cidade)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Evento_acontece ADD CONSTRAINT FK_Evento_acontece_1
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Livro_genero ADD CONSTRAINT FK_Livro_genero_0
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Livro_genero ADD CONSTRAINT FK_Livro_genero_1
    FOREIGN KEY (FK_GENERO_cod_genero)
    REFERENCES GENERO (cod_genero)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Escreve_livro ADD CONSTRAINT FK_Escreve_livro_0
    FOREIGN KEY (FK_PESSOA_cod_pessoa)
    REFERENCES PESSOA (cod_pessoa)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Escreve_livro ADD CONSTRAINT FK_Escreve_livro_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Evento_possui_tipo ADD CONSTRAINT FK_Evento_possui_tipo_0
    FOREIGN KEY (FK_TIPO_EVENTO_cod_tipo)
    REFERENCES TIPO_EVENTO (cod_tipo)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Evento_possui_tipo ADD CONSTRAINT FK_Evento_possui_tipo_1
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
        
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
#### 8.1 DETALHAMENTO DAS INFORMAÇÕES
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físic
        b) formato .SQL
        
insert into pais values (1,'Brasil'),(2,'Estados Unidos'),(3,'França'),(4,'Japão'),(5,'Áustria');

insert into estado values (1,'Espírito Santo',1),(2,'Rio de Janeiro',1),(3,'São Paulo',1),
(4,'Indiana',2),(5,'Maine',2),(6,'Nova Iorque',2),(7,'Doubs',3),(8,'Kyoto',4),(9,'Boemia',5);

insert into cidade values (1,'Vitória',1),(2,'Serra',1),(3,'Campos',2),(4,'Campinas',3),(5,'São Paulo',3),
(6,'Indianápolis',4),(7,'Portland',5),(8,'Nova Iorque',6),(9,'Besançon',7),(10,'Kyoto',8),(11,'Praga',9);

insert into pessoa values (1,'João',1), (2,'Pedro',2), (3,'José',2), (4,'Maria',3), (5,'Joana',4), 
(6,'Mário',4),(7,'Plínio',5),(8,'Fernando',5),(9,'Rafael',5),(10,'Carlos',5),(11,'Leonardo',5),(12,'John',6),(13,'Bob',7),(14,'Fred',8),
(15,'Haru',10),(16,'Machado de Assis',3), (17,'Stephen King',7), (18,'Victor Hugo',9), (19,'Franz Kafka',11), 
(20,'Haruki Murakami',10), (21,'John Green',6), (22,'Robert Lawrence',8);

insert into usuario values ('joao@gmail',md5('batata123'),1), ('pedro@gmail',md5('paozinho123'),2), ('jose@gmail',md5('senha123'),3),
('maria@gmail',md5('maria123'),4),('joana@gmail',md5('bolo123'),5), ('mario@gmail',md5('luigi123'),6),('plinio@gmail',md5('plinio123'),7),
('fernando@gmail',md5('fer123'),8),('rafa@gmail',md5('rafa123'),9),('carlos@gmail',md5('car123'),10),('leo@gmail',md5('leo123'),11),
('john@gmail',md5('john123'),12),('bob@gmail',md5('bob123'),13),('fred@gmail',md5('fred123'),14),('haru@gmail',md5('haru123'),15);

insert into livro values (1,'Helena'), (2,'O Iluminado'), (3,'Goosebumps'), (4,'Os Miseráveis'), (5,'Dom Casmurro'), (6,'A Metamorfose'), 
(7,'Norwegian Wood'), (8,'Kafka a beira-mar'), (9,'A Culpa é das Estrelas'), (10,'Tartarugas até lá embaixo');

insert into postagem_posta_comentario values (1,'2018-02-04','12:00:00',1,1), (2,'2018-02-05','11:30:00',2,2), (3,'2018-04-06','08:45:00',3,3),
(4,'2018-05-06','18:00:00',4,3), (5,'2018-05-06','20:00:00',5,4), (6,'2018-06-07','07:00:00',6,6),(7,'2018-06-07','09:30:00',7,8),
(8,'2018-06-07','15:00:00',7,9),(9,'2018-07-07','18:00:00',7,11),(10,'2018-08-07','20:00:00',8,14);

insert into evento values (1,'Leitura Coletiva'), (2,'Encontro de Leitores'), (3,'Doação de Livros'), (4,'Livros Antigos'), (5,'Feira de livros'), 
(6,'Sebo Veredas'), (7,'Venda de livros usados');

insert into genero values (1,'Terror'), (2,'Romance'), (3,'Ficção');

insert into tipo_evento values ('Encontro',1), ('Vendas',2), ('Outros',3);

insert into leu values (1,1),(1,2),(1,3),(2,2),(2,3),(2,5),(3,4),(3,5),(3,6),(4,1),(4,2),(5,1),(5,2),(5,3),(5,6),(6,1),
(7,1),(7,2),(7,3),(7,4),(8,2),(8,7),(8,10),(9,1),(10,3),(10,4),(12,3),(12,5),(12,7),(12,9),(13,1),(13,10),(14,2),(14,3),(14,6),(14,9),(15,1),(15,2),(15,3),
(15,4),(15,5),(15,6),(15,7),(15,8),(15,9),(15,10);

insert into amizade values (1,2),(1,3),(1,4),(2,3),(2,4),(2,5),(3,4),(3,5),(3,6),(4,1),(4,2),(4,3),(4,5),(4,11),(4,13),(4,14),(5,10),(5,12),(5,15),(6,1),(6,3),
(7,1),(7,2),(7,3),(7,4),(7,5),(9,10),(9,11),(10,2),(11,12),(11,13),(11,4),(12,5),(13,7),(14,1),(14,2),(14,3),(15,6),(15,7),(15,9);

insert into comparece_evento values (1,1),(1,2),(1,3),(2,1),(2,4),(2,5),(2,6),(3,5),(4,1),(5,4),(6,1),(6,2),
(7,1),(7,3),(7,4),(8,2),(8,7),(8,1),(9,1),(10,3),(10,4),(12,3),(12,4),(12,6),(12,7),(13,1),(13,2),
(14,2),(14,3),(14,5),(14,6),(15,1),(15,2),(15,3),(15,4),(15,5),(15,6),(15,7);

insert into curte values (1,1),(1,2),(2,2),(3,1),(4,3),(4,4),(5,2),(6,2),(7,5),(7,6),(7,7),(8,1),(8,8),(9,9),(9,10),(10,5),(10,6),(10,7),
(11,3),(11,9),(12,1),(13,4),(13,5),(14,7),(14,9),(15,6),(15,8);

insert into evento_acontece values (1,1,'2019-01-01','10:00:00'), (2,2,'2019-02-01','18:00:00'), (3,3,'2019-03-04','12:00:00'), 
(5,4,'2019-05-05','11:00:00'), (6,5,'2019-08-10','15:00:00'), (7,6,'2019-01-11','19:00:00'), (7,7,'2019-09-12','20:00:00');

insert into evento_possui_tipo values (1,1),(1,2),(3,3),(3,4),(3,5),(3,6),(3,7);

insert into livro_genero values (1,2),(2,1),(3,1),(4,2),(5,2),(6,3),(7,2),(8,2),(9,2),(10,3);

insert into escreve_livro values (16,1),(16,5),(17,2),(18,4),(19,6),(20,7),(20,8),(21,9),(21,10),(22,3);

#### 8.2 INCLUSÃO DO SCRIPT PARA CRIAÇÃO DE TABELA E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (create para tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
 CREATE TABLE PESSOA (
    cod_pessoa int PRIMARY KEY,
    nome varchar(50),
    FK_CIDADE_cod_cidade int
);

CREATE TABLE USUARIO (
    email varchar(50),
    senha varchar(50),
    FK_PESSOA_cod_pessoa int PRIMARY KEY
);

CREATE TABLE EVENTO (
    cod_evento int PRIMARY KEY,
    nome_evento varchar(50)
);

CREATE TABLE POSTAGEM_Posta_comentario (
    cod_postagem int PRIMARY KEY,
    data_postagem date,
    hora_postagem time,
    FK_LIVRO_cod_livro int,
    FK_USUARIO_FK_PESSOA_cod_pessoa int
);

CREATE TABLE LIVRO (
    cod_livro int PRIMARY KEY,
    nome_livro varchar(50)
);

CREATE TABLE ESTADO (
    cod_estado int PRIMARY KEY,
    estado_desc varchar(50),
    FK_PAIS_cod_pais int
);

CREATE TABLE CIDADE (
    cod_cidade int PRIMARY KEY,
    cidade_desc varchar(50),
    FK_ESTADO_cod_estado int
);

CREATE TABLE PAIS (
    cod_pais int PRIMARY KEY,
    pais_desc varchar(50)
);

CREATE TABLE GENERO (
    cod_genero int PRIMARY KEY,
    genero_desc varchar(50)
);

CREATE TABLE TIPO_EVENTO (
    tipo_desc varchar(50),
    cod_tipo int PRIMARY KEY
);

CREATE TABLE Amizade (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_USUARIO_FK_PESSOA_cod_pessoa_ int
);

CREATE TABLE Comparece_evento (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_EVENTO_cod_evento int
);

CREATE TABLE Leu (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_LIVRO_cod_livro int
);

CREATE TABLE Curte (
    FK_USUARIO_FK_PESSOA_cod_pessoa int,
    FK_POSTAGEM_Posta_comentario_cod_postagem int
);

CREATE TABLE Evento_acontece (
    FK_CIDADE_cod_cidade int,
    FK_EVENTO_cod_evento int,
    data_evento date,
    hora_evento time
);

CREATE TABLE Livro_genero (
    FK_LIVRO_cod_livro int,
    FK_GENERO_cod_genero int
);

CREATE TABLE Escreve_livro (
    FK_PESSOA_cod_pessoa int,
    FK_LIVRO_cod_livro int
);

CREATE TABLE Evento_possui_tipo (
    FK_TIPO_EVENTO_cod_tipo int,
    FK_EVENTO_cod_evento int
);
 
ALTER TABLE PESSOA ADD CONSTRAINT FK_PESSOA_1
    FOREIGN KEY (FK_CIDADE_cod_cidade)
    REFERENCES CIDADE (cod_cidade)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE USUARIO ADD CONSTRAINT FK_USUARIO_1
    FOREIGN KEY (FK_PESSOA_cod_pessoa)
    REFERENCES PESSOA (cod_pessoa)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE POSTAGEM_Posta_comentario ADD CONSTRAINT FK_POSTAGEM_Posta_comentario_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro);
 
ALTER TABLE POSTAGEM_Posta_comentario ADD CONSTRAINT FK_POSTAGEM_Posta_comentario_2
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa);
 
ALTER TABLE ESTADO ADD CONSTRAINT FK_ESTADO_1
    FOREIGN KEY (FK_PAIS_cod_pais)
    REFERENCES PAIS (cod_pais)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE CIDADE ADD CONSTRAINT FK_CIDADE_1
    FOREIGN KEY (FK_ESTADO_cod_estado)
    REFERENCES ESTADO (cod_estado)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Amizade ADD CONSTRAINT FK_Amizade_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Amizade ADD CONSTRAINT FK_Amizade_1
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa_)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE CASCADE ON UPDATE CASCADE;
 
ALTER TABLE Comparece_evento ADD CONSTRAINT FK_Comparece_evento_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Comparece_evento ADD CONSTRAINT FK_Comparece_evento_1
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Leu ADD CONSTRAINT FK_Leu_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Leu ADD CONSTRAINT FK_Leu_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Curte ADD CONSTRAINT FK_Curte_0
    FOREIGN KEY (FK_USUARIO_FK_PESSOA_cod_pessoa)
    REFERENCES USUARIO (FK_PESSOA_cod_pessoa)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Curte ADD CONSTRAINT FK_Curte_1
    FOREIGN KEY (FK_POSTAGEM_Posta_comentario_cod_postagem)
    REFERENCES POSTAGEM_Posta_comentario (cod_postagem)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Evento_acontece ADD CONSTRAINT FK_Evento_acontece_0
    FOREIGN KEY (FK_CIDADE_cod_cidade)
    REFERENCES CIDADE (cod_cidade)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Evento_acontece ADD CONSTRAINT FK_Evento_acontece_1
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Livro_genero ADD CONSTRAINT FK_Livro_genero_0
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Livro_genero ADD CONSTRAINT FK_Livro_genero_1
    FOREIGN KEY (FK_GENERO_cod_genero)
    REFERENCES GENERO (cod_genero)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Escreve_livro ADD CONSTRAINT FK_Escreve_livro_0
    FOREIGN KEY (FK_PESSOA_cod_pessoa)
    REFERENCES PESSOA (cod_pessoa)
    ON DELETE RESTRICT ON UPDATE RESTRICT;
 
ALTER TABLE Escreve_livro ADD CONSTRAINT FK_Escreve_livro_1
    FOREIGN KEY (FK_LIVRO_cod_livro)
    REFERENCES LIVRO (cod_livro)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Evento_possui_tipo ADD CONSTRAINT FK_Evento_possui_tipo_0
    FOREIGN KEY (FK_TIPO_EVENTO_cod_tipo)
    REFERENCES TIPO_EVENTO (cod_tipo)
    ON DELETE SET NULL ON UPDATE CASCADE;
 
ALTER TABLE Evento_possui_tipo ADD CONSTRAINT FK_Evento_possui_tipo_1
    FOREIGN KEY (FK_EVENTO_cod_evento)
    REFERENCES EVENTO (cod_evento)
    ON DELETE SET NULL ON UPDATE CASCADE;
    
insert into pais values (1,'Brasil'),(2,'Estados Unidos'),(3,'França'),(4,'Japão'),(5,'Áustria');

insert into estado values (1,'Espírito Santo',1),(2,'Rio de Janeiro',1),(3,'São Paulo',1),
(4,'Indiana',2),(5,'Maine',2),(6,'Nova Iorque',2),(7,'Doubs',3),(8,'Kyoto',4),(9,'Boemia',5);

insert into cidade values (1,'Vitória',1),(2,'Serra',1),(3,'Campos',2),(4,'Campinas',3),(5,'São Paulo',3),
(6,'Indianápolis',4),(7,'Portland',5),(8,'Nova Iorque',6),(9,'Besançon',7),(10,'Kyoto',8),(11,'Praga',9);

insert into pessoa values (1,'João',1), (2,'Pedro',2), (3,'José',2), (4,'Maria',3), (5,'Joana',4), 
(6,'Mário',4),(7,'Plínio',5),(8,'Fernando',5),(9,'Rafael',5),(10,'Carlos',5),(11,'Leonardo',5),(12,'John',6),(13,'Bob',7),(14,'Fred',8),
(15,'Haru',10),(16,'Machado de Assis',3), (17,'Stephen King',7), (18,'Victor Hugo',9), (19,'Franz Kafka',11), 
(20,'Haruki Murakami',10), (21,'John Green',6), (22,'Robert Lawrence',8);

insert into usuario values ('joao@gmail',md5('batata123'),1), ('pedro@gmail',md5('paozinho123'),2), ('jose@gmail',md5('senha123'),3),
('maria@gmail',md5('maria123'),4),('joana@gmail',md5('bolo123'),5), ('mario@gmail',md5('luigi123'),6),('plinio@gmail',md5('plinio123'),7),
('fernando@gmail',md5('fer123'),8),('rafa@gmail',md5('rafa123'),9),('carlos@gmail',md5('car123'),10),('leo@gmail',md5('leo123'),11),
('john@gmail',md5('john123'),12),('bob@gmail',md5('bob123'),13),('fred@gmail',md5('fred123'),14),('haru@gmail',md5('haru123'),15);

insert into livro values (1,'Helena'), (2,'O Iluminado'), (3,'Goosebumps'), (4,'Os Miseráveis'), (5,'Dom Casmurro'), (6,'A Metamorfose'), 
(7,'Norwegian Wood'), (8,'Kafka a beira-mar'), (9,'A Culpa é das Estrelas'), (10,'Tartarugas até lá embaixo');

insert into postagem_posta_comentario values (1,'2018-02-04','12:00:00',1,1), (2,'2018-02-05','11:30:00',2,2), (3,'2018-04-06','08:45:00',3,3),
(4,'2018-05-06','18:00:00',4,3), (5,'2018-05-06','20:00:00',5,4), (6,'2018-06-07','07:00:00',6,6),(7,'2018-06-07','09:30:00',7,8),
(8,'2018-06-07','15:00:00',7,9),(9,'2018-07-07','18:00:00',7,11),(10,'2018-08-07','20:00:00',8,14);

insert into evento values (1,'Leitura Coletiva'), (2,'Encontro de Leitores'), (3,'Doação de Livros'), (4,'Livros Antigos'), (5,'Feira de livros'), 
(6,'Sebo Veredas'), (7,'Venda de livros usados');

insert into genero values (1,'Terror'), (2,'Romance'), (3,'Ficção');

insert into tipo_evento values ('Encontro',1), ('Vendas',2), ('Outros',3);

insert into leu values (1,1),(1,2),(1,3),(2,2),(2,3),(2,5),(3,4),(3,5),(3,6),(4,1),(4,2),(5,1),(5,2),(5,3),(5,6),(6,1),
(7,1),(7,2),(7,3),(7,4),(8,2),(8,7),(8,10),(9,1),(10,3),(10,4),(12,3),(12,5),(12,7),(12,9),(13,1),(13,10),(14,2),(14,3),(14,6),(14,9),(15,1),(15,2),(15,3),
(15,4),(15,5),(15,6),(15,7),(15,8),(15,9),(15,10);

insert into amizade values (1,2),(1,3),(1,4),(2,3),(2,4),(2,5),(3,4),(3,5),(3,6),(4,1),(4,2),(4,3),(4,5),(4,11),(4,13),(4,14),(5,10),(5,12),(5,15),(6,1),(6,3),
(7,1),(7,2),(7,3),(7,4),(7,5),(9,10),(9,11),(10,2),(11,12),(11,13),(11,4),(12,5),(13,7),(14,1),(14,2),(14,3),(15,6),(15,7),(15,9);

insert into comparece_evento values (1,1),(1,2),(1,3),(2,1),(2,4),(2,5),(2,6),(3,5),(4,1),(5,4),(6,1),(6,2),
(7,1),(7,3),(7,4),(8,2),(8,7),(8,1),(9,1),(10,3),(10,4),(12,3),(12,4),(12,6),(12,7),(13,1),(13,2),
(14,2),(14,3),(14,5),(14,6),(15,1),(15,2),(15,3),(15,4),(15,5),(15,6),(15,7);

insert into curte values (1,1),(1,2),(2,2),(3,1),(4,3),(4,4),(5,2),(6,2),(7,5),(7,6),(7,7),(8,1),(8,8),(9,9),(9,10),(10,5),(10,6),(10,7),
(11,3),(11,9),(12,1),(13,4),(13,5),(14,7),(14,9),(15,6),(15,8);

insert into evento_acontece values (1,1,'2019-01-01','10:00:00'), (2,2,'2019-02-01','18:00:00'), (3,3,'2019-03-04','12:00:00'), 
(5,4,'2019-05-05','11:00:00'), (6,5,'2019-08-10','15:00:00'), (7,6,'2019-01-11','19:00:00'), (7,7,'2019-09-12','20:00:00');

insert into evento_possui_tipo values (1,1),(1,2),(3,3),(3,4),(3,5),(3,6),(3,7);

insert into livro_genero values (1,2),(2,1),(3,1),(4,2),(5,2),(6,3),(7,2),(8,2),(9,2),(10,3);

insert into escreve_livro values (16,1),(16,5),(17,2),(18,4),(19,6),(20,7),(20,8),(21,9),(21,10),(22,3);
#### 8.3 INCLUSÃO DO SCRIPT PARA EXCLUSÃO DE TABELAS EXISTENTES, CRIAÇÃO DE TABELA NOVAS E INSERÇÃO DOS DADOS
        a) Junção dos scripts anteriores em um único script 
        (Drop table + Create de tabelas e estruturas de dados + dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    <b>TODAS AS CONSULTAS ATUALIZADAS ESTÃO NO JUPYTER:</b>
    PDF:
    ARQUIVO .ipynb: 
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

select * from autor<br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/autor.png "Autor")<br>
select * from evento<br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/evento.png "Evento")<br>
select * from livro<br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/livro.png "Livro")<br>
select * from pessoa<br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa.png "Pessoa")<br>
select * from postagem_posta_comentario<br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/postagem.png "Postagem")<br>
select * from usuario<br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/usuario.png "Usuário")<br>
#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
select * from pessoa where estado = 'São Paulo' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa%20where%20SP.png "Pessoa")<br>
select cod_pessoa,nome from pessoa where cod_pessoa <= 5 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa%20where%20nome.png "Pessoa")<br>
select * from livro where genero = 'Terror' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/livro%20where%20genero.png "livro")<br>
select * from evento where hora > '10:00:00' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/evento%20where%20hora.png "evento")<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
select * from pessoa where cod_pessoa > 3 and estado <> 'São Paulo' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa%20cod%20and%20estado.png)<br>
select * from usuario where fk_pessoa_cod_pessoa = 1 or fk_pessoa_cod_pessoa = 4 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/usuario%20cod%20or.png)<br>
select * from evento where not cod_evento = 1 and not cod_evento = 3 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/evento%20where%20not.png)<br>
select * from livro where genero = 'Romance' and not cod_livro = 1 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/livro%20where%20not.png)<br>
select * from pessoa where not nome = 'João' and not idade = 'Búzios' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa%20joao%20buzios.png)<br>

    b) Criar no mínimo 3 consultas com operadores aritméticos 
select * from pessoa where cod_pessoa <> 5 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa%20aritmetico.png)<br>
select * from evento where cod_evento <= 3 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/evento%20aritmetico.png)<br>
select * from usuario where fk_pessoa_cod_pessoa >= 2 <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/usuario%20aritmetico.png)<br>

    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
select * from pessoa as pes where nome <> 'Maria' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/pessoa%20renomear.png)<br>
select * from livro as book where nome_livro = 'Os Miseráveis' <br>
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/livro%20renomear.png)<br>
select * from evento as festa where nome <> 'Doação de Livros' <br> 
![Alt text](https://github.com/BibliotecaVirtualBD1/trabalho01/blob/master/imagens/prints%20tabelas/evento%20renomear.png)<br>
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


        
        


    





