---
title: Installing Atom
---
### Installing Atom
**Установка Atom**

Чтобы начать работу с Atom, нам нужно установить его в вашей системе. В этом разделе будет рассказано об установке Atom в вашей системе, а также об основных принципах его сборки из исходного кода.

Установка Atom должна быть довольно простой. Как правило, вы можете перейти на https://atom.io, и вы должны увидеть кнопку загрузки, как показано здесь:

{{#mac}}

![Download buttons on https://atom.io](../../images/mac-downloads.png "Download buttons on https://atom.io")

![Download buttons on https://atom.io](../images/mac-downloads.png "Download buttons on https://atom.io")

{{/mac}}

{{#windows}}

![Download buttons on https://atom.io](../../images/windows-downloads.png "Download buttons on https://atom.io")

![Download buttons on https://atom.io](../images/windows-downloads.png "Download buttons on https://atom.io")

{{/windows}}

{{#linux}}

![Download buttons on https://atom.io](../../images/linux-downloads.png "Download buttons on https://atom.io")

![Download buttons on https://atom.io](../images/linux-downloads.png "Download buttons on https://atom.io")

{{/linux}}

Кнопка или кнопки должны соответствовать вашей платформе, а загружаемый пакет должен легко устанавливаться. Однако, давайте рассмотрим их здесь немного подробнее.

{{#mac}}

#### Installing Atom on Mac
**Установка Atom на Mac**

Atom следует стандартному процессу установки zip на Mac. Вы можете либо нажать кнопку загрузки с сайта https://atom.io либо перейти на [страницу релизов Atom](https://github.com/atom/atom/releases/latest), чтобы явно загрузить файл `atom-mac.zip`. Получив этот файл, вы можете щелкнуть по нему, чтобы извлечь приложение, а затем перетащить новое `Atom` приложение в папку "Приложения".

При первом открытии Atom, он будет пытаться установить `atom` и `apm` команды для использования в терминале. В некоторых случаях Atom может быть не в состоянии установить эти команды, потому что ему нужен пароль администратора. Чтобы проверить, удалось ли Atom установить `atom` команду, например, откройте окно терминала и введите `which atom`. Если `atom` команда была установлена, вы увидите что-то вроде этого:

``` command-line
$ which atom
> /usr/local/bin/atom
$
```

Если команда `atom` не была установлена, команда `which` ничего не вернет:

``` command-line
$ which atom
$
```

Для установки команд `atom` и `apm`, запустите "Window: Install Shell Commands" из [Command Palette](/getting-started/sections/atom-basics#command-palette), которая запросит у вас пароль администратора.

{{/mac}}

{{#windows}}

#### Installing Atom on Windows
**Установка Atom на Windows**

Atom доступен с установщиками Windows, которые можно загрузить с https://atom.io или со [страницы релизов Atom](https://github.com/atom/atom/releases/latest). Используя `AtomSetup.exe` для 32-битных систем и `AtomSetup-x64.exe` для 64-битных систем. Эта программа установки установит Atom, добавит команды `atom` и `apm` к вашему `PATH`, а также создавать ярлыки на рабочем столе и в меню Пуск.

![Atom on Windows](../../images/windows-system-settings.png)
![Atom on Windows](../images/windows-system-settings.png)

Контекстное меню `Open with Atom` в проводнике, и возможность сделать Atom доступным для сопоставления файлов `Open with...`, управляются панелью System Settings как показано выше.

Открыв Atom, нажмите `File > Settings`, а затем вкладку `System` слева. Установите флажки рядом с `Show in file context menus`, а также `Show in folder context menus`. И все готово.

{{/windows}}

{{#linux}}

#### Installing Atom on Linux
**Установка Atom на Linux**

Вы можете установить Atom в Linux, используя менеджер пакетов вашего дистрибутива, настроив его для использования одного из наших официальных репозиториев пакетов. Это также позволит вам обновлять Atom при публикации новых версий.

##### Debian and Ubuntu (deb/apt)
**Debian и Ubuntu (deb/apt)**

Чтобы установить Atom в Debian, Ubuntu или связанных дистрибутивах, добавьте наш официальный репозиторий пакетов в вашу систему, выполнив следующие команды:

``` command-line
$ wget -qO - https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
$ sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
$ sudo apt-get update
```

Теперь вы можете установить Atom используя `apt-get` (или `apt` в Ubuntu):

``` command-line
# Install Atom
$ sudo apt-get install atom

# Install Atom Beta
$ sudo apt-get install atom-beta
```

Кроме того, вы можете скачать [пакет Atom .deb](https://atom.io/download/deb) и установить его напрямую:

``` command-line
# Install Atom
$ sudo dpkg -i atom-amd64.deb

# Install Atom's dependencies if they are missing
$ sudo apt-get -f install
```

##### Red Hat and CentOS (YUM), or Fedora (DNF)
**Red Hat и CentOS (YUM), или Fedora (DNF)**

Чтобы установить Atom в CentOS, Oracle Linux, Red Hat Enterprise Linux, Scientific Linux, Fedora или связанных с ними дистрибутивах, использующих менеджеры пакетов YUM или DNF, добавьте наш официальный репозиторий пакетов в вашу систему, выполнив следующие команды:

``` command-line
$ sudo rpm --import https://packagecloud.io/AtomEditor/atom/gpgkey
$ sudo sh -c 'echo -e "[Atom]\nname=Atom Editor\nbaseurl=https://packagecloud.io/AtomEditor/atom/el/7/\$basearch\nenabled=1\ngpgcheck=0\nrepo_gpgcheck=1\ngpgkey=https://packagecloud.io/AtomEditor/atom/gpgkey" > /etc/yum.repos.d/atom.repo'
```

Теперь вы можете установить Atom, используя `dnf` (или `yum` в зависимости от вашего дистрибутива):

``` command-line
# Install Atom
$ sudo dnf install atom

# Install Atom Beta
$ sudo dnf install atom-beta
```

Кроме того, вы можете скачать [пакет Atom .rpm](https://atom.io/download/rpm) и установить его напрямую:

``` command-line
# On YUM-based distributions
$ sudo yum install -y atom.x86_64.rpm

# On DNF-based distributions
$ sudo dnf install -y atom.x86_64.rpm
```

##### SUSE (zypp)
**SUSE (zypp)**

Чтобы установить Atom в openSUSE или других дистрибутивах, использующих менеджер пакетов Zypp, добавьте наш официальный репозиторий пакетов в вашу систему, выполнив следующие команды:

``` command-line
$ sudo sh -c 'echo -e "[Atom]\nname=Atom Editor\nbaseurl=https://packagecloud.io/AtomEditor/atom/el/7/\$basearch\nenabled=1\ntype=rpm-md\ngpgcheck=0\nrepo_gpgcheck=1\ngpgkey=https://packagecloud.io/AtomEditor/atom/gpgkey" > /etc/zypp/repos.d/atom.repo'
$ sudo zypper --gpg-auto-import-keys refresh
```

Теперь вы можете установить Atom, используя `zypper`:

``` command-line
# Install Atom
$ sudo zypper install atom

# Install Atom Beta
$ sudo zypper install atom-beta
```

Кроме того, вы можете скачать [пакет Atom .rpm](https://atom.io/download/rpm) и установить его напрямую:

``` command-line
$ sudo zypper in -y atom.x86_64.rpm
```

{{/linux}}

#### Updating Atom
**Обновление Atom**

Вы должны периодически обновлять Atom для последних улучшений программного обеспечения. Кроме того, когда Atom получает исправления для уязвимостей системы безопасности, вы захотите обновить свою версию Atom как можно скорее.

{{#mac}}

"Automatically Update" включено по умолчанию в Core Settings в [Settings View](https://flight-manual.atom.io/getting-started/sections/atom-basics/#settings-and-preferences), что позволит Atom автоматически проверять наличие обновлений. Если вы отключите этот параметр, вы можете обновить Atom вручную.

Чтобы выполнить обновление вручную:

* Нажмите на `Atom > Check for Update` пункт меню в строке меню.
* Найдите `Application: About` в [Command Palette](https://flight-manual.atom.io/getting-started/sections/atom-basics/#command-palette) и нажмите кнопку `Check now`.

Atom начнет обновляться, если обновление доступно.

{{/mac}}

{{#windows}}

"Automatically Update" включено по умолчанию в Core Settings в [Settings View](https://flight-manual.atom.io/getting-started/sections/atom-basics/#settings-and-preferences), что позволит Atom автоматически проверять наличие обновлений. Если вы отключите этот параметр, вы можете обновить Atom вручную.

Чтобы выполнить обновление вручную:

* Нажмите на `Help > Check for Update` пункт меню в строке меню.
* Найдите `Application: About` в [Command Palette](https://flight-manual.atom.io/getting-started/sections/atom-basics/#command-palette) и нажмите кнопку `Check now`.

Atom начнет обновляться, если обновление доступно.

{{/windows}}

{{#linux}}

Если вы используете официальные репозитории пакетов Atom, используйте менеджер пакетов вашего дистрибутива для обновления Atom. В противном случае вам нужно будет вручную загрузить и установить последнюю версию `.rpm` или `.deb` пакет с https://atom.io. Для получения дополнительной информации см. [Установка Atom на Linux](https://flight-manual.atom.io/getting-started/sections/installing-atom/#installing-atom-on-linux).

{{/linux}}

#### Portable Mode
**Портативный режим**

Atom хранит конфигурацию и состояние в `.atom` каталоге, обычно расположенном в вашем домашнем каталоге <span class="platform-windows">(`%userprofile%` на Windows)</span>. Однако вы можете запустить Atom в портативном режиме, где и приложение, и конфигурация хранятся вместе, например, на съемном устройстве хранения.

Чтобы настроить Atom в переносном режиме, загрузите [пакет zip/tar.gz для своей системы](https://github.com/atom/atom/releases/latest) и распакуйте его на съемный носитель.

{{#windows}}

Затем создайте `.atom` каталог рядом с каталогом, который содержит atom.exe, например:

```
e:\atom-1.14\atom.exe
e:\.atom
```

{{/windows}}

{{#mac}}

Затем создайте `.atom` каталог вместе с приложением Atom.app, например:

```
/MyUSB/Atom.app
/MyUSB/.atom
```

{{/mac}}

{{#linux}}

Затем создайте `.atom` каталог рядом с каталогом, который содержит двоичный файл Atom, например:

```
/media/myusb/atom-1.14/atom
/media/myusb/.atom
```

{{/linux}}

##### Portable Notes
**Портативные заметки**

- Каталог `.atom` должен быть доступен для записи
- Вы можете переместить существующий `.atom` каталог на ваше портативное устройство
- Atom также может хранить свои пользовательские данные Electron в вашем каталоге `.atom` - просто создайте подкаталог, названый `electronUserData` внутри `.atom`
- В качестве альтернативы вы можете установить `ATOM_HOME` переменную окружения так, чтобы она указывала куда угодно (вы можете написать сценарий .sh или .cmd, чтобы временно установить его и запустить из него)
- Установки в портативном режиме не обновляются автоматически

#### Building Atom from Source
**Сборка Atom'a из исходников**

Раздел [Взлом на Atom Core](/hacking-atom/sections/hacking-on-atom-core/) руководства по полету содержит инструкции по клонированию и созданию исходного кода, если вы предпочитаете эту опцию.

#### Proxy and Firewall Settings
**Настройки прокси и брандмауэра**

##### Behind a Firewall?
**Позади брандмауэра?**

Если вы находитесь за брандмауэром и видите ошибки SSL при установке пакетов, вы можете отключить строгий SSL, выполнив:

``` command-line
$ apm config set strict-ssl false
```

##### Using a Proxy?
**Используете прокси?**

Если вы используете прокси-сервер HTTP(S), вы можете настроить его запустив `apm`:

``` command-line
$ apm config set https-proxy <em>YOUR_PROXY_ADDRESS</em>
```

Вы можете запустить `apm config get https-proxy` чтобы убедиться, что он был установлен правильно.
