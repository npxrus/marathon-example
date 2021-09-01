# Прохождение марафона "Заверстаю #2" от [HTMLAcademy](https://htmlacademy.ru)


*Внимание: Используемый подход и инструменты не всегда совпадают с подходом, рекомендуемым Академией*

*Весь процесс происходит на машине под управлением Windows 10*

*Я в Telegram [@npxrus](https://t.me/npxrus)*

- [Прохождение марафона "Заверстаю #2" от HTMLAcademy](#прохождение-марафона-заверстаю-2-от-htmlacademy)
  - [Шаг 0. Подготовка](#шаг-0-подготовка)
    - [Инструменты](#инструменты)
    - [Git](#git)
    - [VS Code](#vs-code)
    - [Figma](#figma)
    - [Структура проекта](#структура-проекта)
    - [Сохранение изменений](#сохранение-изменений)
  - [Шаг 1. Создание разметки](#шаг-1-создание-разметки)
    - [Семантика](#семантика)
    - [Первоначальная структура](#первоначальная-структура)
    - [Выделяем крупные смысловые блоки](#выделяем-крупные-смысловые-блоки)
    - [Выделяем в блоках смысловые разделы](#выделяем-в-блоках-смысловые-разделы)
    - [Задаём заголовки](#задаём-заголовки)
    - [Размечаем мелкие элементы](#размечаем-мелкие-элементы)
      - [Шапка сайта](#шапка-сайта)
      - [Заглавный раздел](#заглавный-раздел)
      - [Раздел с преимуществами](#раздел-с-преимуществами)
      - [Раздел с популярными букетами](#раздел-с-популярными-букетами)
      - [Раздел с катологом](#раздел-с-катологом)
      - [Раздел со спецпредложением](#раздел-со-спецпредложением)

## Шаг 0. Подготовка

### Инструменты
Для прохождения марафона нам понадобятся следующие инструменты:
1. Система управления версиями - [git](https://git-scm.com/download/win)
2. Работа с репозиториями GitHub'а - [GitHub CLI](https://github.com/cli/cli/releases/download/v2.0.0/gh_2.0.0_windows_amd64.msi)
3. Командная строка - [Windows Terminal](https://www.microsoft.com/ru-ru/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab)
4. Текстовый редактор - [VS Code](https://code.visualstudio.com/download#)
5. Работа с макетом - [Figma](https://www.figma.com/download/desktop/win)

- Заводим учётную запись на сайте [github.com](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)

- Скачиваем и устанавливаем все программы.

### Git
- Настраиваем git - в терминале вводим команды `git config --global user.name "Ваше Имя"` и `git config --global user.email "ваш@email"`

- Настраиваем GitHub CLI - в терминале вводим команду `gh auth login` и вводим данные учётной записи на [github.com](https://github.com)

### VS Code
- [Настраиваем VS Code](https://htmlacademy.ru/blog/boost/tools/editors-for-the-coders#VSCode). Рекомендую зарегистрироваться на сайте [FrontendMasters](https://frontendmasters.com) и просмотреть первые три главы бесплатного курса [Visual Studio Code Can Do That?](https://frontendmasters.com/courses/customize-vs-code/)

### Figma
- [Знакомимся с Figma](https://htmlacademy.ru/blog/boost/tools/figma)

### Структура проекта
- Подготавливаем проект:
  1. Создаём папку для проекта

  ![создаём папку для проекта](./img/00-1.jpg)

  2. Переходим в созданную папку

  ![переходим в созданную папку](./img/00-2.jpg)

  3. Иницилизируем git-репозиторий и создаём репозиторий на [github.com](https://github.com)

  ![создаём репозиторий](./img/00-3.jpg)

  4. В созданной папке создаём ещё две папки - img и styles. В /img импортируем все изображения из макета, в /styles создаём файл `styles.css`, в котором будем прописывать стили для нашего проекта, также на шаге 2 мы сохраним в эту папку файл `normalize.css`.
  5. В корневом каталоге нашего проекта создаём файл `index.html`.
  6. Структура проекта должна выглядеть следующим образом:

  ![файловая структура проекта](./img/00-4.jpg)

### Сохранение изменений
- На этом шаге остаётся только зафиксировать проделанную работу и отправить изменения на [github.com](https://github.com):
  1. В командной строке вводим `git add -A`. Эта команда добавляет в репозиторий добавленные нами папки и файлы.
  2. Дальше вводим `git commit -m "init: start marathon project"`. Данной командой мы фиксируем и описываем все изменения в проекте. Про правила написания коммитов можно почитать [тут](https://www.conventionalcommits.org/ru/v1.0.0/).

На этом подготовительный этап завершён.


## Шаг 1. Создание разметки

### Семантика
На этом этапе нам предстоит задать задать семантическую структуру документа. Что это такое и зачем это нужно хорошо разбирается в [этом докладе](https://www.youtube.com/watch?v=bDYEnNzprzE). Итак, приступим.

### Первоначальная структура
*Здесь и далее для удобства я буду использовать Emmet - утилиту, упрощающую и ускоряющую работу с html и css. Проще говоря, это набор сокращений, которые развёртываются в полноценные языковые конструкции. Список таких сокращений можно посмотреть [тут](https://docs.emmet.io/cheat-sheet/).*

Откроем ранее созданный файл `index.html`. На первой строке вводим `!` и жмём на `Tab` и получаем готовый каркас нашего html-документа.

![каркас html-документа](./img/01-1.jpg)

Поменяем `title`, возьмём текст из логотипа

![задаём title](./img/01-2.jpg)

По умолчанию Emmet указывает английский в качестве языка страницы, поменяем на русский

![задаём язык страницы](./img/01-3.jpg)

### Выделяем крупные смысловые блоки
Основа страницы задана, можем приступить непосредственно к написанию разметки.
Для начала определим самые крупные смысловые блоки страницы. Ими у нас будут шапка (`header`) - здесь размещаем введение к сайту, информацию, повторяющуюся на каждой странице (логотип, навигация, слоган, поле поиска по сайту); основная содержательная часть страницы (`main`); подвал (`footer`) - здесь мы размещаем дополнительную информацию, повторяющуюся на каждой странице (дополнительная навигация, копирайты, контакты и т.д.).

*Не стоит думать, что элементы `header` и `footer` предназначены исключительно для глобальных областей страницы. Они просто размечают вступительную и дополнительную информацию о контенте соответственно и могут входить в состав элементов `main`, `section`, `article`, `aside`.*

Разместим эти блоки на странице при помощи Emmet

![размечает header, main и footer](./img/01-4.jpg)

### Выделяем в блоках смысловые разделы
Далее определяем в этих блоках крупные смысловые разделы, т.е. `nav`, `section`, `article` и `aside`. В элементе `nav` размещают ссылки навигации как на разделы текущего документа, так и на другие страницы. Навигацию можно считать вступительной информацией к сайту, поэтому размещаем этот элемент внутри `header`

![размещаем элемент nav](./img/01-5.jpg)

Изучив макет, определяем основные разделы в блоке `main` - заглавный раздел с информацией о деятельности компании, раздел с преимуществами, раздел с популярными букетами, раздел с категориями каталога, раздел со спецпредложением, раздел с описанием оформления заказа, раздел с новостями, раздел с отзывами о компании и раздел с информацией о компании. Перенесём все эти разделы в разметку, для удобства сразу назначим им классы и идентификаторы для навигации. Получим следующую структуру:

![структура секции main](./img/01-6.jpg)

В элементе `footer` дублируется навигация по сайту. Так как есть [рекомендация от составителей спецификации](https://web-standards.ru/articles/avoiding-html5-mistakes/), что если навигация дублируется в двух местах — например, в шапке и в подвале — то в подвале можно её в `nav` не оборачивать.

### Задаём заголовки
На макете не заголовка первого уровня, поэтом добавим его самостоятельно и визуально скроем

![основной заголовок страницы](./img/01-7.jpg)

Добавляем заголовки разделов в соответствии с макетом. Разделы с преимуществами, каталогом и спецпредложениями по макету не имеют заголовка, поэтому добавляем их самостоятельно и визуально скрываем. Сейчас наша страница выглядит так

![структура заголовков](./img/01-8.jpg)

### Размечаем мелкие элементы

#### Шапка сайта
Начнём с навигации в шапке. Разметим логотип сайта. Согласно обязательным требованиям [технического задания](https://docs.google.com/document/d/1UZQpZItCsK2jYSU7fWlNasmQHS-uAzeC87Qt80HKEtg/edit) логотип должен быть ссылкой на главную страницу, поэтому обернём его в `a`

![вставляем логотип](./img/01-9.jpg)

и расставим необходимые атрибуты

![расставляем атрибуты](./img/01-10.jpg)

Навигация - это список ссылок, которые можно располагать в любом порядке, поэтому для его разметки используем неупорядоченный список `ul`, вводим `ul>li*6>a` и заполняем атрибуты и текст ссылок. Шапка сайта приобретает следующий вид

![разметка шапки сайта](./img/01-11.jpg)

#### Заглавный раздел
Добавляем параграф с информацией о деятельности компании, ссылку на каталог и изображения букетов, которые показывают, что компания предлагает. Изображения однородные, поэтому делаем их элементами неупорядоченного списка. Вводим `p+a{Смотреть каталог}+ul>li*2>img` и заполняем атрибуты и текст

![разметка заглавного раздела](img/01-12.jpg)

#### Раздел с преимуществами
Данный раздел состоит из трёх одинаковых блоков, состоящих из заголовка с наименованием преимущества и текстом, описывающим это преимущество. Изображения не играют никакой роли, мы можем их удалить, смысл блока от этого не изменится, поэтому добавим их на следующих этапах с помощью стилей. Так как все блоки в этом разделе одинаковые и могут быть расположены в любом порядке, то делаем их элементами неупорядоченного списка. Вводим `ul>li*3>h3+p` и вставляем текст из макета

![разметка раздела с преимуществами](./img/01-13.jpg)

#### Раздел с популярными букетами
Данный раздел подразумевает использование слайдера для прокрутки популярных букетов и хотя в [техническом задании](https://docs.google.com/document/d/1UZQpZItCsK2jYSU7fWlNasmQHS-uAzeC87Qt80HKEtg/edit#heading=h.n318s0es3uz9) говорится о том, что реализовывать слайдер не нужно, тем не менее разметку будем делать с учётом использования слайдера. В карточке слайда расположим заголовок с названием букета, описание этого букета, его размер, цену, ссылку на страницу заказа и его изображение. Так как слайдов может быть несколько и они прокручиваются в любом порядке, то используем наш привычный неупорядоченный список. Вводим `ul>li>h3+p*3+a+img` и заполняем атрибуты ссылки и изображения, а также вставляем текст из макета. Остаётся добавить кнопки управления слайдером - `btn*2>span.visually-hidden`

![разметка раздела с популярными букетами](./img/01-14.jpg)

#### Раздел с катологом
Здесь у нас по [техзаданию](https://docs.google.com/document/d/1UZQpZItCsK2jYSU7fWlNasmQHS-uAzeC87Qt80HKEtg/edit) список карточек, которые являются ссылками на страницу каталога. Со списком всё понятно, вопрос как оформить карточку. Тут возможны два варианта - либо это текстовый блок с фоновой картинкой, либо это изображение с подписью, иллюстрирующее содержимое соответствующего раздела каталога. Мне более симпатичен второй вариант, поэтому реализуем его. Для изображений с подписью есть специальный элемент `figure`. Таким образом структура карточки получается такой - `figure` с изображением, в нём `figcaption` с подписью и всё это обёрнуто в ссылку. Вводим `ul>li*3>a>figure>img+figc>h3+p` и, как обычно, заполняем атрибуты и вставляем текст из макета.

![разметка раздела каталога](./img/01-15.jpg)

#### Раздел со спецпредложением
Здесь всё просто - текстовый блок и блок с фоновым изображением, которое мы добавим позже. Вводим `h3+p` и вставляем текст из макета.

![разметка раздела со спецпредложением](./img/01-16.jpg)
