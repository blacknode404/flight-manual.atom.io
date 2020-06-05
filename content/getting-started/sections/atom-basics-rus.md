---
title: Atom Basics
---
### Atom Basics
**Atom Основы**

Теперь, когда Atom установлен в вашей системе, давайте запустим его, настроим и познакомимся с редактором.

Когда вы впервые запускаете Atom, вы должны получить экран, который выглядит следующим образом:

![Atom's welcome screen](../../images/first-launch.png)
![Atom's welcome screen](../images/first-launch.png)

Это экран приветствия Atom и дает вам довольно хорошую отправную точку для начала работы с редактором.

#### Terminology
**Терминология**

Вы можете найти определения для всех различных терминов, которые мы используем в руководстве, в нашем [Глоссарии](/resources/sections/glossary/).

#### Command Palette
**Command Palette**

На этом экране приветствия мы знакомимся с, пожалуй, самой важной командой в Atom, Command Palette. Если вы нажмете, <kbd class="platform-mac">Cmd+Shift+P</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+P</kbd> находясь в фокусе на панели редактора, появится Command Palette.

{{#note}}

На протяжении всей книги мы будем использовать сочетания клавиш, например, <kbd class="platform-mac">Cmd+Shift+P</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+P</kbd> чтобы продемонстрировать, как запустить команду. Это привязки клавиш по умолчанию для платформы, на которой мы вас обнаружили.

Если вы хотите увидеть платформу, отличную от той, которую мы обнаружили, вы можете выбрать другую платформу, используя селектор платформ в верхней части страницы:

![Platform Selector](../../images/platform-selector.png "Platform Selector")
![Platform Selector](../images/platform-selector.png "Platform Selector")

Если селектор платформ отсутствует, то текущая страница не имеет контента для конкретной платформы.

Если вы настроили свою комбинацию клавиш Atom, вы всегда можете увидеть привязку клавиш, которую вы отобразили, в Command Palette или на вкладке Keybindings в [Settings View](#settings-and-preferences).

{{/note}}

Это управляемое поиском меню может выполнить практически любую важную задачу, которая возможна в Atom. Вместо того, чтобы щелкать по всем меню приложения, чтобы что-то найти, вы можете нажать <kbd class="platform-mac">Cmd+Shift+P</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+P</kbd> и выполнить поиск команды.

![Command Palette](../../images/command-palette.png "Command Palette")
![Command Palette](../images/command-palette.png "Command Palette")

Вы можете не только просматривать и быстро выполнять поиск среди тысяч возможных команд, но и видеть, есть ли привязка клавиш, связанная с ней. Это здорово, потому что это означает, что вы можете угадать свой путь к интересным вещам, одновременно изучая комбинации клавиш для этого.

В остальной части книги мы попытаемся прояснить текст, который вы можете искать в Command Palette в дополнение к связыванию клавиш для различных команд.

#### Settings and Preferences
**Настройки и Предпочтения**

Atom имеет ряд настроек и предпочтений, которые вы можете изменить в Settings View.

![Settings View](../../images/settings.png "Settings View")
![Settings View](../images/settings.png "Settings View")

Это включает в себя такие вещи, как изменение темы, указание, как обрабатывать перенос, настройки шрифта, размер вкладки, скорость прокрутки и многое другое. Вы также можете использовать этот экран для установки новых пакетов и тем, которые мы рассмотрим в [Atom Пакеты](/using-atom/sections/atom-packages).

Чтобы открыть Settings View, вы можете:

* Использовать пункт меню <span class="platform-mac">*Atom > Preferences*</span> | <span class="platform-windows">*File > Settings*</span> | <span class="platform-linux">*Edit > Preferences*</span> в строке меню
* Искать `settings-view:open` в [Command Palette](#command-palette)
* Использовать <kbd class="platform-mac">Cmd+,</kbd><kbd class="platform-windows platform-linux">Ctrl+,</kbd> связывание клавиш

##### Changing the Theme
**Смена Темы**

Settings View также позволяет менять темы для Atom. Atom поставляется с 4 различными темами пользовательского интерфейса, темными и светлыми вариантами тем Atom и One, а также с 8 различными синтаксическими темами. Вы можете изменить активную тему, щелкнув вкладку Themes на боковой панели в Settings View, или установить новые темы, щелкнув вкладку Install.

![Changing the theme from the Settings View](../../images/theme.png "Changing the theme from the Settings View")
![Changing the theme from the Settings View](../images/theme.png "Changing the theme from the Settings View")

UI Theme управляют стилем элементов пользовательского интерфейса, таких как вкладки и древовидная структура, а Syntax Theme управляют подсветкой синтаксиса текста, загружаемого в редактор. Чтобы изменить синтаксис или тему пользовательского интерфейса, просто выберите что-то другое в соответствующем раскрывающемся списке.

На https://atom.io также есть десятки тем, которые вы можете выбрать, если хотите что-то другое. Мы рассмотрим настройку темы в [Твики Стиля](/using-atom/sections/basic-customization) и создание собственной темы в [Создание Темы](/hacking-atom/sections/creating-a-theme).

##### Soft Wrap
**Мягкая Упаковка**

Вы можете использовать Settings View вкладку Editor, чтобы указать свой пробел и параметры переноса.



![Whitespace and wrapping preferences settings](../../images/settings-wrap.png)
![Whitespace and wrapping preferences settings](../images/settings-wrap.png)

Включение "Soft Tabs" будет вставлять пробелы вместо фактических символов табуляции при нажатии клавиши <kbd class="platform-all">Tab</kbd>, а параметр "Tab Length" указывает, сколько пробелов вставлять при этом, или сколько пробелов используется для представления вкладки, если "Soft Tabs" выключен.

Параметр "Soft Wrap" будет переносить слишком длинные строки, чтобы поместиться в текущее окно. Если "Soft Wrap" отключен, строки будут просто выходить за пределы экрана, и вам придется прокручивать окно, чтобы увидеть остальную часть содержимого. При переключении "Soft Wrap At Preferred Line Length", строки будут переноситься на 80 символов вместо конца экрана. Вы также можете изменить длину строки по умолчанию на значение, отличное от 80 на этом экране.

[Основные Настройки](/using-atom/sections/basic-customization/) покажут, как установить различные параметры переноса для разных типов файлов (например, если вы хотите переносить файлы Markdown, но не другие файлы).

#### Opening, Modifying, and Saving Files
**Открытие, Изменение и Сохранение файлов**

Теперь, когда ваш редактор выглядит и работает так, как вы хотите, давайте начнем открывать и редактировать файлы. В конце концов, это текстовый редактор, верно?

##### Opening a File
**Открытие Файла**

Есть несколько способов открыть файл в Atom. Вы можете сделать это, выбрав *File > Open* в строке меню или нажав, <kbd class="platform-mac">Cmd+O</kbd><kbd class="platform-windows platform-linux">Ctrl+O</kbd> чтобы выбрать файл из стандартного диалога.

![Open file by dialog](../../images/open-file.png "Open file by dialog")
![Open file by dialog](../images/open-file.png "Open file by dialog")

Это полезно для открытия файла, который не содержится в проекте, в котором вы находитесь (подробнее об этом далее), или если вы по какой-то причине начинаете работу из нового окна.

Другой способ открыть файл в Atom - из командной строки с помощью команды `atom`. <span class="platform-mac">Строка меню Atom имеет команду под названием "Install Shell Commands", которая устанавливает команды `atom` и `apm`, [если Atom не удалось установить их самостоятельно](/getting-started/sections/installing-atom/#installing-atom-on-mac). </span><span class="platform-windows platform-linux"> Команды `atom` и `apm` автоматически устанавливаются как часть Atom'a [Установка Atom](/getting-started/sections/installing-atom/).</span>

Вы можете запустить команду `atom` с одним или несколькими путями к файлам, чтобы открыть эти файлы в Atom.

``` command-line
$ atom --help
> Atom Editor v1.8.0

> Usage: atom [options] [path ...]

> One or more paths to files or folders may be specified. If there is an
> existing Atom window that contains all of the given folders, the paths
> will be opened in that window. Otherwise, they will be opened in a new
> window.

> ...
```

Это отличный инструмент, если вы привыкли к терминалу или много работаете с терминалом. Просто включите `atom [files]` и вы готовы начать редактирование.
Вы даже можете открыть файл в определенной строке (и, необязательно, столбце), чтобы курсор был расположен именно там, где вы хотите. Например, вы можете выполнить поиск по ключевому слову в репозитории, чтобы найти строку, которую хотите изменить:

```command-line
$ git grep -n 'Opening a File$'
content/getting-started/sections/atom-basics.md:84:##### Opening a File
```

а затем перейдите к этой строке, добавьте двоеточие и номер строки к пути к файлу:

```command-line
$ atom content/getting-started/sections/atom-basics.md:84
```

Иногда вы можете захотеть, чтобы курсор перешел к точной позиции столбца искомого ключевого слова. Просто добавьте еще двоеточие плюс номер столбца:

```command-line
$ git grep -n --column 'Windows Explorer'
content/getting-started/sections/atom-basics.md:150:722
$ atom content/getting-started/sections/atom-basics.md:150:722
```

##### Editing and Saving a File
**Редактирование и Сохранение Файла**

Редактировать файл довольно просто. Вы можете нажимать вокруг и прокручивать мышью и вводить, чтобы изменить содержимое. Нет специального режима редактирования или клавишных команд. Если вы предпочитаете редактировать с режимами или более сложными клавишами, вам следует взглянуть на [список пакетов Atom](https://atom.io/packages). Существует множество пакетов, которые имитируют популярные стили.

Чтобы сохранить файл, вы можете выбрать *File > Save* в строке меню или нажать <kbd class="platform-mac">Cmd+S</kbd><kbd class="platform-windows platform-linux">Ctrl+S</kbd> чтобы сохранить файл. Если вы выберете *File > Save As* или нажмете <kbd class="platform-mac">Cmd+Shift+S</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+S</kbd> тогда вы можете сохранить текущий контент в вашем редакторе под другим именем файла. Наконец, вы можете выбрать *File > Save All* <span class="platform-mac"> или нажать <kbd class="platform-mac">Alt+Cmd+S</kbd></span> чтобы сохранить все открытые файлы в Atom.

#### Opening Directories
**Открытие Каталогов**

Atom работает не только с файлами. Вы будете проводить большую часть своего времени. Чтобы открыть каталог, выберите пункт меню <span class="platform-mac">*File > Open*</span> | <span class="platform-windows platform-linux">*File > Open Folder*</span> и выберите каталог в диалоговом окне. Вы также можете добавить более одного каталога в текущее окно Atom, выбрав *File > Add Project Folder* пункт меню или нажав <kbd class="platform-mac">Cmd+Shift+O</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+A</kbd>.

Вы можете открыть любое количество каталогов из командной строки `atom`. Например, вы можете запустить команду `atom ./hopes ./dreams` чтобы открыть оба `hopes` и `dreams` каталоги, одновременно.

Когда вы открываете Atom вы автоматически получаете сборку в окне Tree View.

![Tree View in an open project](../../images/project-view.png "Tree View in an open project")
![Tree View in an open project](../images/project-view.png "Tree View in an open project")

Tree View позволяет вам исследовать и изменять структуру файлов и каталогов вашего проекта. Вы можете открывать, переименовывать, удалять и создавать новые файлы из этого представления.

Вы также можете скрыть и показать его с помощью <kbd class="platform-mac">Cmd+\\</kbd><kbd class="platform-windows platform-linux">Ctrl+\\</kbd> или команды `tree-view:toggle` из Command Palette, и нажав <kbd class="platform-mac">Ctrl+0</kbd><kbd class="platform-windows platform-linux">Alt+\\</kbd> вы сфокусируете его. Когда Tree View сфокусирован, вы можете нажать <kbd class="platform-all">A</kbd>, <kbd class="platform-all">M</kbd>, или <kbd class="platform-all">Delete</kbd> чтобы добавить, переместить или удалить файлы и папки. Вы также можете щелкнуть правой кнопкой мыши файл или папку в Tree View, чтобы увидеть множество различных опций, включая все эти, а также отображение файла в <span class="platform-mac">Finder</span> | <span class="platform-windows">Windows Explorer</span> | <span class="platform-linux">вашей собственной файловой системы</span> или копирование пути к файлу в буфер обмена.

{{#note}}

**Atom Packages**

Как и многие другие части Atom, Tree View не встроен непосредственно в редактор, а представляет собой отдельный пакет, который по умолчанию поставляется с Atom. Пакеты, связанные с Atom, называются Core Packages. Те, которые не связаны с Atom, называются Community Packages.

Вы можете найти исходный код для представления дерева на GitHub по адресу https://github.com/atom/tree-view.


Это одна из интересных вещей об Atom. Многие из его основных функций на самом деле представляют собой просто пакеты, реализованные так же, как и любые другие функции. Это означает, что если вам не нравится, например, Tree View, вы можете написать собственную реализацию этой функциональности и полностью ее заменить.

{{/note}}

##### Opening a File in a Project
**Открытие Файла в Проекте**

Когда у вас есть проект, открытый в Atom, вы можете легко найти и открыть любой файл в этом проекте.

Если вы нажмете <kbd class="platform-mac">Cmd+T</kbd><kbd class="platform-windows platform-linux">Ctrl+T</kbd> или <kbd class="platform-mac">Cmd+P</kbd><kbd class="platform-windows platform-linux">Ctrl+P</kbd>, появится Fuzzy Finder. Это позволит вам быстро найти любой файл в вашем проекте, набрав части пути.

![Opening files with the Fuzzy Finder](../../images/finder.png "Opening files with the Fuzzy Finder")
![Opening files with the Fuzzy Finder](../images/finder.png "Opening files with the Fuzzy Finder")

Вы также можете выполнять поиск только в тех файлах, которые в данный момент открыты (а не в каждом файле в вашем проекте) с помощью <kbd class="platform-mac">Cmd+B</kbd><kbd class="platform-windows platform-linux">Ctrl+B</kbd>. Это поиск через ваши "буферы" или открытые файлы. Вы также можете ограничить Fuzzy Finder с помощью <kbd class="platform-mac">Cmd+Shift+B</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+B</kbd>, который ищет только те файлы, которые являются новыми или были изменены с момента вашей последнего Git Commit'a.

Fuzzy Finder использует `core.ignoredNames`, `fuzzy-finder.ignoredNames` и `core.excludeVCSIgnoredPaths` параметры конфигурации , чтобы отфильтровать файлы и папки , которые не будут показаны. Если у вас есть проект с тоннами файлов, которые вы не хотите, чтобы он просматривал, вы можете добавить шаблоны или пути к любому из этих параметров конфигурации или к вашим [стандартным `.gitignore` файлам](https://git-scm.com/docs/gitignore). Мы узнаем больше о настройках конфигурации в [Глобальных Параметрах Конфигураций](/using-atom/sections/basic-customization/#global-configuration-settings), но сейчас вы можете легко установить их в Settings View в разделе Core Settings.

И то `core.ignoredNames` и другое `fuzzy-finder.ignoredNames` интерпретируется как шаблоны glob, реализованные [модулем Node minimatch](https://github.com/isaacs/minimatch).

{{#tip}}

**Configuration Setting Notation**

Иногда вы увидите, что мы обращаемся к настройкам конфигурации, которые прописаны как "Ignored Names" в "Core Settings". В других случаях вы увидите, как мы используем сокращенное имя, например `core.ignoredNames`. Оба из них относятся к одному и тому же. Сокращенное обозначение - это имя пакета, затем точка `.`, за которой следует название настройки в "camelCased".

Если у вас есть фраза, которую вы хотите использовать в случае верблюда, выполните следующие действия:

1. Все буквы первого слова в нижнем регистре
1. Первая буква во всех последующих словах верхний регистр
1. Удалить пробелы

Таким образом, "Ignored Names" становится "ignoredNames".

{{/tip}}
