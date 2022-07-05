# Звіт по роботі
інженера з метрології відділу НМЗ ГЦТО УГМЦ  
**Синящока О. М.**  
за червень 2022 р.  

### Скорочення в цьому файлі

**БД** - база даних  
**МП** - мова программування  
**ОС** - операційна система  
**ПЗ** - програмне забезпечення  
**ПК** - персональний компьютер  

## Стисло

Більшою мірою робота в цьому місяці полягала в налаштуванні робочого місця (ПК, ОС, ПЗ) для розробки БД гідрометеорологічного вимірювального обладнання та початкові роботи зі створення структури БД.
Раніше працював з власного ноутбука, але знайшовся ПК з неробочою ОС Windows. Відновити її роботу без дистрибутиву не вдалося.

## Докладно

Замість того, щоб його відправляти наявний неробочий ПК на ремонт у Центр
- **перевірив на ньому працездатність ОС Linux** за допомогою live-дистрибутива, після чого
- **встановив ОС Linux**, що дало змогу розробки БД і ПЗ безпосередньо на цьому ПК.

### Налаштування Linux

- оновлення наявного ПЗ
- налаштування робочого місця (клавіатурні розкладки, системний монітор, інші допоміжні програми, налаштування уподобань)
- налаштування робочого місця для співробітника (Мазур В.П.)
- встановлення ПЗ необхідного для роботи:
  - емулятор терміналу ([terminator](https://terminator-gtk3.readthedocs.io/en/latest/))
  - текстовий редактор коду ([sublime text](https://www.sublimetext.com/))
  - файловий менеджер ([double commander](https://doublecmd.sourceforge.io/))
  - програми порівняння коду ([meld](https://meldmerge.org/), [diffuse](http://diffuse.sourceforge.net/))
  - розподілена система керування версіями ([git](https://github.com/git/git))
  - більш зручні програми перегляду графічних документів ([gwenview](https://apps.kde.org/gwenview/), [okular](https://okular.kde.org/)) та плагіни (в т.ч. для форматів PSD, EPS)

### Налаштування засобів для тестування

- браузери ([firefox](https://www.mozilla.org/uk/firefox/new/), [opera](https://www.opera.com/), [tor browser](https://www.torproject.org/download/))
- віртуальна машина з Windows ([virtualbox](https://www.virtualbox.org))
- [Selenium IDE](https://www.selenium.dev/)
  
### Налаштування локального сайту для розробки БД

- встановлення необхідного ПЗ та налаштування:
  - [встановлення веб-сервера Apache](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04)
    - підключення модулів ([mod_python](https://modpython.org/), [mod_rewrite](https://httpd.apache.org/docs/current/mod/mod_rewrite.html), [ssi](https://olexsyn.github.io/e-note/apache/ssi/))
    - створення [самопідписаного ключа та сертифікатів OpenSSL](https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-apache-in-ubuntu-20-04)
    - конфігурація віртуального хоста ([.conf](https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps))
    - локальна конфігурація ([.htaccess](https://httpd.apache.org/docs/2.4/howto/htaccess.html))
  - [встановлення сервера баз даних MySQL](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)
    - створення адміністратора БД (доступ для адміністрування)
    - створення користувача БД (доступ для ПЗ)
  - [віртуальне середовище](https://docs.python.org/3/library/venv.html) розробки МП Python
    - встановлення необхідних бібліотек (mysql-connector, ninja2)

### Налагодження сайту в мережі Інтернет

- **реєстрація [тимчасового бескоштовного домена](https://meteo.pp.ua/)**
- **реєстрація хостинг-акаунту** на [віддаленому сервері](https://mirohost.net/ua/vps) для розміщення сайта і БД
- **реєстрація SSL-сертифікату** для безпечної передачі даних від користувача до БД
- **налаштування FTP-доступу** до сервера для завантаження коду сторінок, скриптів та ін. даних
- **налаштування SSH-доступу** для віддаленого налашування сайту, роботи з БД, запуску скриптів
- **створення БД, та користувачів**:
  - адміністратор БД (доступ до БД для адміністрування)
  - користувач БД (доступ до БД через ПЗ, що розробляється)

### Інше

- **реєстрація на GitHub [акаунту УГМЦ](https://github.com/ukrmeteo)** для зберігання, контролю та розповсюдження.
- створення/імпорт [ключів SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- створення репозиторію [опису структури БД](https://github.com/ukrmeteo/meteqdb-decs)
- ознайомлення з технічною документацією
- вирішення поточних проблем, що виникали в процесі роботи
- нотування знайдених рішень до особистої бази знань

