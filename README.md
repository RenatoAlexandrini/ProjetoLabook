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
Sendo assim o projeto possuí uma estrutura que simula uma api de redes sociai contendo as entidades prinicipais de usuários e postgens junto com entidades complementares, de amizades, likes e comentários feita inteiramente em Typescript e SQL.
</h4>
<hr>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/231604801-2819f988-b3ac-4cda-8b69-f9201cd15635.png" width="30" height="30"/>
Como Testar
</h3>
<h4>
<img src="https://user-images.githubusercontent.com/102265620/230519105-cde9cf7d-02fe-4561-8073-38e6ad1909dd.png" width="20" height="20"/> Link do Render:

https://projeto-jemison-labook11-vylc.onrender.com

<br></br>
</h4>

```
- git clone https://github.com/RenatoAlexandrini/Projeto-LabEcommerce-Backend
- npm install
- npm run migrations
- npm run start
```
<hr>



<h2>
<img src="https://user-images.githubusercontent.com/102265620/230520548-8ad92534-3dc5-404e-a71d-e2e13313e0ee.png" width="35" height="35"/> Endpoints:
<br></br>
</h2>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/230521871-67ca7956-aa6e-4152-a991-ad3dfa981e42.png" width="30" height="30"/> Adicionar um usuário:
</h3>
<h5>
Endpoint que adiciona um novo usuário ao banco de dados, utilizando os dados passados através do "body". Não sendo permitida a falta de nenhuma das propriedades e também a criação de um usuário com o email igual a outro usuário adicionado anteriormente.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/230522729-493be4de-0665-4465-9d01-59962d7a5195.png" width="30" height="30"/> Buscar todos os usuários e compras:
</h3>
<h5>
Endpoint que não recebe nenhum tipo de parâmetro, apenas retorna um array com todos os usuários e todas as compras realizadas por ele, retornando um array de compras vazio caso o usuário não tenha realizado nenhuma compra anterior.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/230523061-210fba1e-dc0c-4e63-ada9-5f8aec3b9c68.png" width="30" height="30"/> Adicionar um produto:
</h3>
<h5>
Endpoint que adiciona um novo produto ao banco de dados, utilizando os dados passados através do "body". Não sendo permitida a falta de nenhuma das propriedades e também a criação de um produto com o nome igual a outro produto adicionado anteriormente.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/230523369-0b310ba2-78d5-40cb-b188-db824b8728dd.png" width="30" height="30"/> Buscar todos os produtos:
</h3>
<h5>
Endpoint que retorna uma lista com todos os produtos do banco de dados, podendo ser passado através de uma query um termo para busca de produtos ou uma ordenação(crescente: "ASC" ou decrescente "DESC").
Todos os parâmetros("order" e "search") são opcionais, gerando diferentes resultados, de acordo com o solicitado.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/230523740-afcc9045-9373-4e69-947b-12e88ac040b4.png" width="30" height="30"/> Adicionar uma compra:
</h3>
<h5>
Endpoint que adiciona uma nova compra ao banco de dados, utilizando os dados passados através do "body". Não sendo permitida a falta de nenhuma das propriedades e também havendo a verificação da existência do usuário e do produto pelo id informado.
</h5>

<h3>
<img src="https://user-images.githubusercontent.com/102265620/230526640-fdbb8b79-2261-404c-8939-46a2fbfa2869.png" width="30" height="30"/> Buscar compras de um usuário:
</h3>
<h5>
Endpoint que recebe o id de um usuário através do "path.params", retornando as informações deste usuário junto com as compras realizadas por ele, havendo a verificação da existência do usuário através do id informado.
</h5>

<hr>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/230520839-647a68bd-8a3d-4c4f-890f-e3edbbadcb19.png" width="30" height="30"/> Técnicas e tecnologias utilizadas
<br></br>

- ``Typescript`` <img src="https://user-images.githubusercontent.com/102265620/230519766-2b4903ad-94f7-48e7-b949-4fc981ee519d.png" width="19" height="19"/>
- ``SQL`` <img src="https://user-images.githubusercontent.com/102265620/230519864-6ee2f9d0-1377-4528-a6a1-2b19b5b75d5e.jpg" width="22" height="22"/>

</h3>
<hr>
<h3>
<img src="https://user-images.githubusercontent.com/102265620/230521150-79ed8394-6e7e-4188-80e9-d726e1500137.png" width="30" height="30"/>Autor:
</h3>

