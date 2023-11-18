# Шпаргалка

## Основные команды терминала

### Навигация
* ```pwd``` (от англ. *print working directory*, «показать рабочую папку») — покажи, в какой я папке;
* ```ls``` (от англ. *list directory contents*, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;
* ```ls -a``` — покажи также скрытые файлы и папки, названия которых начинаются с символа ```.```;
* ```cd first-project``` (от англ. *change directory*, «сменить директорию») — перейди в папку ```first-project```;
* ```cd first-project/html``` — перейди в папку ```html```, которая находится в папке ```first-project```;
* ```cd ..``` — перейди на уровень выше, в родительскую папку;
* ```d ~``` — перейди в домашнюю директорию ```(/Users/Username)```;
* ```cd /``` — перейди в корневую директорию.
### Работа с файлами и папками
#### Создание
* ```touch index.html``` (англ. *touch*, «коснуться») — создай файл ```index.html``` в текущей папке;
* ```touch index.html style.css script.js``` — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;
* ```mkdir second-project``` (от англ. make *directory*, «создать директорию») — создай папку с именем ```second-project``` в текущей папке.
#### Копирование и перемещение
* ```cp file.txt ~/my-dir``` (от англ. *copy*, «копировать») — скопируй файл в другое место;
* ```mv file.txt ~/my-dir``` (от англ. *move*, «переместить») — перемести файл или папку в другое место.
#### Чтение
* ```cat file.txt``` (от англ. *concatenate and print*, «объединить и распечатать») — распечатай содержимое текстового файла ```file.txt```.
#### Удаление
* ```rm about.html``` (от англ. *remove*, «удалить») — удали файл ```about.html```;
* ```rmdir images``` (от англ. *remove directory*, «удалить директорию») — удали папку ```images```;
* ```rm -r second-project``` (от англ. *remove*, «удалить» + *recursive*, «рекурсивный») — удали папку ```second-project``` и всё, что она содержит.
### Полезные возможности
* Команды необязательно печатать и выполнять по очереди. Можно указать их списком — разделить двумя амперсандами (```&&```).
* У консоли есть собственная память — буфер с несколькими последними командами. По ним можно перемещаться с помощью клавиш со стрелками вверх (```↑```) и вниз (```↓```).
* Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать ```Tab```. Если файл или папка есть в текущей директории, командная строка допишет путь сама.
Например, вы находитесь в папке ```dev```. Начните вводить ```cd first``` и дважды нажмите ```Tab```. Если папка ```first-project``` есть внутри ```dev```, командная строка автоматически подставит её имя. Останется только нажать ```Enter```.


## Основные команды Git

Git - система контроля версий.

* ```git init``` (от англ. initialize — «инициализировать»)
* ```rm -rf .git``` Если случайно сделали Git-репозиторием не ту папку, её можно "разгитить". Для этого нужно удалить скрытую подпапку ```.git```.
- ключ ```-r``` (от англ. *recursive* — «рекурсивно») позволяет удалять папки вместе с их содержимым;
- ключ ```-f``` (от англ. *force* — «заставить») избавит вас от вопросов вроде «Вы точно хотите удалить этот файл? А этот? И этот тоже?».
* ```git status``` (от англ. *status* — «статус», «состояние») — показывает текущее состояние репозитория.
* ```git add``` (от англ. *add* — «добавить») - подготовить файлы к сохранению.
- ```--all``` (от англ. *all* — «всё») - ключ/флаг позволяет подготовить к сохранению все файлы в репозитории. <br>
Также можно добавить текущую папку целиком — в этом случае все файлы в ней тоже будут добавлены. Обратиться к текущей папке в Bash позволяет точка (```.```).
* ```git commit``` c ключом ```-m``` (от англ. *message* — «сообщение») - выполнить коммит и присвоить коммиту сообщение.
Пример: ```git commit -m ‘Мой первый коммит!’```
* ```git push``` (от англ. *push* — «толкать»). <br>
```Хеширование``` (от англ. *hash*, «рубить», «крошить», «мешанина») — это способ преобразовать набор данных. <br>
```Git``` хеширует (преобразует) информацию о коммите с помощью алгоритма **SHA-1** (от англ. *Secure Hash Algorithm* — «безопасный алгоритм хеширования») и получает для каждого коммита свой уникальный хеш — результат хеширования. <br>
Все хеши, а также таблицу соответствий ```хеш → информация о коммите``` Git хранит в папке ```.git```.
* ```git log``` (от англ. *log* — «журнал записей») - просмотр истории коммитов.
* ```--oneline``` (англ. «одной строкой») - получить сокращённый лог. <br>
Выход из просмотра логов - нажмите клавишу ```Q``` (от англ. *Quit* — «выйти») в английской раскладке клавиатуры. <br>
Файл ```HEAD``` (англ. «голова», «головной») — один из служебных файлов папки ```.git```. Он указывает на коммит, который сделан последним (то есть на самый новый). <br>
Внутри ```HEAD``` — ссылка на служебный файл: ```refs/heads/master```. Если заглянуть в этот файл, можно увидеть хеш последнего коммита. <br>
Вместо хеша последнего коммита можно написать слово ```HEAD``` — Git вас поймёт. <br>

## Основные команды Markdown

Markdown — это специальный язык разметки.

* Заголовки <br>
```# H1 — заголовок первого уровня, самый большой``` <br>
```## H2 — заголовок второго уровня, поменьше``` <br>
```### H3``` <br>
```#### H4``` <br>
```##### H5``` <br>
```###### H6 — заголовок шестого уровня, самый маленький``` <br>
* Черта <br>
```-----```
* Разрыв строки <br>
```<br>``` или конце строки поставить 2 пробела
* Новый параграф <br>
Чтобы начать новый параграф, в конце предыдущей строки должно стоять два символа переноса. Для этого нужно нажать ```Enter``` два раза.
* Выделение текста курсивом <br>
Заключить текст в ```*``` зли в ```_```
* Выделение текста полужирным шрифтом <br>
Заключить текст в ```**``` зли в ```__```
* Зачеркнуть текст <br>
Заключить текст в ```~~```
* Нумерованный список <br>
Поставить в начала строки ```цифры с точкой```
* Ненумерованный список <br>
Поставить ```*``` или ```-``` с пробелом в начале строки
* Ссылка <br>
Заключить в квадратне скобки текст, а затем указывают нужный адрес в круглых скобках.
Пример: ```[Яндекс](https://www.yandex.ru)```
* Ссылка с Тайтлом <br>
Тайтл (от англ *title* — «название», «заголовок»)
Тайтл нужно заключить в кавычки и указать внутри скобок после адреса.
Пример: ```[Яндекс](https://www.yandex.ru "Я Yandex!")```
* Код <br>
Заключить код/текст тройками косых кавычек