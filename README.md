
Bash (Bourne Again Shell) — это командный интерпретатор, который является стандартной оболочкой в большинстве UNIX-подобных операционных систем, таких как Linux и macOS. Bash позволяет пользователю взаимодействовать с операционной системой, выполняя команды, скрипты и автоматизируя задачи.

Основные функции Bash:

Выполнение команд: позволяет выполнять команды, например, создание, копирование или удаление файлов.
Автоматизация задач: написание скриптов для автоматизации повторяющихся задач.
Управление процессами: запуск и управление процессами.
Обработка ввода/вывода: работу с потоками данных, перенаправление вывода и ввода.
Переменные и параметры: использование переменных для хранения значений и параметров команд.
Условия и циклы: создание условий и циклических конструкций для выполнения более сложных задач.
Теперь рассмотрим основные команды Bash:

Основные команды Bash:
Навигация по файловой системе:

pwd — вывести текущую рабочую директорию.
cd <директория> — перейти в указанную директорию.
ls — вывести список файлов в текущей директории.
ls -l — вывести список файлов с подробной информацией (права доступа, размер, дата и т.д.).
ls -a — показать все файлы, включая скрытые.
Работа с файлами и директориями:

cp <файл_источник> <файл_назначение> — копировать файл.
mv <файл_источник> <файл_назначение> — переместить или переименовать файл.
rm <файл> — удалить файл.
rmdir <директория> — удалить пустую директорию.
rm -r <директория> — рекурсивное удаление директории и всех её содержимых.
touch <файл> — создать новый пустой файл или обновить дату последнего изменения файла.
Работа с текстом:

cat <файл> — вывести содержимое файла.
less <файл> — постраничный просмотр содержимого файла.
echo <текст> — вывести текст в терминал.
grep <шаблон> <файл> — искать шаблон в файле.
wc <файл> — подсчитать количество строк, слов и символов в файле.
head <файл> — вывести первые 10 строк файла.
tail <файл> — вывести последние 10 строк файла.
Работа с процессами:

ps — вывести список текущих процессов.
top — показать информацию о процессах в реальном времени.
kill <PID> — завершить процесс по его идентификатору (PID).
bg — запустить процесс в фоновом режиме.
fg — вернуть процесс на передний план.
jobs — показать список фоновых процессов.
Перенаправление и каналы:

> — перенаправить вывод в файл, заменив его содержимое.
>> — перенаправить вывод в файл, добавляя к его содержимому.
< — перенаправить ввод из файла.
| — каналы (pipes) для передачи вывода одной команды на ввод другой.
Переменные и параметры:

export <имя_переменной> — создать или изменить переменную среды.
echo $<имя_переменной> — вывести значение переменной.
$? — вывести код завершения последней команды.
$# — количество аргументов командной строки.
Условия и циклы:

if [ условие ]; then <команды> fi — условная конструкция.
for <переменная> in <список>; do <команды> done — цикл for.
while [ условие ]; do <команды> done — цикл while.
Управление доступом:

chmod <права> <файл> — изменить права доступа к файлу.
chown <пользователь>:<группа> <файл> — изменить владельца и группу файла.
Редактирование файлов:

nano <файл> — редактировать файл в текстовом редакторе nano.
vim <файл> — редактировать файл в текстовом редакторе vim.
Другие полезные команды:

man <команда> — показать справочную информацию о команде.
history — вывести историю выполненных команд.
clear — очистить экран терминала.
alias <имя_псевдонима>='<команда>' — создать псевдоним для команды.
unalias <имя_псевдонима> — удалить псевдоним.
Эти команды являются основой для работы в Bash, и их знание важно для эффективного использования терминала в Linux или других UNIX-подобных системах.


Основные команды для работы с ветками в Git:

1. Просмотр веток:
git branch — выводит список всех локальных веток. Текущая ветка будет отмечена звездочкой (*).
git branch -a — выводит все ветки, включая удаленные.
git branch -r — выводит только удаленные ветки.
2. Создание и переключение на ветки:
git branch <branch-name> — создаёт новую локальную ветку с именем <branch-name>, но не переключается на неё.
git checkout <branch-name> — переключается на существующую ветку.
git switch <branch-name> — альтернатива команде git checkout для переключения на ветку (новая команда в Git 2.23+).
git checkout -b <branch-name> — создаёт новую ветку с именем <branch-name> и сразу переключается на неё.
git switch -c <branch-name> — аналогично git checkout -b, но с использованием команды switch.
3. Удаление ветки:
git branch -d <branch-name> — удаляет локальную ветку <branch-name>, если она была слита с текущей или с другой веткой.
git branch -D <branch-name> — принудительно удаляет ветку, даже если она не была слита.
git push origin --delete <branch-name> — удаляет удалённую ветку на сервере (например, на GitHub).
4. Слияние (merge) веток:
git merge <branch-name> — сливает ветку <branch-name> с текущей веткой. Перед этим нужно переключиться на ветку, в которую вы хотите влить изменения.
git merge --no-ff <branch-name> — слияние с созданием дополнительного коммита даже при возможности fast-forward (чтобы сохранить историю ветки).
5. Решение конфликтов:
Иногда при слиянии веток могут возникнуть конфликты, когда изменения в двух ветках не могут быть автоматически объединены. В этом случае необходимо вручную разрешить конфликт, после чего использовать:

git add <файл> — после разрешения конфликта добавьте изменённый файл в индекс.
git merge --abort — отменяет слияние и возвращает вас к состоянию до начала слияния.
6. Перенос изменений (rebase):
git rebase <branch-name> — позволяет "перенести" изменения из текущей ветки на другую ветку. Это позволяет сохранить более чистую историю без множества коммитов слияния.
git rebase -i <commit-hash> — интерактивный rebase, который позволяет изменить (например, объединить) коммиты в истории.
7. Удаленные ветки:
git fetch — получает последние изменения с удалённого репозитория, включая новые ветки.
git pull — получает последние изменения с удалённого репозитория и сливает их с текущей веткой.
git push origin <branch-name> — отправляет вашу локальную ветку на удалённый репозиторий.
git push origin <branch-name>:<branch-name> — отправляет локальную ветку на удалённый сервер с возможностью её переименования.
8. Работа с ветками в удалённом репозитории:
git branch -r — показать все удалённые ветки.
git checkout -t origin/<branch-name> — создает локальную ветку, отслеживающую ветку на удаленном репозитории.
git push origin <branch-name> — отправить локальную ветку на удалённый репозиторий.
