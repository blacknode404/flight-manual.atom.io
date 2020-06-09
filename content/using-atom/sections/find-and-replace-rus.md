---
title: Find and Replace
---
### Find and Replace
**Поиск и Замена**

Поиск и замена текста в вашем файле или проекте выполняется быстро и просто в Atom.

* <kbd class="platform-mac">Cmd+F</kbd><kbd class="platform-windows platform-linux">Ctrl+F</kbd> - Поиск в буфере
* <kbd class="platform-mac">Cmd+Shift+F</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+F</kbd> - Поиск по всему проекту

Если вы запустите одну из этих команд, вы увидите панель Find and Replace в нижней части экрана.

![Find and replace text in the current file](../../images/find-replace-file.png "Find and replace text in the current file")
![Find and replace text in the current file](../images/find-replace-file.png "Find and replace text in the current file")

Для поиска в текущем файле вы можете нажать <kbd class="platform-mac">Cmd+F</kbd><kbd class="platform-windows platform-linux">Ctrl+F</kbd>, ввести строку поиска и нажать <kbd class="platform-all">Enter</kbd> (или кнопку <kbd class="platform-mac">Cmd+G</kbd><kbd class="platform-windows platform-linux">F3</kbd> или кнопку "Find") несколько раз, чтобы просмотреть все совпадения в этом файле. <kbd class="platform-all">Alt+Enter</kbd> найдет все вхождения строки поиска. Панель Find and Replace также содержит кнопки для переключения чувствительности к регистру, выполнения сопоставления регулярных выражений, выбора области поиска и выполнения поиска по всему слову.

Если вы введете строку в текстовое поле замены, вы можете заменить совпадения другой строкой. Например, если вы хотите заменить каждый экземпляр строки "Scott" строкой "Dragon", введите эти значения в два текстовых поля и нажмите кнопку "Replace All", чтобы выполнить замены.

{{#note}}

**Примечание:** Atom использует регулярные выражения JavaScript для выполнения поиска по регулярным выражениям.

При выполнении поиска по регулярному выражению синтаксис замены для возврата к группам поиска составляет $1, $2, … $&. Обратитесь к JavaScript [руководству по регулярным выражениям](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions), чтобы узнать больше о синтаксисе регулярных выражений, который вы можете использовать в Atom.

{{/note}}

Вы также можете найти и заменить весь ваш проект, если вы вызываете панель с помощью <kbd class="platform-mac">Cmd+Shift+F</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+F</kbd>.

![Find and replace text in your project](../../images/find-replace-project.png "Find and replace text in your project")
![Find and replace text in your project](../images/find-replace-project.png "Find and replace text in your project")

Это отличный способ узнать, где в вашем проекте вызывается функция, с которой связан якорь или находится конкретная орфографическая ошибка. Нажмите на соответствующую строку, чтобы перейти к этому месту в этом файле.

Вы можете ограничить поиск подмножеством файлов в вашем проекте, введя [glob pattern](https://en.wikipedia.org/wiki/Glob_%28programming%29) в текстовое поле "File/directory pattern". Например, шаблон `src/*.js` будет ограничивать поиск файлами JavaScript в каталоге `src`. Шаблон "globstar" (`**`) может использоваться для сопоставления произвольного количества подкаталогов. Например, `docs/**/*.md` будет соответствовать `docs/a/foo.md`, `docs/a/b/foo.md` и т.д. Вы можете ввести несколько glob patterns, разделенных запятыми, который является полезным для поиска в нескольких типов файлов или подкаталогов.

Если у вас открыто несколько папок проекта, эту функцию также можно использовать для поиска только в одной из этих папок. Например, если у вас есть открытые папки `/path1/folder1` и `/path2/folder2`, вы можете ввести шаблон, только для поиска в `folder1`.

Нажмите, <kbd class="platform-all">Esc</kbd> одновременно сфокусировавшись на панели Find and Replace, чтобы очистить панель от рабочей области.

Функциональность Find and Replace реализована в пакете [find-and-replace](https://github.com/atom/find-and-replace) и использует [scandal](https://github.com/atom/scandal) модуль Node для фактического поиска.
