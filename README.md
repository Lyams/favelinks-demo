# favelinks-demo

## Как запустить проект:

0. Скопировать проект:

```bash
git clone git@github.com:Lyams/favelinks-demo.git
cd favelinks-demo
git submodule init
git submodule update
```

1. Используем докер компоуз:

```bash
docker compose build
docker compose run backend bundle exec bin/rails db:migrate db:seed
docker compose run frontend npm install
docker compose 
docker compose up
```
многовато потратил времени на докер, в т.ч. почему-то не мог загрузить сиды заранее и какие-то траблы с npm.
Давно не настраивал его с нуля. Обещаю разобраться, в чем тут дело, но убил на него больше все времени. 

2. Открываем страницу с приложением в браузере [http://localhost:3001](localhost:3001)

3. При желании можем открыть страницу с grathiql - [http://localhost:3000/graphiql](localhost:3000)


## Что не успел:
1. Добавить тесты на фронт, донастроить линтеры.
2. Сделать CI/CA.
3. Добавить пагинацию/ленивую подгрузку на фронт списка закладок.
4. Вынести логику создания/удаления закладки в сервисы.
5. Поправить некоторые зависимости.
6. А там уже то, что предлагалось еще в задании... А потом можно добавить юзера с аутентификацией/авторизацией и т.д.
