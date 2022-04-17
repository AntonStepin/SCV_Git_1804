# Инструкция Git
## 1. Описание Git 
Система управления версиями, созданная Линусом Торвальдсом для управления разработкой ядра Linux. Первая версия выпущена 7 апреля 2005 года.
## 2. Проверка наличия установленного Git
Для того, чтобы проверить наличие установленного Git требуется выполнить команду в терминале:
```
git version
```
после введения команды в терминале появится информация о версии установленного Git, если Git не установлен, то появится информация об ошибке.
## 3. Установка Git
Скачать Git можно с сайта https://git-scm.com/downloads
для операционных систем:
* Windows
* MacOS
* Linux/Unix

После установки требуется представиться системе через терминал путем следующих комманд:
```
git config --global user.name "Your Name"
git config --global user.email "Your@mail.com"
```
## 4. Инициализация репозитория
Для начала работы Git треуется открыть или создать папку (например в _**VSCode**_), в которой планируется работать и инициировать работу Git командой `git init`.
Далее создается файл и добавляется к отслеживанию Git командой:
```
git add "Название файла"
```
И как правило, делается первый коммит "Initial commit" для фиксации первоначальной стадии файла командой:
```
git commit -m "наименование коммита"
```
## 5. Запись изменений в репозитории
По мере работы с файлом необходимо сохранять изменения производимые в нем в обязательном порядке перед добавлением и фиксацией его новой версии:

* Сочетанием клавиш Cntr+S 
* Через интерфейс вкладки "File"
* Путем настройки функции автосохранения во вкладке "File"

Добавить файл изменения к фиксации можно следующими командами:
```
git add "Наименование файла"
```
Создать новый коммит (зафиксировать изменения) можно командой:
```
git commit -m "наименование коммита"
```
Одновременно два этих действия выполняются командой:
```
git commit -a -m "наименование коммита"
```
Посмотреть разницу между предыдущим сохранением и текущим вариантом можно командой:
```
git diff
```
## 6. Просмотр истории коммитов и перемещение между ними
Для того чтобы посмотреть всю историю коммитов требуется выполнить одну из команд:
```
git log (перечень коммитов с хеш-кодами и др. более полной информацией)
git log --oneline (перечень коммитов с сокращенной информацией)
```
Перемещение между коммитам происходит посредством команды:
```
git checkout "не менее 4 знаков хеш-кода нужного коммита"
```
Для возврата в текущий коммит используется одна из следующих команд:
```
git checkout master
git switch -
```
## 7. Ветвление в Git
Git позволяет осуществлять работу с файлом одновременно в несколько редакциях (частях) путем создания дополнительных веток к основному экземляру (чистовику), в роли которого выступает основная ветка `master` или `main`.  
### 7.1. Создание веток

### 7.2. Слияние веток

### 7.3. Конфликт при слиянии веток

## 8. Игнорирование файлов