# БЫСТРЫЙ СТАРТ В МИР Git !

### Система контроля версий Git позволяет:

* Работать с локальными и удаленными репозиториями, одному либо в команде
* Хранить всю историю изменений в проекте с комментариями
* Иметь множество независимых веток кода
* Определить кто из членов команды что и когда сделал
* Восстановить любую из предыдущиx версий проекта 

### Преимущества Git перед обычным резервным копированием в хранилище:

Параметры | Хранилище | Git
--- | --- | ---
Ветвление разработки | Строго линейно | Гибкая разработка
Детальная история | Отсутствует | Все файлы с комментариями
Версионирование внешних файлов | Сохранение изолированных версий | Любые файлы версионируются в одном проекте

### Шаг первый. Скачиваем и устанавливаем что надо, регистрируемся где надо.

* Переходим по [ссылке на Git] (https://git-scm.com/download/win)
Скачиваем Standalone Installer в зависимости от Вашей системы и устанавливаем.
* Переходим по [ссылке на GitHub] (https://github.com/). Проходим стандартную процедуру регистрации.

### Шаг второй. Изучаем основы работы в командной строке.

Команда | Описание
--- | --- |
pwd | показать папку, где находимся
cd ~ | перейти в домашнюю директорию
cd / | перейти в корневую директорию
cd имя_папки | перейти в указанную папку

> если в названии папки есть пробелы, при вводе нужно использовать кавычки!

Команда | Описание
--- | --- |
cd .. | перейти на уровень выше
cd ../.. | перейти на 2 уровня выше и выше аналогично 
cd . | обратиться к текущей директории
ls | вывести содержимое папки (без скрытых файлов)
ls -a | вывести расширенный список. В нём отобразятся все скрытые файлы, которые начинаются с символа .
ls -l | вывести более читабельный список, где можно будет сразу увидеть дату создания файла, его размер, автора и выданные файлу права     
ls -al | совмещает два указанных выще способа вывода
ls ~ | вывод содержимого домашней директории вне зависимости от нахождения
ls / | вывод содержимого корневой директории вне зависимости от нахождения
ls .. | вывод содержимого родительской директории
mkdir имя_папки | создать папку
mkdir имя_папки имя_папки | создать 2 папки и более аналогично
mkdir -p имя_папки/имя_папки/имя_папки | создание структуры папок (как матрешка)
touch имя_файла | создать файл
touch имя_файла имя_файла | создать 2 файла и более аналогично
cp имя_файла (который копируем) имя_папки (куда копируем) | копировать файл или файлы в указанную папку, можно сразу переименовать если ввести имя_папки/новое имя_файла
cp -r имя_папки (которую копируем) имя_папки (куда копируем) | копировать папку рекурсивно

> рекурсивное копирование означает, что папка скопируется со всем своим содержимым! 

Команда | Описание
--- | --- |
 | 

