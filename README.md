﻿# Космический Телеграм
Скрипты```fetch_eath.py fetch_nasa.py fetch_spacex.py``` скачивают фотографии через  API.
Каждый скрипт создает свою директорию в папке ```images``` .
Cкрипт ```bot.py``` публикует эти фотографии в телеграмм канале с заданным интервалом времени.

# Создание бота и добавление его в Администраторы.
Сначала вам нужно получить API Token Telegram и создать телеграмм бота.
Как это сделать?

1.  Перейти в бота: [@BotFather](https://telegram.me/BotFather).
2.  Нажать кнопку: START (Если вы ранее уже создавали ботов — перейдите к 3 пункту)
3.  Написать боту: /newbot.
4.  Бот спросит вас как назвать нового бота. Придумайте и напишите .
5.  Далее нужно ввести ник бота, что бы он заканчивался нa слово bot.
6.  Бот создан!

Далее вам нужно создать канал и добавить туда своего бота как администратора.
В [этой](https://softolet.ru/telegramm/boty/dlya-chego-delat-bota-administratorom-i-kak-eto-delaetsya.html) статье описано как это сделать. 

# Настройка скрипта.
Для работы скрипта вам нужен ```Python``` если он у вас не установлен скачайте его с [официального сайта](https://www.python.org/) и установите.

Скачайте репозиторий и запустите команду 
```python 
pip install -r requirements.txt
``` 
он установить все зависимости для программы .


Перед запуском вам нужно  изменить название ```.env.dist``` на ```.env```
Далее откройте его текстовым редактором и замените там все параметры на свои .

Для бота нужен  ```chat_id``` канала прочитайте [эту](https://lumpics.ru/how-find-out-chat-id-in-telegram/) статью и получите ```chat_id``` своего канала и замените значение ```chat_id``` в файле ```.env``` на свои.

Для скриптов  ```fetch_eath.py```и ```fetch_nasa.py``` нужен API Token от Nasa его можно получить по этому [сайту](https://api.nasa.gov/).Получив Api Token вам нужно будет Открыть файл ```.env``` и заменить значение ```NASA_TOKEN ``` своим токеном .

# Порядок запуска.
Сначала запускаете все скрипты которые скачивают фотографии только потом можно запускать ```bot.py``` он будет публиковать скачанные фотографии в канале телеграмм раз в сутки .

Время публикации можно изменить в файле ```.env```  время нужно указывать в секундах .

# Примеры запуска скриптов.
```python
python fetch_spacex.py
```

```python
python fetch_nasa.py
```

```python
python fetch_eath.py
```

```python
python bot.py
```






