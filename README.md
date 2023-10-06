# CommexFutures

trading bot for exchange Commex

Бот для торговли на криптобирже Bybit фьючерсами USDT Perpetual (аналог BinFutures-18).

Запуск бота на VPS с ubuntu

    Подключаемся к серверу и по умолчанию находимся в корневом каталоге.
    Создаем новую папку (например, с именем CommexFutures) командой:
    mkdir CommexFutures
    Создаём новую screen-сессию (назовем, например, тоже CommexFutures) для бота командой:
    screen -S CommexFutures
    Заходим в папку CommexFutures командой:
    cd CommexFutures
    Скачиваем бота в папку CommexFutures командой:
    wget https://github.com/ebot732/CommexFutures/releases/download/CommexFutures-18/CommexFutures-18
    Даём права на запуск бота командой:
    chmod 755 CommexFutures-18
    Запускаем бота командой:
    ./CommexFutures-18
    и следуем подсказкам.
    Выходим из работающего screen, не прерывая его работу, командой:
    ctrl+a, d (при нажатой ctrl жмем а, отпускаем их, и затем жмем d)

Далее, чтобы зайти в screen работающего бота, введите команду:
screen -x CommexFutures
То есть, второй раз вводить
screen -S CommexFutures
не нужно, а то создастся еще одна screen-сессия.
