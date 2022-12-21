# Инструкция по работе с Git

## Что такое git?
***GIT*** - самая популярная реализация распределенной системы контроля версий (версинность поддерживается и на сервере, у каждого клиента). Самой распространенной реализацией ***GIT*** является (GitHub) [http://githab.com]

## Подготовка репозитория
Для создания репозитория используется команда *git init*, для этого необходимо открыть в терминале папку с будущим репозиторием и написать *git init*

## Создание коммитов

### Добавление файлов к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Используется она следующим образом: в терминале с папкой-репозиторием пишем *git add <название файла>*.

## Перемещение между коммитами
Для перемещения на другую фиксацию (коммит) используется команда *git checkout*. Для этого необходимо, как показано в прошлом пункте, в журнале изменений найти необходимый коммит и его хеш (номер), после чего в терминале с папкой-репозиторием надо написать *git checkout <хеш коммита>*. После выполнения этой команды мы попадаем в состояние **detached head**, в котором никакие следубщие команды сохранятся не будут.  Для выхода из этого состояния необходимо написать *git checkout master*. 

### Создание коммита
Для создания новой фиксации коммита используется команда *git commit*. Для этого в терминале с папкой репозитория пишем *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!!!***

## Журнал изменений
Для просмотра историй изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*

## Ветка в git
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*
* **Для проверки созданной ветки** используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch* - мы увидим, что наша ветка создалась. Но при этом, мы остаемся на главной ветке.
* **Для перехода на другую ветку**( в нашем случае созданную ветку), необходимо использовать команду *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*. После перехода на другую ветку, также можно использовать команду *git branch*, и посмотреть, что переход на нужную нам ветку осуществлен (в терминале с папкой-репозиторием перед нашей активной веткой будет стоять звездочка(*) и наименование активной ветки подвечена зеленым цветом.

##  Слияние веток и разрешение конфликтов
Для слияния веток используется команда *git merge* .  
> Изначально, мы встаем на ту ветку, в которую мержим, а в параметрах указываем ту ветку, из которой мы приносим все. 
Напомню, что переход на ветку в которую мержим используется команда *git checkout <название ветки>*, к примеру: *git checkout master*

Для слияния, в терминале с папкой репозитория пишем *git merge <название ветки из которой нужно перенести изменения>*

## Удаление веток