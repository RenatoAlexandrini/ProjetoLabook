<h1 align="center" >
<img src="https://user-images.githubusercontent.com/102265620/231602286-cb633643-53f6-46cc-a904-88234c02f257.png" width="40" height="40"/>
Projeto Labook
<img src="https://user-images.githubusercontent.com/102265620/231602395-78d09afe-6380-43f3-a25e-5c6b509731b0.png" width="40" height="40"/>
</h1>

![Badge Finalizado](http://img.shields.io/static/v1?label=STATUS&message=FINALIZADO&color=GREEN&style=for-the-badge)

<hr>
<h4>
<img src="https://user-images.githubusercontent.com/102265620/231603695-fc764ffd-d827-4c91-8ac3-73a0dc16322f.png" width="25" height="25"/>
O Projeto Labook tem como função, colocar em prática os conceitos de arquitetura de software, como a Arquitetura em três camadas(Data, Controller e Business), rotas com Express Router, Data Trasnfer Object(DTO), arquitetura limpa junto com a Inversão de dependências e introduzindo os conceitos de validação por token e criptografia.
</h4>
<h4>
<img src="https://user-images.githubusercontent.com/102265620/231604465-8ca9a5b5-ff6a-4e4f-b09f-ec530dc69bd7.png" width="25" height="25"/>
Sendo assim o projeto possuí uma estrutura que simula uma API de redes sociais, contendo as entidades principais de usuários e postagens junto com entidades complementares, de amizades, likes e comentários, realizado inteiramente em Typescript e SQL.
</h4>
<hr>
<h3>
  
  <img src="https://user-images.githubusercontent.com/102265620/231604801-2819f988-b3ac-4cda-8b69-f9201cd15635.png" width="35" height="35" align="center"/>
Como Testar
</h3>
<h4>
<img src="https://user-images.githubusercontent.com/102265620/231886670-84bbf853-61da-4e86-9e84-ed339e0869bb.png" width="20" height="20" align="center" /> Link da Documentação via Postman:
<br></br>
https://documenter.getpostman.com/view/24755055/2s935oM4kC
<br></br>
- Com o Postman instalado em seu computador, basta abrir a documentação e clicar no botão <img src="https://github.com/RenatoAlexandrini/LabenuSystem/assets/102265620/b4329b29-60d4-4ed4-8f94-0ca08cc866a9" width="170" height="50" align="center"/>  para testar diretamente no Postman.
<br></br>
</h4>
<h4>
<img src="https://github.com/RenatoAlexandrini/ProjetoLabook/assets/102265620/bac2c7fb-7ee2-4440-a68d-0e413a3480af" width="30" height="30" align="center"/> Para testar localmente:
</h4>


```
- inicie o Git Bash em uma pasta e digite:
- git clone https://github.com/RenatoAlexandrini/ProjetoLabook
- npm install
- npm run migrations
- npm run start
- Em cada endpoint, substitua o "https://projeto-jemison-labook11-vylc.onrender.com" por "http://localhost:3003"
```
<hr>

<h2>
<img src="https://user-images.githubusercontent.com/102265620/231631949-1cf7490b-390e-47fe-8915-545fae05a0ee.png" width="35" height="35"/> Endpoints:
</h2>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/231635312-5b4ea142-0a3d-4a85-9870-25358055770c.png" width="30" height="30"/> Criar Usuário:
</h3>
<h5>

>Este endpoint simula o cadastro de um novo usuário na nossa rede social.
Ele não necessita de nenhum tipo de autorização e deve receber os dados nome, email e password através do "body", fazendo a verificação dos dados como: se o email já existe um email igual no banco de dados, se o email de cadastro possui uma estrutura padrão de email (nome@provedor.com) e se a senha é considerada uma senha forte, contendo no mínimo oito caracteres, sendo eles ao menos uma letra maíscula, uma letra minúscula, um número e um caracter especial.

>Após a verificação ele deve gerar um novo usuário contendo a senha criptografada e retornando uma mensagem de sucesso, o novo usuário criado, para verificação e um token que deverá ser utilizado nos demais endpoints.
</h5>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/231635423-7664dcc7-bcc4-41ad-a09b-64a385052205.png" width="30" height="30"/> Login:
</h3>
<h5>


>Este endpoint simula o login de um usuário, recebendo através do "body" os dados email e senha e fazendo a verificação no banco de dados, por fim retornando um token que será necessário na autenticação dos demais endpoints.

>Como as senhas no banco estão criptografadas, para facilitar o teste do projeto, dentro da pasta "migrations" existe um arquivo em JSON contendo os usuários com as senhas sem a criptografia.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231635489-871e4cea-3994-454b-b38a-ea55aa75e199.png" width="30" height="30"/> Criar uma Postagem:
</h3>
<h5>


> Este endpoint, simula a criação de um novo post, sendo necessário a adição do token no "header" para a autorização e então, através do "body" devem ser passados a url de uma imagem, uma descrição e um tipo entre "normal" e "event". sendo este tipo opcional, no caso do dado tipo estar vazio ou não existir no body, por padrão o pos terá o tipo "normal", o ID do autor do post não é adicionado ao "body", pois ele é retirado do token de autenticação do usuário.

>Este endpoint retorna uma mensagem de sucesso e o post recém criado, apenas para facilitar a visualização.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636289-fc523a94-011c-4287-aa03-ed9fb2c9dbda.png" width="30" height="30"/> Buscar um Post através do ID:
</h3>
<h5>

> Este endpoint deve receber um token no "header" e no "body" o ID de um post, ele então faz a verificação se o post existe no banco de dados e então retorna o post escolhido.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636364-53b3a97a-c8bd-40b5-bf85-b218a8789b1a.png" width="30" height="30"/> Buscar um Post através do tipo:
</h3>
<h5>

>Este endpoint retorna um Post através do seu tipo("normal" ou "event"), para isso é necessário passar através do "header" o token de autenticação e o tipo através do body, como neste endpoint não existe um padrão de tipo, como o endpoint de criação, obrigatóriamente é necessário passar um dos dois tipos possíveis.

>Este endpoint retorna todos os Posts do tipo escolhdo, ordenados pela data de criação deles.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636415-4c8af825-d182-4126-a936-a4970e0aefff.png" width="30" height="30"/> Criar uma nova amizade:
</h3>
<h5>

>Este endpoint deve receber através do "header" o token de autenticação e o id de um outro usuário através do "body", então ele verifica se o id do usuário existe no banco de dados, verifica se o id recebido pelo "body" não é igual ao id retirado do token de autorização, verifica se a amizade entre os dois usuários já existe, para então por fim criar uma nova amizade.

>Este endpoint retorna uma mensagem de sucesso e a amizade criada, para a visualização.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636459-ad9bccfa-c50d-48e4-9ebe-4df182f5bf0d.png" width="30" height="30"/> Deletar uma amizade:
</h3>
<h5>

>Este endpoint deve receber através do "header" o token de autenticação e o id de um outro usuário através do "body", ele verifica se a amizade entre os dois usuários já existe, então ele deleta esta relção de amizade.

>Este endpoint retorna apenas uma mensagem de sucesso na remoção da amizade.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636606-2bc698d9-5a89-432e-a113-b9191ff8175e.png" width="30" height="30"/> Criar uma relação de like em um Post:
</h3>
<h5>

>Este endpoint deve receber um token de autorização através do "header" e o ID de um post através do "body", então ele verifica se o post existe no banco de dados e se a relação de like entre o usuário e o post já existe no banco de dados, para então criar a relção.

>Este endpoint retorna uma mensagem de sucesso e a relação criada, para visualização.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636642-7cac1fa4-143e-402c-ba30-a3064bf3871e.png" width="30" height="30"/> Deletar arelação de like de um Post:
</h3>
<h5>

>Este endpoint deve receber através do "header" o token de autenticação e o id de um post através do "body", ele verifica se já foi dado o like neste post, então ele deleta esta relção.

>Este endpoint retorna apenas uma mensagem de sucesso na remoção do like.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231637089-507dd3af-ae1a-4c39-9990-82891ada8769.png" width="30" height="30"/> Criar um comentário:
</h3>
<h5>

>Este endpoint recebe um token de autorização através do "header" e o id de um post através do "Body", ele apenas verifica se o post informado existe para então criar um comentário, não existindo nenhuma outa restrição, sendo possível o mesmo usuário comentar diversas vezes o mesmo post.

>Este endpoint retorna uma mensagem de sucesso e o comentário, para visualização.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636796-2d79c382-0e68-4b95-9850-2dcf2485ff96.png" width="30" height="30"/> Buscar os comentários de um usuário:
</h3>
<h5>

>Endpoint que recebe um token de autorização através do "header" e utiliza o ID do usuário contido nele para retornar todos os comentários em posts do usuário, ordenados pela data de criação.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636873-0955d2f3-741c-4e40-9c44-791d9486a953.png" width="30" height="30"/> Buscar os ultimos Posts dos amigos do usuário:
</h3>
<h5>

>Este endpoint recebe um token de autorização através do "header" e utiliza o ID retirado deste token para retornar os ultimos posts criados pelos amigos do usuário.
por padrão, são exibidos os cinco ultimos posts, porém é possível passar através do "body" um limite maior, sendo que se este limite for menor que cinco ou não existir o endpoint irá manter o padrão de cinco posts.
</h5>

<hr>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636953-10d35d2f-6dfe-4147-944c-2f3c69dfb2c5.png" width="30" height="30"/> Técnicas e tecnologias utilizadas
<br></br>

- ``Typescript`` <img src="https://user-images.githubusercontent.com/102265620/230519766-2b4903ad-94f7-48e7-b949-4fc981ee519d.png" width="19" height="19"/>
- ``SQL`` <img src="https://user-images.githubusercontent.com/102265620/230519864-6ee2f9d0-1377-4528-a6a1-2b19b5b75d5e.jpg" width="22" height="22"/>

</h3>
<hr>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/231636997-c67b108c-2dae-436b-b13a-89f5bbf3bb7d.png" width="30" height="30"/>Autor:
</h3>

| [<img src="https://avatars.githubusercontent.com/u/102265620?v=4" width=115><br><sub>Renato Alexandrini</sub>](https://github.com/RenatoAlexandrini) | 
| :---: |
