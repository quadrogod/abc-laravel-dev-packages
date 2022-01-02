- Create folder ../packages
- Clone repositories: 

```quadrogod/abc-cms into ../packages/Quadrogod/Abc/Cms```

```quadrogod/abc-core into ../packages/Quadrogod/Abc/Core```

```quadrogod/abc-pages into ../packages/Quadrogod/Abc/Pages```

- Run: 

```composer install```

```./vendor/bin/sail up```

Тут есть важный момент, докер сконфигурирован под работу репозитория из под докер контейнера :)
Потому, вероятно, придется временно убрать блок "repositories" и require: quadrogod/abc-cms
что бы композер, изначально правильно установил зависимости, и потом, когда докер будет запущен, 
вернуть блоки и выполнить:

```./vendor/bin/sail composer update```

Для удобства работы с sail, рекомендую добавить алиас в вашу баш-консоль:

https://laravel.com/docs/8.x/sail#configuring-a-bash-alias
