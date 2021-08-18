# Скрипт для получения расширенной информации для A-Bot

![image](/images/main.png)

1. Установить RVM (https://rvm.io/rvm/install)
```
   gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
   \curl -sSL https://get.rvm.io | bash
```
2. Переподключиться к серверу или перезапустить терминал (если бот работает на локальном компьютере)
3. Установить ruby версии 2.6.6
```
rvm install 2.6.6
```
    При установке попросит пароль пользователя. Вводим его и нажимаем 'enter'
4. Установить gem abot-info
```
gem install abot-info
```
5. Запустить скрипт
```
abot-info

Доступные параметры:
Обязательные:
--db_path PATH: абсолютный путь до БД A-Bot

Опциональные:
--template (default или mobile): Шаблон
--add COLUMN1,COLUMN2,COLUMN3: Добавить колонки
--del COLUMN1,COLUMN2,COLUMN3: Удалить колонки
--symbols SYMBOL1,SYMBOL2,SYMBOL3: Пары монет для отобрадения курсов

Доступные колонки:
name: Названия монет
name_mobile: Название монет(без изменения по дню)
sell_up: Прибыль со сделки
sell_price: Цена продажи
max_price: Максимальная цена за 24ч.
min_price: Минимальная цена за 24ч.
current_price: Текущая цена
next_average_price: Цена следующего усреднения
current_quote: Текущая стоимость позиции, $
buy_date: Дата покупки
timer: Время с покупки
current_profit: Текущая прибыль
potential_profit: Потенциальная прибыль
current_price_perc_of_order: Текущая цена (подсчет процента от цены продажи)
max_price_perc_of_order: Максимальная цена за 24ч (подсчет процента от цены продажи)
```
Пример:
abot-info --db_path /home/ubuntu/abot/abot_db.db --symbols BTCUSDT,ETHUSDT,BNBUSDT --template default --del buy_date

6. Полезные команды
Обновления скрипта:
```
gem update abot-info
```
Удалениe:
```
gem uninstall abot-info
```
7. Для удобства использования рекомендуется запускать в отдельном screen окне.

Примечание: скрипт тестировался на 90% в торговле к USDT и при торговле в паре к другим монетам возможены неточности.
Баг репорты и предложения по улучшению принимаются в телеграм @xoen88

Если понравился проект:\
Кошелек на Binance BEP20(BSC)\
0x48e9bcb324a4a8c24b3394b830a6aae9ade3f0d0