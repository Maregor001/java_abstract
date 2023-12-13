# java_abstract
Обучение java (конспекты)

Инициализация репозитория
git init (от англ. initialize, «инициализировать») — инициализируй репозиторий.
Подготовка файла к коммиту
git add todo.txt (от англ. add, «добавить») — подготовь файл todo.txt к коммиту;
git add --all (от англ. add, «добавить» + all, «всё») — подготовь к коммиту сразу все файлы, в которых были изменения, и все новые файлы;
git add . — подготовь к коммиту текущую папку и все файлы в ней.
Создание коммита
git commit -m "Комментарий к коммиту." (от англ. commit, «совершать», «фиксировать» + message, «сообщение») — сделай коммит и оставь комментарий, чтобы было проще понять, какие изменения внесены. 
Просмотр информации о коммитах
git log (от англ. log, «журнал [записей]») — выведи подробную историю коммитов.
Просмотр состояния файлов
git status (от англ. status, «статус», «состояние») — покажи текущее состояние репозитория.
С этим набором команд вы сможете самостоятельно инициализировать проект и начать отслеживать в нём изменения. Фундамент знаний о Git заложен!


В этой теме вы взглянули на Git как на инструмент командной работы и научились создавать удалённые репозитории, а затем связывать их с локальными. Теперь вы также можете копировать чужие репозитории. Повторим основные команды и концепты из уроков.
Синхронизация локального и удалённого репозиториев
git remote add origin https://github.com/YandexPracticum/first-project.git (от англ. remote, «удалённый» + add, «добавить») — привяжи локальный репозиторий к удалённому с URL https://github.com/YandexPracticum/first-project.git;
git remote -v (от англ. verbose, «подробный») — проверь, что репозитории действительно связались;
git push -u origin main (от англ. push, «толкать») — в первый раз загрузи все коммиты из локального репозитория в удалённый с названием origin.
💡 Ваша ветка может называться master, а не main. Подправьте команду, если это необходимо.
git push (от англ. push, «толкать») — загрузи коммиты в удалённый репозиторий после того, как он был привязан с помощью флага -u.
Копирование чужих репозиториев
Клонирование
git clone git@github.com:TheGreatOwner/the-great-project.git (от англ. clone, «клон», «копия») — склонируй репозиторий с URL the-great-project.git из аккаунта TheGreatOwner на мой локальный компьютер.
«Форк»
«Форк» — операция, которая не связана с Git напрямую и выполняется через графический интерфейс GitHub (кнопка Fork в правом верхнем углу страницы репозитория). «Форк» создаёт независимую копию репозитория со всеми файлами, коммитами и ветками в аккаунте GitHub. Такая копия будет полностью независима. Внесённые изменения не будут синхронизированы с исходным репозиторием.
💡 Комбинацию «форк» + clone часто используют для внесения изменений в публичные репозитории. В этом случае «форк» становится подготовительным этапом перед клонированием чужого репозитория на локальный компьютер.
Если репозиторий приватный или это репозиторий вашей компании, при работе с ним достаточно clone.
SSH-ключи
Протокол SSH обеспечивает безопасный обмен данными в сети. С его помощью можно получать данные с удалённого компьютера или отправлять их на него. Трафик шифруется, поэтому протокол безопасен.
SSH-ключ состоит из двух частей — публичной и приватной. Приватный ключ хранится только на вашем компьютере и не должен передаваться кому-либо ещё. Он используется для расшифровки данных. Публичный ключ доступен всем и используется для шифрования данных. Они могут быть расшифрованы парным приватным ключом.
Файл с расширением .pub содержит публичный ключ, им можно делиться с веб-сайтами или коллегами. Файл без расширения .pub — приватный.
Прежде чем генерировать новую пару ключей, следует убедиться, что они отсутствуют на вашем компьютере. Проверить это можно командой ls -la .ssh/ в домашней директории. Если ключи отсутствуют, создать их можно командой ssh-keygen в директории ~/.ssh. После генерации ключ нужно привязать к GitHub.