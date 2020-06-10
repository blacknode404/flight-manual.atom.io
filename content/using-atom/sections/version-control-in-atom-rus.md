---
title: Version Control in Atom
---
### Version Control in Atom
**Контроль Версий в Atom**

Контроль версий является важным аспектом любого проекта, и Atom поставляется со встроенной базовой интеграцией [Git](https://git-scm.com) и [GitHub](https://github.com).

Чтобы использовать контроль версий в Atom, в корне проекта должен быть репозиторий Git.

#### Checkout HEAD revision
**Оформить заказ HEAD revision**

В привязках <kbd class="platform-mac">Alt+Cmd+Z</kbd><kbd class="platform-windows platform-linux">Alt+Ctrl+Z</kbd> проверяется на `HEAD` пересмотр файла в редакторе.

Это быстрый способ отменить все внесенные вами сохраненные и поэтапные изменения и восстановить файл до версии в коммите `HEAD`. Это, по существу так, как работает `git checkout HEAD -- <path>` и `git reset HEAD -- <path>` из командной строки для этого пути.

![Git checkout `HEAD`](../../images/git-checkout-head.gif "Git checkout `HEAD`")
![Git checkout `HEAD`](../images/git-checkout-head.gif "Git checkout `HEAD`")

Эта команда попадает в стек отмены, поэтому вы можете, впоследствии использовать ее для восстановления предыдущего содержимого с помощью отмены <kbd class="platform-mac">Cmd+Z</kbd><kbd class="platform-windows platform-linux">Ctrl+Z</kbd>.

#### Git status list
**Список статуса Git**

Atom поставляется с пакетом [fuzzy-finder](https://github.com/atom/fuzzy-finder) который позволяет быстро открывать файлы в проекте <kbd class="platform-mac">Cmd+T</kbd><kbd class="platform-windows platform-linux">Ctrl+T</kbd> и переходить к любому открытому редактору <kbd class="platform-mac">Cmd+B</kbd><kbd class="platform-windows platform-linux">Ctrl+B</kbd>. Пакет также предоставляет список всех неотслеживаемых и измененных файлов в проекте <kbd class="platform-mac">Cmd+Shift+B</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+B</kbd>. Это будут те же файлы, которые вы увидите в командной строке, если вы запустите `git status`.

![Git status list](../../images/git-status.gif "`git status` list")
![Git status list](../images/git-status.gif "`git status` list")

Справа от каждого файла появится значок, указывающий, был ли он отслежен или изменен.

#### Commit editor
**Редактор коммитов**

Atom может использоваться в качестве редактора коммитов Git и поставляется с пакетом [language-git](https://github.com/atom/language-git), который добавляет подсветку синтаксиса к отредактированным сообщениям коммитов, слияний и перебазирования.

![Git commit message highlighting](../../images/git-message.gif "Git commit message highlighting")
![Git commit message highlighting](../images/git-message.gif "Git commit message highlighting")

Вы можете настроить Atom как редактор коммитов Git с помощью следующей команды:

``` command-line
$ git config --global core.editor "atom --wait"
```

Пакет [language-git](https://github.com/atom/language-git) поможет напомнить вам краткость, раскрасив первые строки сообщений коммита, когда они длиннее 50 или 65 символов.

#### Status bar icons
**Значки строки состояния**

Пакет [status-bar](https://github.com/atom/status-bar), который поставляется с Atom, включает в себя несколько украшений Git, которые отображаются в правой части строки состояния:

![Git Status Bar decorations](../../images/git-status-bar.png "Git Status Bar decorations")
![Git Status Bar decorations](../images/git-status-bar.png "Git Status Bar decorations")

Текущее извлеченное имя ветки отображается с количеством коммитов, ветвь которой находится перед или позади ее восходящей ветки. Значок добавляется, если файл не отслежен, изменен или проигнорирован. Количество строк, добавленных и удаленных с момента последней фиксации файла, также будет отображено.

#### Line diffs
**Линия различий**

Пакет [git-diff](https://github.com/atom/git-diff) раскрашивает желоб рядом со строками, которые были добавлены, отредактированы или удалены.

![Git line diff indications](../../images/git-lines.png "Git line diff indications")
![Git line diff indications](../images/git-lines.png "Git line diff indications")

тот пакет также добавляет <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">Down</kbd> и <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">Up</kbd> сочетания клавиш, которые позволяют перемещать курсор к следующему или предыдущему различию в текущем редакторе.

#### Open on GitHub
**Открыть на GitHub**

Если проект, над которым вы работаете, находится на GitHub, есть также несколько очень полезных интеграций, которые вы можете использовать. Большинство команд берет текущий просматриваемый файл и открывает представление этого файла на GitHub - например, историю обвинений или фиксации этого файла.

* <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">O</kbd> - Открыть файл на GitHub
* <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">B</kbd> - Открыть Blame просмотр файла на GitHub
* <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">H</kbd> - Открыть историю просмотра файла на GitHub
* <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">C</kbd> - Скопируйте URL текущего файла на GitHub в буфер обмена.
* <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">R</kbd> - Сравнение веток на GitHub

Сравнение ветвей показывает, что коммиты находятся в той ветке, над которой вы сейчас работаете локально, а не в основной ветке.

![Open Blame of file on GitHub](../../images/open-on-github.png "Open Blame of file on GitHub")
![Open Blame of file on GitHub](../images/open-on-github.png "Open Blame of file on GitHub")
