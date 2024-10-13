<!-- PROJECT LOGO -->
<div align="center">
   <a href="https://github.com/othneildrew/Best-README-Template">
      <img src="https://logodownload.org/wp-content/uploads/2014/12/estacio-logo-1-2048x1641.png" alt="estacio logo" width="80"                  height="80">
   </a>
    <h1 align="center"> Universidade Estácio de Sá </h1>
     <hr>
</div> 

* DESENVOLVIMENTO FULL STACK- 
* Disciplina: RPG0026  - Tirando proveito da nuvem para projetos de software.
* Semestre Letivo: 2024.1
* Repositorio Git:https://github.com/Gregdev22/Missao-4-Mundo-4

<hr>

* [EMERSON GREGORIO ALVES](https://github.com/Gregdev22) - MATRICULA: 2022.0908.4986
<hr>
 <h1 align="center"> Missão Prática | Nível 4 | Mundo 4 </h1>
 <h2 align="left" > Tirando proveito da nuvem para projetos de software </h2> 
 <h3>Microatividade 1: Criar uma Máquina Virtual(VM) no Azure </h3>
 <h3>Microatividade 2: Configurar Regras de Rede e Grupos de Segurança no Azure </h3>
 <h3>Microatividade 3: Criar um banco de dados SQL do Azure </h3>
 <h3>Microatividade 4: Conecta-se ao seu banco de dados </h3>
 <h3>Microatividade 5: CRUD em um Banco de Dados SQL do Azure </h3>
 <hr>

 <h2> :clipboard: Objetivos da Prática </h2>

* Demonstrar habilidade na criação e gerenciamento de recursos na Nuvem Azure, adquirindo conhecimento sobre a estrutura básica da plataforma Azure;
* Utilizar efetivamente o portal Azure para criar e configurar uma Máquina Virtual(VM), demonstrando compreensão dos recursos e suas funções;
* Configurar regras de rede e grupos de segurança, adquirindo conhecimento sobre a estrutura das regras de rede na Nuvem Azure;
* Importar um arquivo .bacpac para um banco de dados no Banco de Dados SQL do Azure;
* Criar e configurar um aplicativo web no Azure, demonstrando compreensão do mecanismo de hospedagem e implantação de aplicativos web.
<hr>

<h1> Códigos </h1>

* Criação e Estruturação das Tabelas:
  
``` SQL
CREATE TABLE Motoristas (DriverID INT PRIMARY KEY,Nome VARCHAR(100),CNH VARCHAR(20),Endereço VARCHAR(200),Contato VARCHAR(50));
CREATE TABLE Clients (ClientID INT PRIMARY KEY, Nome VARCHAR(100),Empresa VARCHAR(100),Endereço VARCHAR(200),Contato VARCHAR(50));
CREATE TABLE Orders (OrderID INT PRIMARY KEY,ClientID INT,DriverID INT,DetalhesPedido TEXT,DataEntrega DATE,Status VARCHAR(50),FOREIGN KEY (ClientID) REFERENCES Clients(ClientID),FOREIGN KEY (DriverID) REFERENCES Drivers(DriverID));

```
* Inserção e Gestão de Dados:

```SQL
INSERT INTO Motoristas (DriverID, Nome, CNH, Endereço, Contato) VALUES (1, ' Cauã Cláudio Filipe Cavalcanti ', ' 18.276.671-8 ', ' Rua Jonatas Batista, 201, Mafua', ' (86) 2754-8416 '), (2, ' Joana Sara Porto ', ' 42.567.195-1 ', 'Travessa Alto do Monte, 210, Planalto', ' (84) 2756-0406'), (3, ' Heloisa Bruna Nogueira', ' 13.202.243-6', 'Rua Sílvio Bussadori, 102, Centro', ' (43) 2765-1015')
INSERT INTO Clients (ClientID, Nome, Empresa, Endereço, Contato) VALUES
(1, ' Rebeca e Lívia Limpeza ME ', ' Rebeca e Lívia Limpeza ME ', 'Rua Yoshihisa Naruki, 10, Centro', ' (19) 3723-4495 '),
(2, ' Kauê e Marlene Entulhos ME ', ' Kauê e Marlene Entulhos ME ', ' Rua Professora Waldecir Amaral, 20, Jardim Nova Aparecida ', ' (16) 2768-8943 '),
(3, ' Cristiane e Joana Vidros ME ', ' Cristiane e Joana Vidros ME ', ' Rua São Vicente das Minas, 300, Jardim Nova Taboão ', ' (11) 3624-4623 ')
INSERT INTO Orders (OrderID, ClientID, DriverID, DetalhesPedido, DataEntrega, Status) VALUES
(1, 1, 1, 'Entregar 10 caixas de produtos de limpeza', '2024-03-26', 'Finalizado'),
(2, 2, 2, 'Retirar 5 Toneladas de Entulho', '2024-05-05', 'Pendente'),
(3, 3, 3, 'Entregar 10 janelas de vidro', '2024-04-05', 'Pendente')
```

* Execução e Validação de Consultas + Operações CRUD Eficientes:

```SQL
SELECT C.Nome, C.Endereço FROM Clients C JOIN Orders O ON C.ClientID = O.ClientID WHERE O.Status = 'Pendente';
SELECT C.Nome, C.Endereço FROM Clients C JOIN Orders O ON C.ClientID = O.ClientID WHERE O.Status = 'Finalizado';
SELECT M.Nome, M.CNH FROM Motoristas M
SELECT C.Nome, C.Endereço FROM Clients C
UPDATE Orders SET Status = 'Finalizado' WHERE OrderID IN (2, 3);
DELETE FROM Orders WHERE OrderID = 2;
```
<br>

<hr>
<h1>Resultados: </h1>

<br>
:triangular_flag_on_post: Microatividade 1: 
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%204.png" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2012.png" width="640" height="360">

<br>
:triangular_flag_on_post: Microatividade 2: 
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%202.png" width="640" height="360">

<br>
:triangular_flag_on_post: Microatividade 3: 
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%203.png" alt="resultado 1" width="640" height="360">


<br>
:triangular_flag_on_post: Microatividade 4: 
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%204.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2042.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2043.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2044.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2045.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2046.png" alt="resultado 1" width="640" height="360">

<br>
:triangular_flag_on_post: Microatividade 5: 
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%205.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/Microatividades/MA%2052.png" alt="resultado 1" width="640" height="360">

<br>
:triangular_flag_on_post: Misão Prática - LogiMove Transportes 

<h5>Configuração e Acesso ao Banco de Dados</h5>
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp1.png"  width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp2.png"  width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp3.png"  width="640" height="360">

<h5>Criação e Estruturação das Tabelas</h5>
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp4.png"  width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp5.png"  width="640" height="360">

<h5>Inserção e Gestão de Dados</h5>
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp6.png"  width="640" height="360">

<h5>Execução e Validação de Consultas + Operações CRUD Eficientes </h5>
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp7.png"  width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp8.png"  width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp9.png"  width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-4-Mundo-4/blob/main/LogiMoveTransportes/mp10.png"  width="640" height="360">

<br>

