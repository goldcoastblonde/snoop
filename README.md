Snoop Project
=============

## Snoop Project один из самых перспективных OSINT-инструментов по поиску никнеймов.
- [X] This is the most powerful software taking into account the CIS location.

<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/snoop.png" />

Is your life slideshow? Ask Snoop.  
Snoop project is developed without taking into account the opinions of the NSA and their friends,  
that is, it is available to the average user.  

Snoop — это исследовательская работа (собственная база данных/закрытые багбаунти)  
в области поиска и обработки публичных данных в сети интернет.  
По части специализированного поиска Snoop способен конкурировать с традиционными поисковыми системами.  

Сравнение индексаций БД-никнеймов подобных инструментов:  
Snoop **~1500** сайтов;  
Spiderfoot **~350** сайтов;  
Sherlock **~350** сайтов;  
Whatsmyname **~290** сайтов;  
Namechk **~100** сайтов.  

| Платформа             | Поддержка |
|-----------------------|:---------:|
| GNU/Linux             |     ✅    |
| Windows 7/10 (32/64)  |     ✅    |
| Android (Termux)      |     ✅    |
| macOS                 |     ❗️    |
| IOS                   |     🚫    |
| WSL                   |     🚫    |  

Snoop for OS Windows and GNU/Linux
==================================

