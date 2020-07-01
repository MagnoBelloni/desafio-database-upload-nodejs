# desafio-conceitos-nodejs-rocketseat
<h3>Desafio do Bootcamp GoStack 11 da Rocketseat.</h3>

Backend de uma aplicação que deve armazenar transações financeiras de entrada e saída e permitir o cadastro e a listagem dessas transações, além de permitir a criação de novos registros no banco de dados a partir do envio de um arquivo csv.

<h2>Para rodar a aplicação</h2>
<ol>
  <li>Execute "yarn" no terminal para instalar todas as dependencias.</li>
  <li>Certifique-se de ter um banco de dados criado igual especificado no arquivo <b>ormconfig.json</b>.</li>
  <li>Execute "yarn typeorm migration:run", para realizar a criação do banco de dados</li>
  <li>Execute "yarn dev:server", para rodar a aplicação, ela ficara no endereço "http://localhost:3333/"</li>
</ol>

<h2>Para rodar os testes</h2>
<ol>
  <li>Execute "yarn" no terminal para instalar todas as dependencias.</li>
  <li>Execute "yarn test" para rodar os testes.</li>
</ol>

<h2>Rotas</h2>
<ul>
  <li><b>POST /transactions:</b> A Rota deve receber title, value, type, e category dentro do corpo da requisição, sendo o type o tipo da transação, que deve ser income para entradas (depósitos) e outcome para saídas (retiradas).</li>
  <li><b>GET /transactions:</b>  A rota deve retornar uma listagem com todas as transações que você cadastrou até agora, junto com o valor da soma de entradas, retiradas e total de crédito.</li>
  <li><b>DELETE /transactions/:id</b> A rota deleta uma transação com o id presente nos parâmetros da rota.</li>
  <li><b>POST /transactions/import:</b> A rota deve permitir a importação de um arquivo com formato .csv contendo as mesmas informações necessárias para criação de uma transação id, title, value, type, category_id, created_at, updated_at, onde cada linha do arquivo CSV deve ser um novo registro para o banco de dados, e por fim retorne todas as transactions que foram importadas para seu banco de dados.</li>
</ul>
