# ProjetoSpreadBible
Autores: Alexandre Mezack de Lima & Gustavo Laur Pisanello
--------------------------------------------//--------------------------------------------
Dados da API escolhida:

-  URL da documentação: https://github.com/marciovsena/abibliadigital/blob/master/DOCUMENTATION.md
-  URL de Acesso a API

- Métodos disponíveis / (endpoints) / Foi utilizado ou não (0 = não foi usado, 1 = foi usado): 
      - Get Books (retorna a lista de 66 livros da bíblia) / GET https://www.abibliadigital.com.br/api/books - 1
      - Get Book (retorna detalhes de um livro específico da bíblia) / GET https://www.abibliadigital.com.br/api/books/:abbrev 1
      - Get Chapter (retorna todos o versos e detalhes de um capítulo) / GET https://www.abibliadigital.com.br/api/verses/:version/:abbrev/:chapter
      - Get Verse (retorna um verso de um capítulo) / GET https://www.abibliadigital.com.br/api/verses/:version/:abbrev/:chapter/:number  
      - Get Random Verse (retorna um verso aleatório de um capítulo aleatório) / GET https://www.abibliadigital.com.br/api/verses/:version/random
      - Get Random Verse Book (retorna um verso aleatório de um livro específico) / GET https://www.abibliadigital.com.br/api/verses/:version/:abbrev/random 
      - Search by word (retorna versos com a palavra digitada como parâmetro) / POST https://www.abibliadigital.com.br/api/verses/search
      - Get Versions (retornatodas as versões da bíblia e o número de versos) / GET https://www.abibliadigital.com.br/api/versions
      
!!!!!!! Todos os métodos ACIMA não requisitam autenticação, mas, se não possuir uma, são limitadas a 20 requisições por hora !!!!!!!

      - Create Users (cria um novo usuário) / POST https://www.abibliadigital.com.br/api/users (Dados para a criação de usuário: Nome, Email e Senha) - NÃO Precisa de autenticação
      - Get User (retorna um usuário) / GET https://www.abibliadigital.com.br/api/users/:email - Precisa de autenticação
      - Get User Stats (retorna as estatísticas do usuário) / GET https://www.abibliadigital.com.br/api/users/stats - Precisa de autenticação
      - Update Token (retorna um token) / PUT https://www.abibliadigital.com.br/api/users/token - NÃO Precisa de autenticação
      - Delete User (remove um usuário) / DELETE https://www.abibliadigital.com.br/api/users - Precisa de autenticação
      - Resend User Password (Manda um email com a senha do usuário) / POST https://www.abibliadigital.com.br/api/users/password/:email - NÃO Precisa de autenticação
      
!!!!!!! Todos os métodos ABAIXO necessitam obrigatoriamente uma autenticação !!!!!!!!

      - Get Requests (retorna as requisições num período) / GET https://www.abibliadigital.com.br/api/requests/:range (mês, semana, dia)
      - Get Number Requisitions (retorna o número de requisições num período / GET https://www.abibliadigital.com.br/api/requests/amount/:range (mês, semana, dia)

- Sumário de Parâmetros desta API:
      - abbrev: abreviação do livro {Gênesis = Gn / Êxodo = Ex / Levítico = Lv / Números = Nm / Deuteronômio = Dt / Josué = Js / Samuel = Sm / Ruth = Rt / Jó = job / 
      - chapter: capítulo da bíblia
      - search: variável digitada pelo usuário como índice de busca
      - verses: verso da bíblia
      - version: versão da bíblia
      
