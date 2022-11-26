К этому репозиторию привязан архив англоязычной Wiki. Намите [Wiki](https://github.com/urho3d-community/wiki-archive/wiki), чтобы перейти к архиву.

## Процесс копирования Wiki

Чтобы GitHub создал репозиторий Wiki, я создал произвольную wiki-страничку. После этого выполнил батник:

```
:: Меняем кодировку консоли на UTF-8
chcp 65001

:: Путь к git.exe
set "PATH=c:\program files\git\bin"

:: Качаем англоязычную Wiki в папку repo
git clone https://github.com/urho3d/Urho3D.wiki repo

:: Переходим в папку репозитория
cd repo

:: Меняем ссылку
git remote set-url origin https://github.com/urho3d-community/wiki-archive.wiki

:: Отправляем изменения на сервер
git push --force

:: Ждём нажатие Enter перед закрытием консоли
pause
```
