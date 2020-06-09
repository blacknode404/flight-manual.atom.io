---
title: Snippets
---
### Snippets
**Фрагменты Кода**

Фрагменты кода являются невероятно мощным способом быстрой генерации часто необходимого синтаксиса кода из ярлыка.

Идея заключается в том , что вы можете ввести что - то вроде `habtm`, а затем нажмете кнопку <kbd class="platform-all">Tab</kbd>, и она будет расширяться в `has_and_belongs_to_many`.

Многие Core Packages и Community Packages поставляются в комплекте со своими собственными фрагментами, специфичными для него. Например, пакет  `language-html`, который обеспечивает поддержку подсветки синтаксиса HTML и грамматики, поставляется с десятками фрагментов для создания множества различных тегов HTML, которые вы, возможно, захотите использовать. Если вы создаете новый HTML-файл в Atom, вы можете ввести, `html` а затем нажать, <kbd class="platform-all">Tab</kbd> и, если вы не устанавливали других плагинов перекрывающих этот фрагмент, он расширится до:

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>

  </body>
</html>
```

Он также установит курсор в значение атрибута `lang`, чтобы вы могли редактировать его при необходимости. Многие фрагменты имеют несколько точек фокусировки, через которые вы также можете перемещаться с помощью клавиши <kbd class="platform-all">Tab</kbd> - например, в случае этого фрагмента HTML, после того, как курсор помещен в значение атрибута `lang` вы можете продолжить нажатие <kbd class="platform-all">Tab</kbd> и курсор перейдет в значение атрибута `dir`, затем к середине тега `title`, затем, наконец, к середине тега `body`.

Чтобы просмотреть все доступные фрагменты для типа файла, который у вас открыт в данный момент, выберите "Snippets: Available" в Command Palette.

![View all available snippets](../../images/snippets.png "View all available snippets")
![View all available snippets](../images/snippets.png "View all available snippets")

Вы также можете использовать Fuzzy Finder, чтобы отфильтровать этот список, введя в поле выбора. Выбор одного из них выполнит фрагмент, где находится ваш курсор (или несколько курсоров).

#### Creating Your Own Snippets
**Создание Ваших Собственных Фрагментов**

Так что это круто, но что, если есть что-то, чего не включил языковой пакет, или что-то нестандартное для написанного вами кода? К счастью, невероятно легко добавлять свои собственные фрагменты.

В вашем каталоге <span class="platform-mac platform-linux">`~/.atom`</span> <span class="platform-windows">`%USERPROFILE%\.atom`</span> есть текстовый файл `snippets.cson`, который содержит все ваши пользовательские фрагменты, которые загружаются при запуске Atom. Вы также можете легко открыть этот файл, выбрав пункт <span class="platform-mac">_Atom > Snippets_</span> | <span class="platform-linux">_Edit > Snippets_</span> | <span class="platform-windows">_File > Snippets_</span>.

##### Snippet Format
**Формат Фрагмента**

Итак, давайте посмотрим, как написать фрагмент. Основной формат фрагмента выглядит следующим образом:

```coffee
'.source.js':
  'console.log':
    'prefix': 'log'
    'body': 'console.log(${1:"crash"});$2'
```

Крайние левые ключи - это селекторы, в которых эти фрагменты должны быть активными. Самый простой способ определить, что это должно быть, - перейти к языковому пакету языка, для которого вы хотите добавить фрагмент кода, и найти строку "Scope".

Например, если мы хотим добавить фрагмент, который будет работать для файлов Java, мы бы посмотрели пакет `language-java` в нашем Settings View и увидели, что Scope у нас `source.java`. Тогда ключом фрагмента верхнего уровня будет `source.java`, которому предшествует точка (как сделал бы селектор класса CSS).

![Finding the selector scope for a snippet](../../images/snippet-scope.png "Finding the selector scope for a snippet")
![Finding the selector scope for a snippet](../images/snippet-scope.png "Finding the selector scope for a snippet")

Следующим ключом является имя фрагмента. Оно используется для описания фрагмента в более читаемом виде в меню фрагмента. Вы можете назвать их как хотите.

Под каждым именем фрагмента находится элемент `prefix`, который должен запускать фрагмент, и элемент `body`, вставляемый при запуске фрагмента.

Каждый, `$` за которым следует номер, является табуляцией. Остановки табуляции циклически повторяются нажатием <kbd class="platform-all">Tab</kbd> после запуска фрагмента.

Закладки с одинаковым номером создадут несколько курсоров.

Приведенный выше пример добавляет `log` фрагмент к файлам JavaScript, который будет расширяться до:

```javascript
console.log("crash");
```

Первоначально будет выбрана строка `"crash"`, и при повторном нажатии клавиши Tab будет установлен курсор после `;`

{{#warning}}

Ключи фрагментов, в отличие от селекторов CSS, могут повторяться только один раз для каждого уровня. Если на том же уровне есть дубликаты ключей, то будет прочитан только последний. см. [Настройка с CSON](/using-atom/sections/basic-customization/#configuring-with-cson) для получения дополнительной информации.

{{/warning}}

##### Multi-line Snippet Body
**Многострочный Фрагмент Кода**

Вы можете также использовать [многострочный синтаксис CoffeeScript](http://coffeescript.org/#strings), используя `"""` для больших шаблонов:

```coffee
'.source.js':
  'if, else if, else':
    'prefix': 'ieie'
    'body': """
      if (${1:true}) {
        $2
      } else if (${3:false}) {
        $4
      } else {
        $5
      }
    """
```

Как и следовало ожидать, есть фрагмент для создания фрагментов. Если вы откроете файл `snippets.cson`, наберете `snip` а затем нажмете <kbd class="platform-all">Tab</kbd>, вы получите следующий текст:

```coffee
'.source.js':
  'Snippet Name':
    'prefix': 'hello'
    'body': 'Hello World!'
```

Просто заполните своими данными, и у вас будет фрагмент. Как только вы сохраните файл, Atom должен перезагрузить фрагменты, и вы сразу сможете его опробовать.

##### Multiple Snippets per Source
**Несколько Фрагментов на Источник**

Ниже вы можете увидеть формат для включения нескольких фрагментов для одной и той же области в вашем файле `snippets.cson`. Просто включите имя фрагмента, префикс и ключи тела для дополнительных фрагментов внутри ключа области действия:

```coffee
'.source.gfm':
  'Hello World':
    'prefix': 'hewo'
    'body': 'Hello World!'

  'Github Hello':
    'prefix': 'gihe'
    'body': 'Octocat says Hi!'

  'Octocat Image Link':
    'prefix': 'octopic'
    'body': '![GitHub Octocat](https://assets-cdn.github.com/images/modules/logos_page/Octocat.png)'
```

Снова, смотрите [Настройка с CSON](/using-atom/sections/basic-customization/#configuring-with-cson) для получения дополнительной информации о структуре ключа CSON и неповторяемости.

#### More Info
**Больше Информации**

Функциональность фрагментов реализована в пакете [snippets](https://github.com/atom/snippets).

Дополнительные примеры см. в фрагментах пакетов [language-html](https://github.com/atom/language-html/blob/master/snippets/language-html.cson) и [language-javascript](https://github.com/atom/language-javascript/blob/master/snippets/language-javascript.cson).
