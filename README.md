# Прохождение марафона "Заверстаю #2" от [HTMLAcademy](https://htmlacademy.ru)


*Внимание: Используемый подход и инструменты не всегда совпадают с подходом, рекомендуемым Академией*

*Весь процесс происходит на машине под управлением Windows 10*

- [Прохождение марафона "Заверстаю #2" от HTMLAcademy](#прохождение-марафона-заверстаю-2-от-htmlacademy)
  - [Шаг 0. Подготовка](#шаг-0-подготовка)
  - [Шаг 1. Создание разметки](#шаг-1-создание-разметки)

## Шаг 0. Подготовка

Для прохождения марафона нам понадобятся следующие инструменты:
1. Система управления версиями - [git](https://git-scm.com/download/win)
2. Работа с репозиториями GitHub'а - [GitHub CLI](https://github.com/cli/cli/releases/download/v2.0.0/gh_2.0.0_windows_amd64.msi)
3. Командная строка - [Windows Terminal](https://www.microsoft.com/ru-ru/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab)
4. Текстовый редактор - [VS Code](https://code.visualstudio.com/download#)
5. Работа с макетом - [Figma](https://www.figma.com/download/desktop/win)

- Заводим учётную запись на сайте [github.com](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)

- Скачиваем и устанавливаем все программы.

- Настраиваем git - в терминале вводим команды `git config --global user.name "Ваше Имя"` и `git config --global user.email "ваш@email"`

- Настраиваем GitHub CLI - в терминале вводим команду `gh auth login` и вводим данные учётной записи на [github.com](https://github.com)

- [Настраиваем VS Code](https://htmlacademy.ru/blog/boost/tools/editors-for-the-coders#VSCode). Рекомендую зарегистрироваться на сайте [FrontendMasters](https://frontendmasters.com) и просмотреть первые три главы бесплатного курса [Visual Studio Code Can Do That?](https://frontendmasters.com/courses/customize-vs-code/)

- [Знакомимся с Figma](https://htmlacademy.ru/blog/boost/tools/figma)

- Подготавливаем проект:
  1. Создаём папку для проекта ![создаём папку для проекта](./img/00-1.jpg)
  2. Переходим в созданную папку ![переходим в созданную папку](./img/00-2.jpg)
  3. Иницилизируем git-репозиторий и создаём репозиторий на [github.com](https://github.com) ![создаём репозиторий](./img/00-3.jpg)
  4. В созданной папке создаём ещё две папки - img и styles. В /img импортируем все изображения из макета, в /styles создаём файл `styles.css`, в котором будем прописывать стили для нашего проекта, также на шаге 2 мы сохраним в эту папку файл `normalize.css`.
  5. В корневом каталоге нашего проекта создаём файл `index.html`.
  6. Структура проекта должна выглядеть следующим образом: ![файловая структура проекта](./img/00-4.jpg)

- На этом шаге остаётся только зафиксировать проделанную работу и отправить изменения на [github.com](https://github.com):
  1. В командной строке вводим `git add -A`. Эта команда добавляет в репозиторий добавленные нами папки и файлы.
  2. Дальше вводим `git commit -m "init: start marathon project"`. Данной командой мы фиксируем и описываем все изменения в проекте. Про правила написания коммитов можно почитать [тут](https://www.conventionalcommits.org/ru/v1.0.0/).

На этом подготовительный этап завершён.


## Шаг 1. Создание разметки


