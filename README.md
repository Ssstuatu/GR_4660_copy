# GR_4660

# Инструкция по работе с системой контроля версий Git

## Что такое Git?
<p style="text-align: justify;">Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённфе репозитории. Является самой популярной реализацией систем контроля версий в мире.  </p>

![Git лого](Git-logo.svg.png) 

## Подготовка репозитория
Для создания репозитория необходимо выполнять команду *git init* в папке с репозиторием. Будет создана **скрытая** папка .git.

## Создание коммитов

### Git add
Для добавления изменений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*. Для добавления всех файлов используйте команду *"git add ."*
>Более подробную информацию об этих командах можно посмотреть на [официальном сайте][def].

### Просмотр состояния репозитория

Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*.

### Создание коммитов

Для того, чтобы создать коммит (сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>". Все файлы для коммита должны быть *__ДОБАВЛЕНЫ__* и сообщение к коммиту писать *__ОБЯЗАТЕЛЬНО__*.

## Перемещение между сохранениями

Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с репозиторием следующим образом: *git checkout <номер коммита>*.

> &#9888; **Warning!**  
> Во избежание ошибок, обязательно вернитесь на конец ветки **master** (**HEAD**) с помошью команды *git checkout master*.


## Журнал изменений

Для того, чтобы посмотреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Ветки в git

### Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*.

> &#128712; **Information**  
> Для вывода списка веток изпользуйте команду *git branch*. Ветка, на которой Вы сейчас находитесь будет отмечена звёздочкой (\*).

### Слияние веток и решение конфликтов

Для того, чтобы добавить ветку в текущую ветку используется команда *git merge*. Команда будет выглядеть следующим образом: *git merge <название ветки>*.

> &#9757; **Important**  
> Важно помнить, что слияние веток происходит в ту, из которой Вы вызываете *git merge*.

Иногда, если в сливаемых ветках в одном и том же месте указаны разные данные, может возникнуть конфликт.  

![Пример конфликта VS code](merge-conflict-in-vscode.png "Пример конфликта слияния в VS Code")

В этом случае VS Code предложит Вам принять текущие (Current) изменения, входящие (Incoming) изменения, оба (Both) изменения или сравнить изменения (Compare Changes).

### Удаление веток

Для удаления ветки используется ключ *-d*. Необходимо ввести команду *git branch -d <имя ветки>*.

## Удаленный репозиторий

Работа нескольких человек над одним репозиторием. Иными словами pull request. Изменения мы можем вносить, выполнив команду *git clone <ссылка на репозиторий>*.
Далее с помощью команды *cd <имя папки в склонированном репозитории>* мы переходим к работе над файлом с удаленного репозитория.

## Краткая сводка по командам
---
|Команда|Действие|Примечание
|:-|:-:|-:
|git init|Создание репозитория|Создаётся скрытая папка .git
|git add|Добавление изменений в коммит|
|git status|Просмотр состояния репозитория|
|git commit|Создание коммита|Фиксация, сохранение, снимок изменений
|git log|Вывод всех изменений в файле|Выводится хэш коммита, автор, его e-mail, дата и время коммита
|git checkout|Перемещение между коммитами|И ветками
|git branch|Создание новой ветки|Вывод списка веток на экран
|git merge|Слияние веток|
|git clone|Клонирование существующего репозитория|
|git push|Выгрузить на удаленный репозиторий|
|git pull|Выгрузить изменения из удаленного репозитория|
|cd|поменять репозиторий|
---





[def]: https://git-scm.com/book/ru/v2/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-Git-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D1%8F