# Инструкция по работе с Git

## Что такое Git?
Git - это наиболее популярная реализация распредеённой системы контроля версий. Наиболее полпулярной реализацией 

## Подготовка репозитория
Для создания репозитория в папке предпологаемого репозитория необходимо написать команду *git init*. Для этого в терминале с открытой папкой-репозиторем пишем *git init*

## Создание коммитов

### Добавление файлов к коммиту
Для добавления файлов к коммиту используется команда *git add*. Для того, чтобы добавить файл к новому коммиту необходимо в терминале с открытой папкой-репозиторием написать *git add <имя файла>*.

### Создание коммитов
Для создание коммитов используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git commit -m "<сообщение к коммиту>"*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***. 

## Журнал изменений
Для просмотра истории изменений используется команда *git log*. Для этого в терминале с папкой-репозиторем необходимо набрать *git log*.

## Перемещение между коммитами
Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <номер коммита>*. Номера коммитов можно посмотреть в истории коммитов, описанной в предыдущем пунткте.

## Ветки в Git

### Просмотр списка веток
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*

### Переход между ветками
Для перехода между ветками используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*.


### Создание новой ветки
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*.

## Слияние веток и разрешение конфликтов

## Удаление веток

Удаление веток можно производить путем прописывания команды 'git branch -d <название ветки, которую нужно удалить>'.

## Работа с удаленным репозиторием
| <br> Команда &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Описание      |
| :-------------------- |:-------------|
| git remote add origin [url]    |добавление связи с удаленным репозиторием 
| git branch -M main  | указываем, что основной веткой является ветка с именем main     
| git push -u origin main | отправляем текущий локальный репозиторий в удаленный репозиторий      
|git push| отправка данных на сервер при изменениях в локальном файле и при наличии текущей ветки в удаленном репозитории	
|git pull|отправка данных c сервера  в локальный репозиторий	Команда позволяет скачать все из удаленного репозитория и автоматически сделать merge с нашей локальной версией
|git fetch|подгрузить обновления из репозитория	При использовании fetch, git собирает все коммиты из целевой ветки, которых нет в текущей ветке, и сохраняет их в локальном репозитории. Однако он не сливает их в текущую ветку. Это особенно полезно, если вам нужно постоянно обновлять свой репозиторий, но вы работаете над функциональностью, неправильная реализация которой может негативно сказаться на проекте в целом. Чтобы слить коммиты в основную ветвь, нужно отдельно использовать merge.
|git push -- force|принудительная заливка данных в удаленный репозиторий после rebase (в случае появления ошибки после git push) или после squash (склеивания коммитов)