| [<img src="https://avatars.githubusercontent.com/u/102265620?v=4" width=115><br><sub>Renato Alexandrini</sub>](https://github.com/RenatoAlexandrini) | 
| :---: |

 
 
 
 
 
 
 
 
 
 <h1 align="center"><strong>Projeto Labook</b></strong></h1></div>

<h4>Projeto 
<hr>



<hr>

### Projeto Realizado por:
* Renato Alexandrini
---

<h3>Endpoinst do projeto<h3>
<h4>

:yellow_circle: Criar Usuário
>Este endpoint simula o cadastro de um novo usuário na nossa rede social.
Ele não necessita de nenhum tipo de autorização e deve receber os dados nome, email e password através do "body", fazendo a verificação dos dados como: se o email já existe um email igual no banco de dados, se o email de cadastro possui uma estrutura padrão de email (nome@provedor.com) e se a senha é considerada uma senha forte, contendo no mínimo oito caracteres, sendo eles ao menos uma letra maíscula, uma letra minúscula, um número e um caracter especial.

>Após a verificação ele deve gerar um novo usuário contendo a senha criptografada e retornando uma mensagem de sucesso, o novo usuário criado, para verificação e um token que deverá ser utilizado nos demais endpoints.
</br>

:yellow_circle: Login
>Este endpoint simula o login de um usuário, recebendo através do "body" os dados email e senha e fazendo a verificação no banco de dados, por fim retornando um token que será necessário na autenticação dos demais endpoints.

>Como as senhas no banco estão criptografadas, para facilitar o teste do projeto, dentro da pasta "migrations" existe um arquivo em JSON contendo os usuários com as senhas sem a criptografia.
</br>

:yellow_circle: Criar uma Postagem
> Este endpoint, simula a criação de um novo post, sendo necessário a adição do token no "header" para a autorização e então, através do "body" devem ser passados a url de uma imagem, uma descrição e um tipo entre "normal" e "event". sendo este tipo opcional, no caso do dado tipo estar vazio ou não existir no body, por padrão o pos terá o tipo "normal", o ID do autor do post não é adicionado ao "body", pois ele é retirado do token de autenticação do usuário.

>Este endpoint retorna uma mensagem de sucesso e o post recém criado, apenas para facilitar a visualização.
</br>

:green_circle: Buscar um Post através do ID
> Este endpoint deve receber um token no "header" e no "body" o ID de um post, ele então faz a verificação se o post existe no banco de dados e então retorna o post escolhido.
</br>

:green_circle: Buscar um Post através do tipo
>Este endpoint retorna um Post através do seu tipo("normal" ou "event"), para isso é necessário passar através do "header" o token de autenticação e o tipo através do body, como neste endpoint não existe um padrão de tipo, como o endpoint de criação, obrigatóriamente é necessário passar um dos dois tipos possíveis.

>Este endpoint retorna todos os Posts do tipo escolhdo, ordenados pela data de criação deles.
</br>

:yellow_circle: Criar uma nova amizade
>Este endpoint deve receber através do "header" o token de autenticação e o id de um outro usuário através do "body", então ele verifica se o id do usuário existe no banco de dados, verifica se o id recebido pelo "body" não é igual ao id retirado do token de autorização, verifica se a amizade entre os dois usuários já existe, para então por fim criar uma nova amizade.

>Este endpoint retorna uma mensagem de sucesso e a amizade criada, para a visualização.
</br>

:red_circle: Deletar uma amizade
>Este endpoint deve receber através do "header" o token de autenticação e o id de um outro usuário através do "body", ele verifica se a amizade entre os dois usuários já existe, então ele deleta esta relção de amizade.

>Este endpoint retorna apenas uma mensagem de sucesso na remoção da amizade.
</br>

:yellow_circle: Criar uma relação de like em um Post
>Este endpoint deve receber um token de autorização através do "header" e o ID de um post através do "body", então ele verifica se o post existe no banco de dados e se a relação de like entre o usuário e o post já existe no banco de dados, para então criar a relção.

>Este endpoint retorna uma mensagem de sucesso e a relação criada, para visualização.
</br>

:red_circle: Deletar arelação de like de um Post
>Este endpoint deve receber através do "header" o token de autenticação e o id de um post através do "body", ele verifica se já foi dado o like neste post, então ele deleta esta relção.

>Este endpoint retorna apenas uma mensagem de sucesso na remoção do like.
</br>

:yellow_circle: Criar um comentário
>Este endpoint recebe um token de autorização através do "header" e o id de um post através do "Body", ele apenas verifica se o post informado existe para então criar um comentário, não existindo nenhuma outa restrição, sendo possível o mesmo usuário comentar diversas vezes o mesmo post.

>Este endpoint retorna uma mensagem de sucesso e o comentário, para visualização.
</br>

:green_circle: Buscar os comentários de um usuário
>Endpoint que recebe através da "query" um termo então retorna todos os estudantes que possuam este termo em qualquer parte do nome ou sobrenome.
</br>

:green_circle: Buscar os ultimos Posts dos amigos do usuário
>Este endpoint recebe um token de autorização através do "header" e utiliza o ID retirado deste token para retornar os ultimos posts criados pelos amigos do usuário.
por padrão, são exibidos os cinco ultimos posts, porém é possível passar através do "body" um limite maior, sendo que se este limite for menor que cinco ou não existir o endpoint irá manter o padrão de cinco posts.
</br>

---

### Tecnologia Utilizada:
* Typescript

<img src="https://user-images.githubusercontent.com/102265620/205476749-786b35ae-cb86-44ab-bff9-4bd8833284b7.png" width="50px">

* SQL

<img src="https://user-images.githubusercontent.com/102265620/205476861-68520703-8f8b-4dc9-9336-fc7d8b4a0764.jpg" width="50px">

### Link da Documentação via Postman
https://documenter.getpostman.com/view/24755055/2s935oM4kC

### Link do Deploy através do Render
https://projeto-jemison-labook11-vylc.onrender.com
