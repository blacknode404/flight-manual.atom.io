---
title: Moving in Atom
---
### Moving in Atom
**Переезд в Atom**

Хотя довольно легко перемещаться по Atom, щелкая мышью или используя клавиши со стрелками, есть некоторые сочетания клавиш, которые могут помочь вам держать руки на клавиатуре и перемещаться немного быстрее.

{{#mac}}

Atom поставляется со многими основными комбинациями клавиш Emacs для навигации по документу. Для перехода вверх и вниз на один символ вы можете использовать <kbd class="platform-mac">Ctrl+P</kbd> и <kbd class="platform-mac">Ctrl+N</kbd>. Чтобы перейти влево и вправо на один символ, вы можете использовать <kbd class="platform-mac">Ctrl+B</kbd> и <kbd class="platform-mac">Ctrl+F</kbd>. Это эквивалентно использованию клавиш со стрелками, хотя некоторые люди предпочитают не перемещать руки туда, где расположены клавиши со стрелками на клавиатуре.

В дополнение к движению одного персонажа, существует ряд других сочетаний клавиш движения:

{{/mac}}

{{#windows}}

Atom поддерживает все стандартные комбинации клавиш перемещения курсора Windows. Для перехода вверх, вниз, влево или вправо на один символ вы можете использовать клавиши со стрелками.

В дополнение к движению одного персонажа, существует ряд других сочетаний клавиш движения:

{{/windows}}

{{#linux}}

Atom поддерживает все стандартные комбинации клавиш перемещения курсора в Linux. Для перехода вверх, вниз, влево или вправо на один символ вы можете использовать клавиши со стрелками.

В дополнение к движению одного персонажа, существует ряд других сочетаний клавиш движения:

{{/linux}}

* <span class="platform-mac"><kbd class="platform-mac">Alt+Left</kbd> или <kbd class="platform-mac">Alt+B</kbd></span><kbd class="platform-windows platform-linux">Ctrl+Left</kbd> - Перейти к началу слова
* <span class="platform-mac"><kbd class="platform-mac">Alt+Right</kbd> или <kbd class="platform-mac">Alt+F</kbd></span><kbd class="platform-windows platform-linux">Ctrl+Right</kbd> - Перейти к концу слова
* <span class="platform-mac"><kbd class="platform-mac">Cmd+Left</kbd> или <kbd class="platform-mac">Ctrl+A</kbd></span><kbd class="platform-windows platform-linux">Home</kbd> - Перейти к первому символу текущей строки
* <span class="platform-mac"><kbd class="platform-mac">Cmd+Right</kbd> или <kbd class="platform-mac">Ctrl+E</kbd></span><kbd class="platform-windows platform-linux">End</kbd> - Перейти к концу строки
* <kbd class="platform-mac">Cmd+Up</kbd><kbd class="platform-windows platform-linux">Ctrl+Home</kbd> - Перейти к началу файла
* <kbd class="platform-mac">Cmd+Down</kbd><kbd class="platform-windows platform-linux">Ctrl+End</kbd> - Перейти к концу файла

Вы также можете перейти непосредственно к определенному номеру строки (и столбца) с помощью <kbd class="platform-all">Ctrl+G</kbd>. Это вызовет диалог, который спрашивает, к какой строке вы хотите перейти. Вы также можете использовать `row:column` синтаксис для перехода к символу в этой строке.

![Go directly to a line](../../images/goto.png "Go directly to a line")
![Go directly to a line](../images/goto.png "Go directly to a line")


#### Additional Movement and Selection Commands
**Дополнительные Команды Перемещения и Выбора**

У Atom также есть несколько команд перемещения и выбора, которые по умолчанию не имеют привязок клавиш. Вы можете получить доступ к этим командам из [Command Palette](/getting-started/sections/atom-basics/#command-palette), но если вы обнаружите, что часто используете команды, которые не имеют привязки клавиш, не бойтесь! Вы можете легко добавить запись в свой, `keymap.cson` чтобы создать комбинацию клавиш. Вы можете открыть `keymap.cson` файл в редакторе из строки меню <span class="platform-mac">_Atom > Keymap_</span> | <span class="platform-windows">_File > Keymap_</span> | <span class="platform-linux">_Edit > Keymap_</span>.

Например, команда `editor:move-to-beginning-of-screen-line` доступна в Command Palette, но она не привязана ни к одной комбинации клавиш. Чтобы создать комбинацию клавиш, вам нужно добавить запись в ваш файл `keymap.cson`. Для `editor:select-to-previous-word-boundary`, вы можете добавить следующее к вашему `keymap.cson`:


{{#mac}}
```coffee
'atom-text-editor':
  'cmd-shift-e': 'editor:select-to-previous-word-boundary'
```
{{/mac}}

{{#windows}}
```coffee
'atom-text-editor':
  'ctrl-shift-e': 'editor:select-to-previous-word-boundary'
```
{{/windows}}

{{#linux}}
```coffee
'atom-text-editor':
  'ctrl-shift-e': 'editor:select-to-previous-word-boundary'
```
{{/linux}}

Это свяжет команду `editor:select-to-previous-word-boundary` с <kbd class="platform-mac">Cmd+Shift+E</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+E</kbd>. Для получения дополнительной информации о настройке ваших сочетаний клавиш см. [Настройка Привязок Клавиш](/using-atom/sections/basic-customization/#customizing-keybindings).

Вот список команд перемещения и выбора, которые по умолчанию не имеют сочетаний клавиш:

{{#mac}}
```
editor:move-to-beginning-of-next-paragraph
editor:move-to-beginning-of-previous-paragraph
editor:move-to-beginning-of-screen-line
editor:move-to-beginning-of-line
editor:move-to-beginning-of-next-word
editor:move-to-previous-word-boundary
editor:move-to-next-word-boundary
editor:select-to-beginning-of-next-paragraph
editor:select-to-beginning-of-previous-paragraph
editor:select-to-beginning-of-line
editor:select-to-beginning-of-next-word
editor:select-to-next-word-boundary
editor:select-to-previous-word-boundary
```

{{/mac}}

{{#windows}}
```
editor:move-to-beginning-of-next-paragraph
editor:move-to-beginning-of-previous-paragraph
editor:move-to-beginning-of-screen-line
editor:move-to-beginning-of-line
editor:move-to-end-of-line
editor:move-to-first-character-of-line
editor:move-to-beginning-of-next-word
editor:move-to-previous-word-boundary
editor:move-to-next-word-boundary
editor:select-to-beginning-of-next-paragraph
editor:select-to-beginning-of-previous-paragraph
editor:select-to-end-of-line
editor:select-to-beginning-of-line
editor:select-to-beginning-of-next-word
editor:select-to-next-word-boundary
editor:select-to-previous-word-boundary
```

{{/windows}}

{{#linux}}
```
editor:move-to-beginning-of-next-paragraph
editor:move-to-beginning-of-previous-paragraph
editor:move-to-beginning-of-screen-line
editor:move-to-beginning-of-line
editor:move-to-end-of-line
editor:move-to-first-character-of-line
editor:move-to-beginning-of-next-word
editor:move-to-previous-word-boundary
editor:move-to-next-word-boundary
editor:select-to-beginning-of-next-paragraph
editor:select-to-beginning-of-previous-paragraph
editor:select-to-end-of-line
editor:select-to-beginning-of-line
editor:select-to-beginning-of-next-word
editor:select-to-next-word-boundary
editor:select-to-previous-word-boundary
```

{{/linux}}


#### Navigating by Symbols
**Навигация по Символам**

Вы также можете более информативно прыгать вокруг с помощью Symbols View. Чтобы перейти к символу, такому как определение метода, нажмите <kbd class="platform-mac">Cmd+R</kbd><kbd class="platform-windows platform-linux">Ctrl+R</kbd>. Откроется список всех символов в текущем файле, который вы можете применить к Fuzzy Filter аналогично <kbd class="platform-mac">Cmd+T</kbd><kbd class="platform-windows platform-linux">Ctrl+T</kbd>. Вы также можете искать символы в вашем проекте, но для этого требуется файл `tags`.

![Search by symbol across your project](../../images/symbol.png)
![Search by symbol across your project](../images/symbol.png)

Вы можете создать `tags` файл с помощью [Ctags Utility](https://ctags.io/). Как только он установлен, вы можете использовать его для создания файла `tags`, выполнив команду для его создания. Подробности смотрите в [Документации по Ctags](https://docs.ctags.io/en/latest/).

{{#mac}}

Создав файл `tags`, вы можете использовать его для поиска символов в вашем проекте, нажав <kbd class="platform-mac">Cmd+Shift+R</kbd>. Это также позволяет использовать <kbd class="platform-mac">Alt+Cmd+Down</kbd> для перехода и <kbd class="platform-mac">Alt+Cmd+Up</kbd> возврата из объявления символа под курсором.

{{/mac}}

{{#linux}}

Создав файл `tags`, вы можете использовать его для поиска символов в вашем проекте, нажав <kbd class="platform-windows platform-linux">Ctrl+Shift+R</kbd>. Это также позволяет использовать <kbd class="platform-linux">Alt+Ctrl+Down</kbd> для перехода и <kbd class="platform-linux">Alt+Ctrl+Up</kbd> возврата из объявления символа под курсором.

{{/linux}}

{{#windows}}

Создав файл `tags`, вы можете использовать его для поиска символов в вашем проекте, нажав <kbd class="platform-mac">Cmd+Shift+R</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+R</kbd>.

{{/windows}}

Вы можете настроить способ создания тегов, создав собственный `.ctags` файл в своем домашнем каталоге, <span class="platform-mac platform-linux">`~/.ctags`</span> <span class="platform-windows">`%USERPROFILE%\.ctags`</span>. Пример можно найти [здесь](https://github.com/atom/symbols-view/blob/master/lib/ctags-config).

Функциональность навигации по символам реализована в пакете [Symbols View](https://github.com/atom/symbols-view).

#### Bookmarks
**Закладки**

У Atom также есть отличный способ отметить отдельные строки в вашем проекте, чтобы вы могли быстро вернуться к ним.

Если вы нажмете <kbd class="platform-mac">Cmd+F2</kbd><kbd class="platform-windows">Alt+Ctrl+F2</kbd><kbd class="platform-linux">Ctrl+Shift+F2</kbd>, Atom переключит "bookmark" в текущей строке. Вы можете установить их в своем проекте и использовать их для быстрого поиска и перехода к важным строкам вашего проекта. Небольшой символ закладки добавляется к желобу линии, как в строке 22 [изображения ниже](#bookmarks-image).

Если вы нажмете <kbd class="platform-all">F2</kbd>, Atom перейдет к следующей закладке в файле, который вы сейчас сфокусировали. Если вы используете <kbd class="platform-all">Shift+F2</kbd>, он будет переключаться на них в обратном направлении.

Вы также можете просмотреть список всех текущих закладок вашего проекта, быстро отфильтровать их и перейти к любой из них, нажав <kbd class="platform-all">Ctrl+F2</kbd>.

<a name="bookmarks-image"/>
![View and filter bookmarks](../../images/bookmarks.png "View and filter bookmarks")

![View and filter bookmarks](../images/bookmarks.png "View and filter bookmarks")

Функциональность закладок реализована в пакете [Bookmarks](https://github.com/atom/bookmarks).
