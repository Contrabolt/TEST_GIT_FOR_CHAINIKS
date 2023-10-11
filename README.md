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
mv что_копируем куда_копируем | переместить файл либо папку
rm имя_файла\файлов | удалить файл
rm имя_файла\файлов -v | удалить и вывести имена удаленных файлов
rm * | удалить все файлы в текущей директории

> Если вы пытаетесь удалить файлы, которые уже используются в программе или доступны только для чтения, система будет переспрашивать: «remove regular file?».

Команда | Описание
--- | --- |
rmdir имя_папки | удаление пустой папки

> Если папка не пуста, то система сообщит об этом: «Directory not empty».

Команда | Описание
--- | --- |
rm -rf | рекурсивное форсированное удаление без вопросов и предупреждений

> рекурсивное удаление означает, что будут последовательно удаляться все элементы папки, затем удалится пустая папка.

Команда | Описание
--- | --- |
команда && команда | позволяет вбивать последовательность команд если она не противоречит логике. Допустите ошибку в одной из команд и даже верные команды вначале не выполнятся!

### Шаг третий. Регистрирум себя как участника процесса контроля версий.

* Переходим в домашнюю директорию <b>cd ~</b>.
* Вводим __git config --global user.name "Ваше_имя"__. Имя или ник вводится в ковычках и на латинице. В серьезных организациях обычно вводят настоящие имена.
* Вводим  __git config --global user.name "электронная_почта"__. Аналогично вводим email личный либо корпоративный.
* Набираем __ls -a__. Должен появиться скрытый файл .gitconfig.
* Для чтения файла необходимо набрать __git config -l__ либо __cat .gitconfig__.
* Теперь эта информация будет привязываться к Вашим комментариям.

### Шаг четвертый. Создаем папку с проектом - репозиторий

* Создаем папку для репозитория. Название на латинице без пробелов. Если нужен пробел лучше заменить его на символ нижнего подчеркивания. Далеко прятать ее не нужно и вкладывать в папки с кириллицей тоже.

> если в названии папки есть пробелы, при работе с ней в командной строке нужно использовать кавычки, а это крайне не удобно!

* Переходим в созданную папку и вводим команду __git init__.
* В ответ получаем сообщение: __Initialized empty Git repository in Ваша_папка_репозитория/.git/__. Это значит, что система создала пустой Git-репозиторий __.git__ в вашей папке. В ней будет храниться вся важная информация.
* Проверьте наличие новой скрытой папки __.git__ вводом __ls -a__.
* Проверить статус созданного репозитория можно командой __git status__.
* В любое время вы можете снять статус репозитория со своей папки командой __rm -rf .git__. Она удалит папку __.git__.

### Шаг пятый. Добавляем файлы в репозиторий.

* Создайте текстовый файл в репозитории или скопируйте из другого места.
* Введите __git status__ и система отобразит новый файл красным цветом как "untracked files" (неотслеженный). 
* Приказать системе отслеживать файл можно командами: __git add имя_одного_файла__ (добавить один указанный файл); __git add --all__ (добавить все новые или измененные файлы); __git add .__ (добавить папку целиком).
* Сохранение файлов происходит с помощью команды __git commit -m ‘Ваш_коммит’__.
* После изменения старых и добавления новых файлов необходимо использовать __git add__ и __git commit__.
* Просмотреть историю коммитов можно с помощью команды __git log__. Выход из лога - кнопка __q__.

### Шаг шестой. Создаем удаленный репозиторий на github, где ранее регистрировались.

* В профиле GitHub переходим на вкладку __Repositories__. 
* Нажимаем __New__ и придумываем имя (Repository name).
* Заполняем описание (Description). Сейчас это делать не обязательно, можно вернуться позже.
* Выбираем уровень доступа. После выбора __Public__ на Ваш репозиторий по ссылке можно будет попадать без авторизации. При выборе __Private__ по ссылке будет выходить ошибка 404, необходимо авторизоваться.
* Нажимаем Create repository. Тонкую настройку можно будет произвести в любой момент.

### Шаг седьмой. Безопасность.

Для обмена данными между домашним удаленным репозиторием нам понадобится защита. Ее обеспечивает протокол SSH, который шифрует трафик. Нам потребуется сгенерировать ключи безопасности (SSH-ключи).

* Проверяем, есть ли какие-либо старые ключи у Вас в системе. Переходим в домашнюю директорию и вводим команду __ls -la .ssh/__. Если нашлись файлы с расширением __.pub__  Вы не создавали их, то удаляйте.
* Генерируем ключи командой __ssh-keygen -t ed25519 -C "email указанный при регистрации на "GitHub"__.
* В случае ошибки используем альтернативный вариант ssh-keygen -t rsa -b 4096 -C "email указанный при регистрации на "GitHub"__.
* После успешного ввода получим сообщение __Generating public/private (ed25519 либо rsa) key pair__.
* Нажимаем __Enter__. По умолчанию ключи сохраняются в домашней директории.
* Система запросит кодовую фразу. Если создавать не хотите - нажимаем __Enter__.
* Проверяем наличие созданных ключей в домашней директории __ls -a .ssh__. Должны появиться 2 файла с одинаковым названием, но у одного из них расширение __.pub__.