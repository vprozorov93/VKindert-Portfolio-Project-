# VKinder - бот Вконтакте для поиска второй половинки.

Данный бот имитирует работу всем знакомого приложения Tinder на основании анкет пользователей VK.

При запуске бота пользователем, бот получает информацию о пользователе: Город, Статус, Семейное положение, Возраст и на основе этих данных подбирает анкеты пользователей VK. Пользователь может менять критерии поиска в соотвествующем меню.

При запуске поиска, бот предложит пользователю всех найденных пользователей по критерям (Город, Статус, Семейное положение, Возраст), на оценку. В случае если понравившийся человек так же отметит пользователя через бота как понравившийся, то случится Match и пользователи получат ссылки на анкеты друг друга.

Ограничений по критериям нет, кроме возраста, доступен поиск пользователей от 18 до 60 лет.

## Подготовка к запуску
Для корректной работы бота необходимо:
1. Создать БД и таблицы
2. Установить необходимые библиотеки из requirements.txt
3. Создать страницу в VK и группу, получить токен группы VK и access токент пользователя.

### Создание БД и таблиц
Бот использует CУБД PostgreSQL, установить можно по [ссылке](https://www.postgresql.org).
После установки или же если PostgreSQL уже установлен, необходимо создать базу данных и польхователя БД.
Сделать это можно с помощью скрипта который расположен в `/VKinder_database/vkinder_create_db.sql`, после создания БД запустите скрипт
`/VKinder_database/vkinder_create_table.sql` чтобы наполнить БД необходимыми таблицами.

### Установка библиотек
Выполните команду `pip install -r requirements.txt` в терминале.

### Получение токенов и регистрация в VK.
В случае если у вас уже есть страница VK - авторизуйтесь на сайте, если нет, то зарегистрируйтесь.

Получение токена группы(сообщества):
1. Создайте группу (сообщество)
2. В группе зайдите в Управление -> Работа с API. Создать ключ.
3. Включить возможность писать сообщения в группу. Управление -> Сообщения -> Сообщения сообщества: включить.
4. Настройки бота. Возможности бота: Включены 

Получение токена пользователя:
1. 11
2. 

## Описание библиотеки VKinder

### Описание модуля VKinder_main

### Описание модуля VKinder_database
