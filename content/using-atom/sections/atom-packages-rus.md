---
title: Atom Packages
---
### Atom Packages
**Atom Пакеты**

Сначала мы начнем с системы пакетов Atom. Как мы упоминали ранее, сам Atom - это базовое ядро ​​функциональности, которое поставляется с рядом полезных пакетов, которые добавляют новые функции, такие как [Tree View](https://github.com/atom/tree-view) и [Settings View](https://github.com/atom/settings-view).

На самом деле, существует более 80 пакетов, которые содержат все функции, доступные в Atom по умолчанию. Например, [Welcome Screen](https://github.com/atom/welcome) который вы видите при первом запуске Atom, [Spell Checker](https://github.com/atom/spell-check), [Themes](https://github.com/atom/one-dark-ui) и [Fuzzy Finder](https://github.com/atom/fuzzy-finder) a- это пакеты, которые обслуживаются отдельно и все используют те же API, к которым у вас есть доступ, как мы увидим в главе [Взлом Atom'a](/hacking-atom/).

Это означает, что пакеты могут быть невероятно мощными и могут изменить все: от внешнего вида всего интерфейса до базовой работы даже основных функций.

Чтобы установить новый пакет, вы можете использовать вкладку Install в привычном Settings View. Откройте Settings View с помощью <kbd class="platform-mac">Cmd+,</kbd><kbd class="platform-windows platform-linux">Ctrl+,</kbd>, нажмите на вкладку "Install" и введите свой поисковый запрос в поле Install Packages.

Перечисленные здесь пакеты были опубликованы по адресу https://atom.io/packages, который является официальным реестром пакетов Atom. Поиск в Settings View приведет к переходу в реестр пакетов Atom и загрузит все, что соответствует вашим условиям поиска.

![Package install screen](../../images/packages-install.png "Package install screen")
![Package install screen](../images/packages-install.png "Package install screen")

Все пакеты появятся с кнопкой "Install". Нажмите, чтобы загрузить пакет и установить его. Ваш редактор теперь будет иметь функциональные возможности, которые предоставляет пакет.

#### Package Settings
**Настройки Пакета**

После установки пакета в Atom он будет отображаться в Settings View на вкладке "Packages" вместе со всеми предустановленными пакетами, которые поставляются с Atom. Чтобы отфильтровать список, чтобы найти его, вы можете ввести его в поле поиска прямо под заголовком "Installed Packages".

![Package settings screen](../../images/package-specific-settings.png "Package settings screen")
![Package settings screen](../images/package-specific-settings.png "Package settings screen")

Нажав на кнопку "Settings" для пакета, вы увидите экран настроек для этого пакета. Здесь у вас есть возможность изменить некоторые переменные по умолчанию для пакета, посмотреть, каковы все сочетания клавиш команды, временно отключить пакет, посмотреть исходный код, посмотреть текущую версию пакета, сообщить о проблемах и удалить пакет.

Если выпущена новая версия любого из ваших пакетов, Atom автоматически обнаружит ее, и вы можете обновить пакет либо с этого экрана, либо с вкладки "Updates". Это поможет вам легко обновлять все установленные пакеты.

#### Atom Themes
**Atom Темы**

Вы также можете найти и установить новые темы для Atom из Settings View. Это могут быть либо темы UI, либо темы Syntax, и вы можете искать их на вкладке "Install", как и при поиске новых пакетов. Обязательно нажмите кнопку "Themes" рядом с окном поиска.

![Theme search screen](../../images/themes.png "Theme search screen")
![Theme search screen](../images/themes.png "Theme search screen")

Нажав на заголовок темы, вы попадете на страницу профиля для темы на atom.io, на которой часто есть скриншот темы. Таким образом, вы можете увидеть, как он выглядит перед установкой.

Нажатие "Install" установит тему и сделает ее доступной в раскрывающихся списках тем, как мы видели в разделе [Смена Темы](/getting-started/sections/atom-basics/#changing-the-theme).

![Example of the Unity UI theme with Monokai syntax theme](../../images/unity-theme.png "Example of the Unity UI theme with Monokai syntax theme")
![Example of the Unity UI theme with Monokai syntax theme](../images/unity-theme.png "Example of the Unity UI theme with Monokai syntax theme")

#### Command Line
**Командная Строка**

Вы также можете установить пакеты или темы из командной строки, используя `apm`.

{{#tip}}

Убедитесь, что вы установили `apm`, запустив следующую команду в вашем терминале:

``` command-line
$ apm help install
```

Вы должны увидеть распечатанное сообщение с подробной информацией о команде `apm install`.

Если вы не видите, вернитесь к разделу [Установка Atom](/getting-started/sections/installing-atom) для получения инструкций о том, как установить команды `atom` и `apm` для вашей системы.

{{/tip}}

Вы также можете установить пакеты с помощью команды `apm install`:

* `apm install <package_name>` установить последнюю версию.
* `apm install <package_name>@<package_version>` установить конкретную версию.

Например, `apm install emmet@0.1.5` устанавливает `0.1.5` выпуск пакета [Emmet](https://github.com/atom/emmet).

Вы также можете использовать `apm`, чтобы найти новые пакеты для установки. Если вы запустите `apm search`, вы можете выполнить поиск в реестре пакетов по запросу.

``` command-line
$ apm search coffee
> Search Results For 'coffee' (29)
> ├── build-coffee Atom Build provider for coffee, compiles CoffeeScript (1160 downloads, 2 stars)
> ├── scallahan-coffee-syntax A coffee inspired theme from the guys over at S.CALLAHAN (183 downloads, 0 stars)
> ├── coffee-paste Copy/Paste As : Js ➤ Coffee / Coffee ➤ Js (902 downloads, 4 stars)
> ├── atom-coffee-repl Coffee REPL for Atom Editor (894 downloads, 2 stars)
> ├── coffee-navigator Code navigation panel for Coffee Script (3493 downloads, 22 stars)
> ...
> ├── language-iced-coffeescript Iced coffeescript for atom (202 downloads, 1 star)
> └── slontech-syntax Dark theme for web developers ( HTML, CSS/LESS, PHP, MYSQL, javascript, AJAX, coffee, JSON ) (2018 downloads, 3 stars)
```

Вы можете использовать `apm view`, чтобы увидеть больше информации о конкретном пакете.

``` command-line
$ apm view build-coffee
> build-coffee
> ├── 0.6.4
> ├── https://github.com/idleberg/atom-build-coffee
> ├── Atom Build provider for coffee, compiles CoffeeScript
> ├── 1152 downloads
> └── 2 stars
>
> Run `apm install build-coffee` to install this package.
```
