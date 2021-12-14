# Сервер Music Player Daemon + клиент Auremo для Windows

* Music Player Daemon documentation
* Сайт MPD: https://musicpd.org
* Документация: https://mpd.readthedocs.io/en/stable/index.html
* Скачать серер MPD для Windows c этой [страницы](https://github.com/DivanX10/MPD-Server-Windows/raw/main/mpd%20server/MPD%20Server%20Windows.zip)
* Скачать клиент Auremo c этой [страницы](https://github.com/DivanX10/MPD-Server-Windows/blob/main/mpd%20client/Auremo-0.6.1-installer.exe)
* Скачать клиент Auremo с проекта [Auremo](https://code.google.com/archive/p/auremo/downloads)

> Это самосборка MPD сервера для запуска MPD на Windows. Все файлы имеются на официальном сайте [Music Player Daemon](https://musicpd.org). При желании можете сами собрать свою сборку, благо документация у Music Player Daemon есть или воспользоваться готовой сборкой, достаточно распаковать в корень диска С. Файл `mpd.exe` не является установочным, его нужно запускать через консоль CMD

***
## Подготовка к запуску MPD Server

**1)** Зарегистрировать библиотеку libmpdclient-2.dll, а после перезагрузитть компьютер. Регистрируем библиотеку командой: regsvr32 c:\mpd\Library\libmpdclient-2.dll

Про libmpdclient можно прочитать здесь https://github.com/MusicPlayerDaemon/libmpdclient
libmpdclient is a C library which implements the Music Player Daemon protocol.


**2)** Конфигурационный файлик mpd.conf с настройками MPD находится c:\mpd\data\

**3)** В папке backup находится файлик mpd(конфиг без правки).conf с описанием настроек

**4)** Музыку и плейлист закидываем в папки music и playlists

**5)** Запускать MPD можно в двух вариантах: скрытный и с отображением консоли
* файлик mpd.cmd это обычный запуск MPD
* файлик "Скрытный запуск MPD.vbs" запускает батник mpd.cmd в скрытном режиме


**6)** При первом запуске в папке c:\mpd\service\ появятся 2 файлика: database, sticker.sql, если они не появятся, то можно их скопировать из бэкапа c:\mpd\backup\service\ 


**7)** Запущенный MPD можно найти в диспетчере задач, процесс называется Music Player Daemon 0.23.5

**8)** Если по какой-то причине MPD не запустился, то запускаем MPD вручную и смотрим что нам в консоли сообщается. 
* Запускаем косноль
* Вводим в консоли cd c:\mpd и жмем Enter
* Вводим в консоли mpd data\mpd.conf и жмем Enter. Анализируем ошибку с помощью гугла


***

## Справочная информация про ошибки

**1)** После регистрации библиотеки libmpdclient-2.dll всплывет ошибка: Модуль "c:\mpd\service\libmpdclient-2.dll" загружен, но точка входа DLL RegisterServer не найдена

> Решение: спокойно игнорим и перезагружаем компьютер

***

**2)** Ошибка в консоли: decoder: Decoder plugin 'wildmidi' is unavailable: configuration file does not exist: /etc/timidity/timidity.cfg

![image](https://user-images.githubusercontent.com/64090632/146062980-ae841eb4-8564-4ff4-8380-cbadf09ae763.png)


> Решение: спокойно игнорим. Сам MPD сервер запущен и готов к работе
