---
title: Editing and Deleting Text
---
### Editing and Deleting Text
**Редактирование и Удаление Текста**

Итак, мы рассмотрели несколько способов перемещения и выбора областей файла, поэтому теперь давайте на самом деле изменим часть этого текста. Очевидно, что вы можете печатать, чтобы вставить символы, но есть также несколько способов удаления и манипулирования текстом, который может пригодиться.

#### Basic Manipulation
**Основные Манипуляции**

Есть несколько классных комбинаций клавиш, которые могут пригодиться. Они варьируются от перемещения строк текста и дублирующих строк до изменения регистра.

* <kbd class="platform-mac">Cmd+J</kbd><kbd class="platform-windows platform-linux">Ctrl+J</kbd> - Присоединить следующую строку к концу текущей строки
* <kbd class="platform-mac">Cmd+Ctrl+Up/Down</kbd><kbd class="platform-windows platform-linux">Ctrl+Up/Down</kbd> - Переместить текущую строку вверх или вниз
* <kbd class="platform-mac">Cmd+Shift+D</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+D</kbd> - Дублировать текущую строку
* <kbd class="platform-mac">Cmd+K</kbd> <kbd class="platform-mac">Cmd+U</kbd><kbd class="platform-windows platform-linux">Ctrl+K</kbd> <kbd class="platform-windows platform-linux">Ctrl+U</kbd> -Верхний регистр текущего слова
* <kbd class="platform-mac">Cmd+K</kbd> <kbd class="platform-mac">Cmd+L</kbd><kbd class="platform-windows platform-linux">Ctrl+K</kbd> <kbd class="platform-windows platform-linux">Ctrl+L</kbd> - Нижний регистр текущего слова

