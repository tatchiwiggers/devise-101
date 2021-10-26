# INTRODUCTION

Okay pessoal, hoje começa o grande dia! Hoje é o primeiro dia do AirBnb week,
da nossa semana aribnb... o que significa que nas próximas duas semanas a rotina de 
vcs será bastante diferente.
Teremos as aulas na parte da manhã como sempre, mas essas aulas serão mais voltadas
aos features, às funcionalidades que vocês poderão ou não adicionar na aplicação
de vocês. Serão features de certa forma opcionais...
Não haverá mais fullstack challenges, podem dizer de vez agora adeus ao nosso querido
rake! como falei com vcs esses dias, vcs agora viraram gente grande - a forma de testar
nosso app é rodando nosso app. Não teremos mais challenges, o único challenge de vocês
será trabalhar, em grupo, no Markplace de vcs.

Como o marketplace vai funcionar - e por favor, TAs sintam-se livres pra dar opiniões,
dar sugestões de experiências passadas que vc ja tiveram ok?

O que eu consigo pensar no momento é relacionado aos pitches que vocês fizeram, que 
não foram votados, se não foram um MP, transforme-os em MP e tentem fazer a ideia 
funcionar! Algum TA aqui tem alguma ideia, alguma sugestão?

# AUTHENTICATION
Nos vamos utilizar o gem devise para fazer nossa autenticação em rails,
ele lida com autenticações muito bem em rails, é um gem profissional usada
na maioria dos aplicativos rails.

Aqui temos a documentação do devise, depois deem uma olhada - mas hj nos vamos 
começar com o que chamamos de 

# START WITH A RAILS MINIMAL TEMPLATE
antes, quando criavamos uma nova aplicação rails, o comando que usavamos era....
rails new (rails new precisava de simple form, a gente alterava os stylesheets pq eles não
vinham no formato certo etc...) 
então o le wagon fez dois templates... o minimal e o template com o devise ja implementado.
aconselho que vcs nessa semana pelo menos, iniciem com o minimal template para que vcs possam
aprender a implementar o devise e depois disso, pra outros projetos utilizarem o temolate com devise. 

o que esse template faz é: adiciona varios gems no gemfile como o simple form, font awesome
ele remove os stylesheets e adiciona os do le wagon, ele faz todo aquele set up que fizemos nos
ultimos dias.

# ABRIR VS CODE
- routes: so tem uma rota pra pages home
- um controller pages com um metodo home
- a view, home.html.erb

# HOW-TO

# INSTALLATION - read
initializers - eles rodam no inicio do rails s e eles são arquivos de configuração.
quando rodamos o comando devise:install ele adiciona td isso aqui ao arquivo
e fica td comentado - a ideia é o dev dar passar por esse arquivo e descomentar
o que ele acha necessario pra aplicação dele.

# CONFIGURATION - explain and do all

# INITIALIZER
MAILER SENDER EMAIL - permite que vcs enviem emails de confirmação, troca de senha etc.
Tem todo um set up pra isso então quem tiver interesse, abra ticket que a gente
ajuda voces.

# MODEL
Etnão agora vamos para o que está faltando ne? criar o model user.
para gerar o modelo do usuario, excepcionalemente vamos utilizar 
rails generate devise User ta? somente para o modelo user.

remember to migrate

# LOOK! (1) - look at documentation

# LOOK! (2) - go over routes with them

# Let's sign up!

# rails c - play with it

# ENTRANDO NO ASSUNTO DOS VIEW MAS 
# ANTES DE FALARMOS DE HELPERS E DE VAMOS FALAR DE SIGN OUT
porque agora conseguimos fazer o sign in mas nao conseuimos sign out e pra ser sincera 
nem da pra saber que estou signed in, certo? Então vamos puxar nosso tão querido
navbar o UI kit que vai fazer isso pra gente.

VAMOS CRIAR UMA PASTA SHARED NOS VIEWS e criar novo arquivo navbar
e com a magica do curl --- voila

***curl***
curl é um utilitário muito utilizado nas linhas de comando para transferir dados de ou para um servidor  sem interação do usuário. Com curl, você pode baixar ou fazer upload de dados usando  HTTP, HTTPS, SCP, SFTP e FTP e assim por diante.
***curl***

não podemos esquecer de renderizar esse arquivo aonde pessoal?
<!-- app/views/layouts/application.html.erb -->
<%= render 'shared/navbar' %>

# HELPERS
user_signed_in?
# => true / false

current_user
# => User instance / nil