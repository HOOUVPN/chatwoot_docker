# chatwoot_docker
Contem apenas nginx, chatwoot, pgadmin, postgres e redis

# Usando o Chatwoot com Docker

Lembrando que precisa ter o docker instalado e o docker-compose
Aconselho tambem a mudar as credencias no .env e docker-compose.yaml e for usa na internet.


Compilar o codigo

    docker-compose up --build --no-start

Apos finalizar o build, deletar as pastas data e depois recria-las data, data/postgres  data/redis.

    docker-compose run --rm rails bundle exec rails db:chatwoot_prepare

Para iniciar tudo e finalizar a instalação do chatwoot no navegador.

    docker-compose up


Lembrando que as portas

      - "8081" #Chatwoot
      - "8082" #PgAdmin

So criar uma hostname e configura no nginx ou apache para "esconder" a porta.

se for usar na internet lembrando de abrir o arquivo .env e altera o **FRONTEND_URL** colocando a url escolhida por você.