{{#mac}}

* <kbd class="platform-mac">Ctrl+T</kbd> - Транспонировать персонажей. Это меняет местами два символа по обе стороны от курсора.

{{/mac}}

Atom также имеет встроенную функциональность для перетекания абзаца в жесткую переноску при заданной максимальной длине строки. Вы можете отформатировать текущий выбор, чтобы строки были длиной не более 80 (или любого другого числа  `editor.preferredLineLength`), используя <kbd class="platform-mac">Alt+Cmd+Q</kbd><kbd class="platform-windows platform-linux">Alt+Ctrl+Q</kbd>. Если ничего не выбрано, текущий абзац будет перекрашен.

#### Deleting and Cutting
**Удаление и Вырезание**

Вы также можете удалить или вырезать текст из буфера с помощью некоторых ярлыков. Будь безжалостным.

* <kbd class="platform-mac platform-windows platform-linux">Ctrl+Shift+K</kbd> - Удалить текущую строку
* <span class="platform-mac"><kbd class="platform-mac">Alt+Backspace</kbd> или <kbd class="platform-mac">Alt+H</kbd></span><kbd class="platform-windows platform-linux">Ctrl+Backspace</kbd> - Удалить до начала слова
* <span class="platform-mac"><kbd class="platform-mac">Alt+Delete</kbd> или <kbd class="platform-mac">Alt+D</kbd></span><kbd class="platform-windows platform-linux">Ctrl+Delete</kbd> - Удалить до конца слова

{{#mac}}

* <kbd class="platform-mac">Cmd+Delete</kbd> - Удалить до конца строки
* <kbd class="platform-mac">Ctrl+K</kbd> - Вырезать до конца строки
* <kbd class="platform-mac">Cmd+Backspace</kbd> - Удалить до начало строки

{{/mac}}

#### Multiple Cursors and Selections
**Несколько Курсоров и Выборка**

Одна из замечательных вещей, которую Atom может сделать из коробки, - поддержка нескольких курсоров. Это может быть невероятно полезно при работе с длинными списками текста.

* <kbd class="platform-mac">Cmd+Click</kbd><kbd class="platform-windows platform-linux">Ctrl+Click</kbd> - Добавить новый курсор в выбранном месте
* <kbd class="platform-mac">Ctrl+Shift+Up/Down</kbd><kbd class="platform-windows">Alt+Ctrl+Up/Down</kbd><kbd class="platform-linux">Alt+Shift+Up/Down</kbd> - Добавить еще один курсор выше / ниже текущего курсора
* <kbd class="platform-mac">Cmd+D</kbd><kbd class="platform-windows platform-linux">Ctrl+D</kbd> -  Выберите следующее слово в документе, которое совпадает с текущим выбранным словом
* <kbd class="platform-mac">Cmd+Ctrl+G</kbd><kbd class="platform-windows platform-linux">Alt+F3</kbd> - Выберите все слова в документе, которые совпадают с текущим выбранным словом

{{#mac}}

* <kbd class="platform-mac">Cmd+Shift+L</kbd> - Преобразование многострочного выделения в несколько курсоров

{{/mac}}

Используя эти команды, вы можете размещать курсоры в нескольких местах документа и эффективно выполнять одни и те же команды в нескольких местах одновременно.

![Using multiple cursors](../../images/multiple-cursors.gif)
![Using multiple cursors](../images/multiple-cursors.gif)

Это может быть невероятно полезно при выполнении множества повторяющихся задач, таких как переименование переменных или изменение формата некоторого текста. Вы можете использовать это практически с любым плагином или командой - например, изменяя регистр и перемещая или дублируя строки.

Вы также можете использовать мышь для выбора текста с нажатой клавишей <kbd class="platform-mac">Cmd</kbd><kbd class="platform-windows platform-linux">Ctrl</kbd>, чтобы выделить несколько областей вашего текста одновременно.

#### Whitespace
**Пробелы**

Atom поставляется с несколькими командами, которые помогут вам управлять пробелами в вашем документе. Одна очень полезная пара команд преобразует начальные пробелы в табуляцию и преобразует начальные пробелы в пробелы. Если вы работаете с документом со смешанным пробелом, эти команды отлично подходят для нормализации файла. Для команд пробелов нет привязок клавиш, поэтому вам придется искать в Command Palette "Convert Spaces to Tabs" (или наоборот), чтобы выполнить одну из этих команд.

Команды пробела реализованы в пакете [atom/whitespace](https://github.com/atom/whitespace). Настройки для команд пустого пространства управляются на странице пакета `whitespace`.

![Managing your whitespace settings](../../images/whitespace.png)
![Managing your whitespace settings](../images/whitespace.png)

{{#note}}

Параметр "Remove Trailing Whitespace" включен по умолчанию. Это означает, что каждый раз, когда вы сохраняете любой файл, открытый в Atom, он удаляет все завершающие пробелы из файла. Если вы хотите отключить это, перейдите к пакету `whitespace` на панели настроек и снимите этот флажок.

{{/note}}

Atom также по умолчанию обеспечит наличие в вашем файле завершающего символа новой строки. Вы также можете отключить эту опцию на этом экране.

#### Brackets
**Скобки**
{dasdasd}
[asdasdasd]
(asdasd)
Atom поставляется с интеллектуальным и простым в использовании кронштейном.

По умолчанию он будет выделять `[]`, `()`, и `{}` стилизовать скобки, когда ваш курсор находится над ними. Также будут выделены совпадающие теги XML и HTML.

Atom автоматически закрывает `[]`, `()`, еще `{}`, `""`, `''`, `“”`, `‘’`, `«»`, `‹›`, при вводе начальной. Если у вас есть выделенная строка, и вы вводите любую из этих открывающих скобок или кавычек, Atom заключит выделенную строку в открывающую и закрывающую скобки или кавычки.

Есть несколько других интересных команд, связанных с квадратными скобками, которые вы можете использовать.

* <kbd class="platform-mac platform-windows platform-linux">Ctrl+M</kbd> - Перейти к скобке, соответствующей той, которая находится рядом с курсором. Он переходит к ближайшей скобке, когда нет соседней скобки.
* <kbd class="platform-mac">Cmd+Ctrl+M</kbd><kbd class="platform-windows platform-linux">Alt+Ctrl+,</kbd> - Выделите весь текст в текущих скобках.
* <kbd class="platform-mac">Alt+Cmd+.</kbd><kbd class="platform-windows platform-linux">Alt+Ctrl+.</kbd> - Закрыть текущий тег XML/HTML.

Функциональность скобок реализована в пакете [bracket-matcher](https://github.com/atom/bracket-matcher). Как и во всех этих пакетах, чтобы изменить значения по умолчанию, связанные с обработкой скобок, или полностью отключить его, вы можете перейти к этому пакету в Settings View.

#### Encoding
**Кодировка**

Atom также поставляется с некоторой базовой поддержкой кодирования файлов, если вы обнаружите, что работаете с файлами не в кодировке UTF-8, или если вы хотите создать один.

* <kbd class="platform-mac platform-windows">Ctrl+Shift+U</kbd><kbd class="platform-linux">Alt+U</kbd> - Переключить меню, чтобы изменить кодировку файла

Если вы откроете диалоговое окно кодировки файлов, вы можете выбрать альтернативную кодировку файлов для сохранения вашего файла.

Когда вы открываете файл, Atom попытается автоматически определить кодировку. Если Atom не может определить кодировку, кодировка по умолчанию будет UTF-8, которая также является кодировкой по умолчанию для новых файлов.

![Changing your file encoding](../../images/encodings.png)
![Changing your file encoding](../images/encodings.png)

Если вы откроете меню кодирования и измените активную кодировку на другую, файл будет записан в этой кодировке при следующем сохранении файла.

Селектор кодирования реализован в пакете [encoding-selector](https://github.com/atom/encoding-selector).
