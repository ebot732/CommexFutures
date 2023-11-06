# CommexFutures

Trading bot for Commex exchange.

Бот для торговли на криптобирже Commex фьючерсами USDT Perpetual (аналог BinFutures-20).

Запуск бота на VPS с ubuntu

1. Подключаемся к серверу и по умолчанию находимся в корневом каталоге.
2. Создаем новую папку (например, с именем CommexFutures) командой:
   mkdir CommexFutures
3. Создаём новую screen-сессию (назовем, например, тоже CommexFutures) для бота командой:
   screen -S CommexFutures
4. Заходим в папку CommexFutures командой:
   cd CommexFutures
5. Скачиваем бота в папку CommexFutures командой:
   wget https://github.com/ebot732/CommexFutures/releases/download/CommexFutures-20/CommexFutures-20
6. Даём права на запуск бота командой:
   chmod 755 CommexFutures-20
7. Запускаем бота командой:
   ./CommexFutures-20
    и следуем подсказкам.
8. Выходим из работающего screen, не прерывая его работу, командой:
    ctrl+a, d (при нажатой ctrl жмем а, отпускаем их, и затем жмем d)

Далее, чтобы зайти в screen работающего бота, введите команду:
screen -x CommexFutures
То есть, второй раз вводить
screen -S CommexFutures
не нужно, а то создастся еще одна screen-сессия.