**Snoop Local database**
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/snoop_run.png" />  
[Snoop Full version database 1500+ websites ⚡️⚡️⚡️](https://github.com/snooppr/snoop/blob/master/websites.md "Database Snoop")    

## Релиз/Release
snoop.exe (for Windows) and snoop (for GNU/Linux)  
https://github.com/snooppr/snoop/releases  

**RU**: Snoop поставляется готовыми сборками (релиз) и не требует зависимостей (библиотек) или установки python3,
то есть работает на чистой машине с OS Windows или GNU/Linux.  
**EN**: Snoop comes with ready-made assemblies (release) and does not require dependencies (libraries) or python3 installation, that is, it runs on a clean machine with OS Windows or GNU/Linux.  
 
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/Run.gif"/>  

Snoop Project Plugins
=====================

## 1. Demonstration of one of the methods in the Plugin — [GEO_IP/domain]  
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/GEO_IP.gif" />  

**Reports are also available in csv/txt/CLI/maps**  
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/GEO_IPcsv.jpeg" />  

## 2. Demonstration of one of the methods in the Plugin — [Yandex_parser]  
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/Yandex_parser.gif" />  

**Search report dozen username (Plugin — Yandex_parser)**  
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/Yandex_parser 4.png" />  

## 3. Demonstration of one of the methods in the Plugin — [Reverse Vgeocoder]  
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/RVG.gif" /> 

<details>
<summary>Использование/Using</summary>  

**English version — of Snoop see release (available 'Snoop EN version').**
```
$ python3 snoop.py --help

usage: snoop.py [-h] [--donate y] [--version] [--verbose] [--base]
                [--web-base] [--site] [--time-out] [--found-print] [--no-func]
                [--userload] [--list all] [--country] [--save-page]
                [--cert-on] [--normal] [--module y] [--update y]
                USERNAMES [USERNAMES ...]

Snoop: поиск никнейма по всем фронтам! (Version :: Source 1.2.9_rus Snoop for GNU/Linux)

positional arguments:
  USERNAMES             Никнейм разыскиваемого пользователя, поддерживается
                        несколько имён

optional arguments:
  -h, --help            show this help message and exit
  --donate y, -d y      Пожертвовать на развитие Snoop. Приобрести full version
  --version,--about, -V НАЧАЛО! Вывод на печать версий: OS; Snoop;
                        Python и Лицензии
  --verbose, -v         Во время поиска 'username' выводить на печать
                        подробную вербализацию
  --base , -b           Указать для поиска 'username' другую БД (Локально)
  --web-base, -w        Подключиться для поиска 'username' к обновляемой
                        web_БД (Online)
  --site , -s           Указать имя сайта из БД '--list all'. Поиск 'username'
                        на одном указанном ресурсе
  --time-out , -t 9     Установить выделение макс.времени на ожидание ответа
                        от сервера (секунды). Влияет на продолжительность
                        поиска. Влияет на 'Timeout ошибки:'Вкл. эту опцию
                        необходимо при медленном интернет соединении, чтобы
                        избежать длительных зависаний при неполадках в сети
                        (по умолчанию значение выставлено 9с)
  --found-print, -f     Выводить на печать только найденные аккаунты
  --no-func, -n         ✓Монохромный терминал, не использовать цвета в url
                        ✓Отключить звук ✓Запретить открытие web browser-а
                        ✓Отключить вывод на печать флагов стран ✓Отключить
                        индикацию и статус прогресса. Экономит ресурсы системы
                        и ускоряет поиск
  --userload , -u       Указать файл со списком user-ов. Пример, 'snoop -u
                        ~/snoop/listusers.txt start'
  --list all            Вывести на печать информацию о локальной базе данных
                        Snoop
  --country, -c         Сортировка 'вывода на печать/запись_результатов' по
                        странам, а не по алфавиту
  --save-page, -S       Сохранять найденные странички пользователей в
                        локальные файлы
  --cert-on, -C         Вкл проверку сертификатов на серверах. По умолчанию
                        проверка сертификатов на серверах отключена, что даёт
                        меньше ошибок и больше положительных результатов при
                        поиске username
  --normal, -N          Переключатель режимов: SNOOPninja > нормальный режим >
                        SNOOPninja. По_умолчанию (GNU/Linux Full Version) вкл
                        'режим SNOOPninja': ускорение поиска ~25pct, экономия
                        ОЗУ ~50pct, повторное 'гибкое' соединение на сбойных
                        ресурсах. Режим SNOOPninja эффективен только
                        для Snoop for GNU/Linux Full Version. По_умолчанию
                        (Windows) вкл 'нормальный режим'
  --module y, -m y      OSINT поиск: используя различные плагины Snoop (список
                        плагинов будет пополняться)
  --update y            Обновить исходный код Snoop
```

**Example**
```
# Для поиска только одного пользователя:
$ python3 snoop.py username1 #Running from source
$ snoop username1 #Running from release
# Или, например, кириллица поддерживается:
$ python3 snoop.py олеся #Running from source
# Для поиска имени, содержащего пробел:
$ snoop "ivan ivanov" #Running from release
$ snoop ivan_ivanov #Running from release
$ snoop ivan-ivanov #Running from release

# Запуск на OS Windows:
$ python snoop.py username1 #Running from source
$ snoop.exe username1 #Running from release
# Для поиска одного и более юзеров:
$ snoop.exe username1 username2 username3 username4 #Running from release

# Поиск множества юзеров — сортировка вывода результатов по странам;
# избежание зависаний на сайтах (чаще 'мёртвая зона' зависит от вашего ip-адреса);
# выводить на печать только найденные аккаунты; сохранять странички найденных
# аккаунтов локально; указать файл со списком разыскиваемых аккаунтов;
# подключиться для поиска к расширяемой и обновляемой web-base Snoop:
$ snoop -с -t 6 -f -S -u ~/file.txt -w start #Running from release
# проверить базу данных Snoop:
$ snoop --list all #Running from release
# распечатать справку по функциям Snoop:
$ snoop --help #Running from release

# Задействовать плагины Snoop:
$ snoop --module y #Running from release

# 'ctrl-c/z' — прервать поиск #не рекомендуется прерывать таким образом поиск в режиме 'SNOOPnina'.
$ kill $(ps aux | grep python/snoop | awk '{print $2}') #лекарство для разгрузки ОЗУ при прерываниях.
```
Найденные учетные записи будут храниться в ~/snoop/results/*/username.{txt.csv.html}.  
Для доступа браузера к результатам поиска на платформе Android требуются рут права.  
csv открывать в *office в кодировке **utf-8**, разделитель полей **запятая**.  

Уничтожить **все** результаты поиска — удалить каталог '~/snoop/results'.  

```
# Обновляйте Snoop для тестирования новых функций в ПО:
$ python3 snoop.py --update y #Требуется установка Git.
```
</details>  

<details>
<summary>Самостоятельная сборка ПО из исходного кода/Self-build software from source</summary>  

**Native Installation**  
Примечание: Требуемая версия python 3.7 либо 3.8.

```
# Клонировать репозиторий
$ git clone https://github.com/snooppr/snoop

# Войти в рабочий каталог
$ cd ~/snoop

# Установить python3 и python3-pip, если они не установлены
$ apt-get update && apt-get install python3 python3-pip

# Установить зависимости 'requirements'
$ pip install --upgrade pip
$ python3 -m pip install -r requirements.txt
# Либо установить все зависимости из 'requirements.txt' в ручную через
$ pip3 install module
# Если вместо флагов стран отображаются спецсимволы, доставить пакет шрифта, например монохромный
$ apt-get install ttf-ancient-fonts или цветной apt-get install fonts-noto-color-emoji
# На OS Windows использовать cmd или powershell (на выбор по удобству), но не WSL!
```
</details>

<details>
<summary>Snoop for Android</summary>  
search username
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/snoopandroid.png" />  

plugins
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/Snoop_termux.plugins.png" />  

**Native Installation**  

Установить [Termux](https://play.google.com/store/apps/details?id=com.termux&hl=en "Google Play")  
```
# Примечание: установка Snoop на Termux продолжительная по времени
# Войти в домашнюю папку Termux (т.е. просто открыть Termux)
$ termux-setup-storage
$ ls #/data/data/com.termux/files/home # дефолтный/домашний каталог

# Установить python3 и зависимости
$ apt update && pkg upgrade && pkg install python libcrypt libxml2 libxslt git
$ pip install --upgrade pip

# Клонировать репозиторий
$ git clone https://github.com/snooppr/snoop -b snoop_termux
# (Если флешкa FAT (ни ext4), в таком случае,
# клонировать репозиторий только в ДОМАШНЮЮ директорию Termux)

# Войти в рабочий каталог Snoop
$ cd ~/snoop
# Установить зависимости 'requirements'
$ python3 -m pip install -r requirements.txt


# Дополнение для устаревших гаджетов (Android 6)
# Примечание на современных гаджетах пакеты уже предустановлены и настроены
# добавьте любое 'рандомное' имя и почту:
$ git config --global user.email "you@example.com"
$ git config --global user.name "username"
# Установите coreutils
$ pkg install coreutils
```
</details>

<details>
<summary>Основные ошибки/Basic errors in</summary>

|  Сторона  |                         Проблема                      | Решение |
|:---------:| ------------------------------------------------------|:-------:|
| ========= |=======================================================| ======= |
| Клиент    |Блокировка соединения проактивной защитой (*Kaspersky) |    1    |
|           |Недостаточная скорость интернет соединения EDGE / 3G   |    2    |
|           |Слишком низкое значение опции '-t'                     |    2    |
|           |недопустимое username                                  |    3    |
|           |Ошибки соединения: [GipsysTeam; RamblerDaing]          |    7    |
|           |Ошибки соединения: [Virtualireland; Ddo; Mamochki]     |    7    |
| ========= |=======================================================| ======= |
| Провайдер |Internet Censorship                                    |    4    |
| ========= |=======================================================| ======= |
| Сервер    |Cайт изменил свой ответ/API; обновился CF/WAF          |    5    |
|           |Блокировка сервером диапазона ip-адресов клиента       |    4    |
|           |Срабатывание/защита ресурса captch-ей                  |    4    |
|           |Некоторые сайты временно недоступны, технические работы|    6    |
| ========= |=======================================================| ======= |

Решения:
1. Перенастроить свой Firewall (например, Kaspersky блочит Ресурсы для взрослых).

2. Проверить скорость своего интернет соединения:  
$ python3 snoop.py -v username  
Если какой-либо из параметров сети выделен красным цветом, Snoop может подвисать во время поиска.  
При низкой скорости увеличить значение 'x' опции '--time-out x':  
$ python3 snoop.py -t 15 username  

3. Фактически это не ошибка. Исправить username  
(например, на некоторых сайтах недопустимы символы кириллицы; "пробелы"; или 'вьетнамо-китайская_кодировка'
в именах пользователей, в целях экономии времени: — запросы фильтруются).

4. **Сменить свой ip-адрес**  
("Серый" ip и цензура - самое частое из-за чего пользователь получает ошибки пропуска/ложного срабатывания/и в некоторых случаях '**Увы**'.  
При использовании Snoop с IP адреса провайдера мобильного оператора скорость **может** упасть в разы, зависит от провайдера.  
Например, самый действенный способ решить проблему — **ИСПОЛЬЗОВАТЬ VPN**, Tor не очень хорошо подходит для данной задачи.  
Правило: одного сканирования с одного ip недостаточно для получения максимальной отдачи от Snoop).

5. Открыть в Snoop репозитории на Github-e Issue/Pull request  
(сообщить об этом разработчику).

6. Не обращать внимание, сайты иногда уходят на ремонтные работы и возвращаются в строй.

7. [Проблема](https://wiki.debian.org/ContinuousIntegration/TriagingTips/openssl-1.1.1 "проблема простая и решаемая") с openssl в некоторых дистрибутивах GNU/Linux.  
Решение:
```
$ sudo nano /etc/ssl/openssl.cnf

# Изменить в самом низу файла строки:
[MinProtocol = TLSv1.2]
на
[MinProtocol = TLSv1]

[CipherString = DEFAULT@SECLEVEL=2]
на
[CipherString = DEFAULT@SECLEVEL=1]
```
</details>

<details>
<summary>Дополнительная информация/Additional information</summary>

[История развития проекта/History](https://raw.githubusercontent.com/snooppr/snoop/master/changelog.txt "Project development history")  

[Лицензия Snoop Project/License](https://github.com/snooppr/snoop/blob/master/COPYRIGHT)  

[Документация/Documentation](https://drive.google.com/open?id=12DzAQMgTcgeG-zJrfDxpUbFjlXcBq5ih)  

**Отпечаток публичного ключа:**	[076DB9A00B583FFB606964322F1154A0203EAE9D](https://raw.githubusercontent.com/snooppr/snoop/master/PublicKey.asc "pgp key")  

**Информация для госслужащих:** Snoop Project включен в реестр отечественного ПО. Приказ Минкомсвязи РФ №515 реестровый № 7012.  

**Snoop неидеален: вэб-сайты падают; закрывающие теги отсутсвуют; хостинги вовремя не оплачиваются. Время от времени необходимо следить за всем этим "Web rock 'n' roll", поэтому донаты приветствуются:**  
[Примеры коррекции БД/Example close/bad websites](https://drive.google.com/file/d/1CJxGRJECezDsaGwxpEw34iJ8MJ9LXCIG/view?usp=sharing)
**BTC (donation):** 1Ae5uUrmUnTjRzYEJ1KkvEY51r4hDGgNd8  

**email:** snoopproject@protonmail.com
</details>
<img src="https://raw.githubusercontent.com/snooppr/snoop/master/images/zvezda.png" />
