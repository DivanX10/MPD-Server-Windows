# Сервер Music Player Daemon + клиент Auremo для Windows

* Music Player Daemon documentation
* Сайт MPD: https://musicpd.org
* Документация: https://mpd.readthedocs.io/en/stable/index.html
* Скачать архивный файл [сервер MPD для Windows](https://github.com/DivanX10/MPD-Server-Windows/raw/main/mpd%20server/MPD%20Server%20for%20Windows.zip)
* Скачать клиент Auremo c этой [страницы](https://github.com/DivanX10/MPD-Server-Windows/raw/main/mpd%20client/Auremo-0.6.1-installer.exe)
* Скачать клиент Auremo с проекта [Auremo](https://code.google.com/archive/p/auremo/downloads)
* Интеграция []((https://github.com/AlexxIT/YandexStation#стриминг-музыки)

> Это самосборка MPD сервера для запуска MPD на Windows. Все файлы имеются на официальном сайте [Music Player Daemon](https://musicpd.org). При желании можете сами собрать свою сборку, благо документация у Music Player Daemon есть или воспользоваться готовой сборкой, достаточно распаковать в корень диска С. Файл `mpd.exe` не является установочным, его нужно запускать через консоль CMD


***
## Видеоинструкция


[![Everything Is AWESOME](https://user-images.githubusercontent.com/64090632/146078413-ac383385-f418-4ba0-a6ef-0fea29f5726e.jpg)](https://youtu.be/ZumXJ_USO4Y "Everything Is AWESOME")


***

## Подготовка к запуску MPD Server

**1)** Скачать архивный файл [MPD Server Windows.zip](https://github.com/DivanX10/MPD-Server-Windows/raw/main/mpd%20server/MPD%20Server%20for%20Windows.zip)

**2)** Распаковать папку mpd в корень диска С

**3)** Внутри папки mpd открыть конфигурационный файлик `mpd.conf` расположенный по пути `с:\mpd\data\mpd.conf` и указать желаемый порт, можно оставитть как есть

**4)** Запускаем MPD сервер через батник **mpd.cmd**, откроется окно и если будет такое сообщение, значит хорошо, значит MPD серевер запущен. не обращаем внмиание на эту ошибку. MPD запущен и работает.
![image](https://user-images.githubusercontent.com/64090632/146062980-ae841eb4-8564-4ff4-8380-cbadf09ae763.png)

**5)** Ставим клиент [Auremo](https://github.com/DivanX10/MPD-Server-Windows/raw/main/mpd%20client/Auremo-0.6.1-installer.exe) и подключаемся к MPD серверу


***

## Справочная информация

**1)** Запускать MPD можно в двух вариантах: скрытный и с отображением консоли
* файлик mpd.cmd это обычный запуск MPD
* файлик "Скрытный запуск MPD.vbs" запускает батник `mpd.cmd` в скрытном режиме

**2)** Конфигурационный файлик mpd.conf с настройками MPD находится `c:\mpd\data\`

**3)** В папке backup находится файлик mpd(конфиг без правки).conf с описанием настроек

**4)** Музыку и плейлист закидываем в папки music и playlists

**5)** При первом запуске в папке `c:\mpd\service\` появятся 2 файлика: `database, sticker.sql`, если они не появятся, то можно их скопировать из бэкапа `c:\mpd\backup\service\`

**6)** Запущенный MPD можно найти в диспетчере задач, процесс называется Music Player Daemon 0.23.5

**7)** Если по какой-то причине MPD не запустился, то запускаем MPD вручную и смотрим что нам в консоли сообщается. 
* Запускаем косноль
* Вводим в консоли `cd c:\mpd` и жмем Enter
* Вводим в консоли `mpd data\mpd.conf` и жмем Enter. Анализируем ошибку с помощью гугла




