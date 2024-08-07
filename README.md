# Git

### Инициализация репозитория и коммит

**Инициализация репозитория**
 * *git init* (от англ. initialize, «инициализировать») — инициализируй репозиторий.  


**Подготовка файла к коммиту**
 1. *git add todo.txt* (от англ. add, «добавить») — подготовь файл todo.txt к коммиту;  
 2. *git add --all* (от англ. add, «добавить» + all, «всё») — подготовь к коммиту сразу все файлы, в которых были изменения, и все новые файлы;  
 3. *git add .* — подготовь к коммиту текущую папку и все файлы в ней.  


**Создание коммита**
 * *git commit -m "Комментарий к коммиту."* (от англ. commit, «совершать», «фиксировать» + message, «сообщение») — сделай коммит и оставь комментарий, чтобы было проще понять, какие изменения внесены.   


**Просмотр информации о коммитах**
 * *git log* (от англ. log, «журнал») — выведи подробную историю коммитов.  


**Просмотр состояния файлов**
 * *git status* (от англ. status, «статус», «состояние») — покажи текущее состояние репозитория.  



### Внутри коммита

**Просмотр информации о коммитах**  
 1. *git log* (от англ. log, «журнал [записей]») — выведи подробную историю коммитов;
 2. *git log --oneline* (от англ. log, «журнал [записей]» + one line, «одной строкой») — покажи краткую информацию о коммитах: сокращённый хеш и сообщение.


**Просмотр состояния файлов**
* *git status* (от англ. status, «статус», «состояние») — покажи текущее состояние репозитория.


**Добавление изменений в последний коммит**
 1. *git commit --amend --no-edit* (от англ. amend, «исправить») — добавь изменения к последнему коммиту и оставь сообщение прежним;
 2. *git commit --amend -m "Новое сообщение"* — измени сообщение к последнему коммиту на Новое сообщение.


**«Откат» файлов и коммитов**
 1. *git restore --staged hello.txt* (от англ. restore, «восстановить») — переведи файл hello.txt из состояния staged обратно в untracked или modified;
 2. *git restore hello.txt* — верни файл hello.txt к последней версии, которая была сохранена через git commit или git add;
 3. *git reset --hard b576d89* (от англ. reset, «сброс», «обнуление» + hard, «суровый») — удали все незакоммиченные изменения из staging и «рабочей зоны» вплоть до указанного коммита.


**Просмотр изменений**
 1. *git diff* (от англ. difference, «отличие», «разница») — покажи изменения в «рабочей зоне», то есть в modified-файлах;
 2. *git diff a9928ab 11bada1* — выведи разницу между двумя коммитами;
 3. *git diff --staged* — покажи изменения, которые добавлены в staged-файлах.



### Работа с ветками

**Создание веток**
 1. *git branch feature/the-finest-branch* (от англ. branch, «ветка») — создай ветку от текущей с названием feature/the-finest-branch;
 2. *git checkout -b feature/the-finest-branch* — создай ветку feature/the-finest-branch и сразу переключись на неё.


**Навигация по веткам**
 1. *git branch* — покажи, какие есть ветки в репозитории и в какой из них я нахожусь (текущая ветка будет отмечена символом *);
 2. *git branch -a* — покажи все известные ветки, как локальные (в локальном репозитории), так и удалённые (в origin на GitHub);
 3. *git checkout feature/br* — переключись на ветку feature/br.


**Сравнение веток**
 1. *git diff main HEAD* (от англ. difference, «отличие», «разница») — покажи разницу между веткой main и указателем на HEAD;
 2. *git diff HEAD~2 HEAD* — покажи разницу между тем коммитом, который был два коммита назад, и текущим.


**Удаление веток**
 1. *git branch -d br-name* — удали ветку br-name, но только если она является частью main;
 2. *git branch -D br-name* — удали ветку br-name, даже если она не объединена с main.


**Слияние веток**
* *git merge main* (от англ. merge, «сливать», «поглощать») — объедини ветку main с текущей активной веткой.


**Работа с удалённым репозиторием**
 1. *git push -u origin my-branch* (от англ. push, «толкнуть», «протолкнуть») — отправь новую ветку my-branch в удалённый репозиторий и свяжи локальную ветку с удалённой, чтобы при дополнительных коммитах можно было писать просто git push, без -u;
 2. *git push my-branch* — отправь дополнительные изменения в ветку my-branch, которая уже существует в удалённом репозитории;
 3. *git pull* (от англ. pull, «вытянуть») — подтяни изменения текущей ветки из удалённого репозитория.
