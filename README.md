# CommexFutures

Trading bot for Commex exchange.

Бот для торговли на криптобирже Commex фьючерсами USDT Perpetual (аналог BinFutures-22).        
( реф ссылка для регистрации: https://accounts.commex.com/en/register?ref=NUC4IQEU )


   Бот может работать в одном из 4-х режимов:
1.  Режим стандартный- перебор пар для выбора подходящей по всем заданным условиям: 
  - объем торгов за 24 часа в USDT больше указанного в настройках;
  - объем торгов последней свечи или предпоследней больше объема выбранной дальней свечи на %, указанный в настройках;
  - изменение текущей цены по отношению к цене открытия дальней свечи:
    с подрежимом delta_start1- при LONG рост цены больше, чем на указанный %,
                             - при SHORT падение цены еще больше, чем на указанный %,
    с подрежимом delta_start2- при LONG падение цены еще больше, чем на указанный %,
                             - при SHORT рост цены больше, чем на указанный %.
  
2. Режим super_asset: бот работает с парой без каких-либо условий до отключения.

3. Режим control_auto: выбор подходящей пары заданным условиям стандартного режима и работа с ней до истечения указанного таймера от старта позиции в этом режиме, или достижения стоп_цены (изменения на указанный % от цены старта).

4. Режим most_changed- перебор пар для выбора подходящей по следующим условиям: 
  - объем торгов за 24 часа в USDT больше указанного в настройках,
  - курс пары за последние 24 часа изменился в заданном коридоре (с выбором ближе к максимальному или минимальному значению коридора).
  
    Режимы super_asset, control_auto и most_changed взаимоисключающие, т.е. при выборе одного из режимов другие режимы отключаются. Если не выбран ни один из режимов, бот будет работать в стандартном режиме.
   Подробнее смотри в описании BinFutures.

Запуск бота на VPS с ubuntu

1. Подключаемся к серверу и по умолчанию находимся в корневом каталоге.
2. Создаем новую папку (например, с именем CommexFutures) командой:
   mkdir CommexFutures
3. Создаём новую screen-сессию (назовем, например, тоже CommexFutures) для бота командой:
   screen -S CommexFutures
4. Заходим в папку CommexFutures командой:
   cd CommexFutures
5. Скачиваем бота в папку CommexFutures командой:
   wget https://github.com/ebot732/CommexFutures/releases/download/CommexFutures-22/CommexFutures-22
6. Даём права на запуск бота командой:
   chmod 755 CommexFutures-22
7. Запускаем бота командой:
   ./CommexFutures-22
    и следуем подсказкам.
8. Выходим из работающего screen, не прерывая его работу, командой:
    ctrl+a, d (при нажатой ctrl жмем а, отпускаем их, и затем жмем d)

Далее, чтобы зайти в screen работающего бота, введите команду:
screen -x CommexFutures
То есть, второй раз вводить
screen -S CommexFutures
не нужно, а то создастся еще одна screen-сессия.
