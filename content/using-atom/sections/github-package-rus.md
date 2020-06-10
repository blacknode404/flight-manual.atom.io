---
title: GitHub package
---
### GitHub package
**Пакет GitHub**

Пакет github обеспечивает интеграцию Git и GitHub прямо внутри Atom.

- [Initialize / Инициализация](#initialize-repositories)
- [Clone / Клон](#clone-repositories)
- [Branch / Ветвь](#branch)
- [Stage / Постановка](#stage)
- [Discard / Отменить](#discard-changes)
- [Commit / Коммит](#commit)
- [Amend and undo / Изменить и отменить](#amend-and-undo)
- [Publish and push / Опубликовать и продовить](#publish-and-push)
- [Fetch and pull / Получить и вытащить](#fetch-and-pull)
- [Resolve conflicts / Разрешить конфликты](#resolve-conflicts)
- [Create a Pull Request / Создать запрос на извлечение](#create-a-pull-request)
- [View Pull Requests / Просмотр запросов на извлечение](#view-pull-requests)
- [Checkout a Pull Request / Оформить запрос на извлечение](#checkout-a-pull-request)
- [Open any Issue or Pull Request / Откройте любой вопрос или запрос на извлечение](#open-any-issue-or-pull-request)
- [View Pull Request review comments / Просмотреть комментарии по запросу на Pull](#view-pull-request-review-comments)
- [Navigate Pull Request review comments / Navigate Pull Request обзор комментариев](#navigate-pull-request-review-comments)
- [Respond to a Pull Request review comment / Ответить на комментарий к запросу о вытягивании](#respond-to-a-pull-request-review-comment)

Большая часть функциональности находится в элементах стыковки Git и GitHub.

![The Git and GitHub panels](../../images/github-panels.png "The Git and GitHub panels")
![The Git and GitHub panels](../images/github-panels.png "The Git and GitHub panels")

Есть разные способы доступа к ним, вероятно, самый распространенный способ - через их сочетания клавиш:

- Откройте панель **Git**: <kbd class=".platform-all">Ctrl+9</kbd>
- Откройте панель **GitHub**: <kbd class=".platform-all">Ctrl+8</kbd>

Другой способ из меню: `Packages -> GitHub -> Toggle Git Tab и Toggle GitHub Tab`

Или вы также можете переключить панель Git из строки состояния, нажав на значок измененных файлов:

![Open Git panel](../../images/github-open-git-panel.png "Open Git panel")
![Open Git panel](../images/github-open-git-panel.png "Open Git panel")


---

#### Initialize repositories
**Инициализировать репозитории**

Если у проекта еще нет репозитория Git, вы можете создать его из панели Git.

![Initialize repositories](../../images/github-initialize.png "Initialize repositories")
![Initialize repositories](../images/github-initialize.png "Initialize repositories")


#### Clone repositories
**Клонирование репозиториев**

Чтобы клонировать репозиторий, откройте панель GitHub, когда у вас нет открытых папок проекта в Atom, и нажмите "Clone an existing GitHub repository". В диалоговом окне вставьте URL-адрес хранилища и нажмите "Clone". Новый проект будет добавлен в Tree View.

![GitHub panel](../../images/github-without-projects.png "GitHub panel without projects")
![GitHub panel](../images/github-without-projects.png "GitHub panel without projects")

![Clone dialog](../../images/github-clone.png "Clone repositories")
![Clone dialog](../images/github-clone.png "Clone repositories")

В качестве альтернативы, запустите команду `GitHub: Clone`, чтобы в любое время открыть диалог клонирования.

#### Branch
**Ветвь**

Чтобы открыть подсказку о ветке, щелкните значок ветки в Status Bar. Оттуда вы можете **create** или **switch** ветвь.

![Create or switch branches](../../images/github-branch.png "Create or switch branches")
![Create or switch branches](../images/github-branch.png "Create or switch branches")


#### Stage
**Постановка**

После внесения некоторых изменений, **stage** все, что хотите, чтобы стать частью следующего коммита. Выбирай между постановкой...

- **All changes**: нажмите кнопку "Stage All" на панели "Unstaged Changes".
- **Files**: дважды щелкните файл или выберите файл и нажмите <kbd class=".platform-all">Enter</kbd>.
- **Hunk**: нажмите кнопку "Stage Hunk" или выберите блок и нажмите <kbd class=".platform-all">Enter</kbd>.
- **Lines**: нажмите на линию (или перетащите на несколько строк), чтобы выбрать, затем нажмите кнопку "Stage Selection". Или используйте клавишу <kbd class="platform-mac">Cmd-/</kbd><kbd class="platform-windows platform-linux">Cmd-/</kbd> для переключения из режима блокировки в режим строки, а затем нажмите <kbd class="platform-mac">Cmd-Enter</kbd><kbd class="platform-windows platform-linux">Ctrl-Enter</kbd>, чтобы поставить только одну строку.

Используйте клавишу со стрелкой <kbd class="platform-mac">Cmd-Left</kbd><kbd class="platform-windows platform-linux">Ctrl-Left</kbd> или <kbd class="platform-mac">Cmd-Right</kbd><kbd class="platform-windows platform-linux">Ctrl-Right</kbd> для переключения между списком файлов и Diff View. Unstaging может быть сделано таким же образом.

![Stage changes](../../images/github-stage.png "Stage changes")
![Stage changes](../images/github-stage.png "Stage changes")


#### Discard changes
**Отменить изменения**

Если вы больше не хотите сохранять какие-либо изменения, вы можете отменить их. Это похоже на постановку, но доступно через контекстное меню.

- **All changes**: щелкните меню <kbd>...</kbd> в заголовке "Unstaged Changes" и выберите "Discard All Changes".
- **Files**: щелкните правой кнопкой мыши файл (или несколько файлов) и выберите "Discard Changes".
- **Hunk**: нажмите на значок корзины в верхней панели hunk.
- **Lines**: щелкните правой кнопкой мыши по строке (или нескольким) и выберите "Discard Selection".

![Discard changes](../../images/github-discard.png "Discard changes")
![Discard changes](../images/github-discard.png "Discard changes")


#### Commit Preview
**Коммит предварительный просмотр**

Чтобы дважды проверить **all changes**, которые будут внесены в ваш следующий коммит, нажмите кнопку "**See All Staged Changes**" над окном сообщения фиксации. Это позволяет вам увидеть все ваши поэтапные изменения в одной панели. Этот "commit preview" может также послужить источником вдохновения для написания сообщения о фиксации.

![Commit Preview](../../images/github-commit-preview.png "Commit Preview")
![Commit Preview](../images/github-commit-preview.png "Commit Preview")


#### Commit
**Коммит**

После внесения изменений введите **message** о коммите. Не стесняйтесь описывать коммит более подробно, оставляя пустую строку. Завершите, нажав кнопку **Commit**. Если вам нужно больше места, щелкните значок расширения в правом нижнем углу. Откроется редактор коммитов в центре.

![Commit changes](../../images/github-commit.png "Commit changes")
![Commit changes](../images/github-commit.png "Commit changes")

Чтобы добавить нескольких **co-authors** в коммит, нажмите кнопку-значок "👤➕" в левом нижнем углу редактора сообщений о коммитах. Теперь вы можете выполнять поиск по имени, электронной почте или имени пользователя GitHub, чтобы отдать должное соавтору.

![Commit with co-authors](../../images/github-commit-with-co-authors.png "Commit with co-authors")
![Commit with co-authors](../images/github-commit-with-co-authors.png "Commit with co-authors")


#### Amend and undo
**Изменить и отменить**

Если вы забыли зафиксировать изменение и хотите добавить его в свой предыдущий коммит, щелкните правой кнопкой мыши последний коммит, затем выберите "Amend" в контекстном меню.

![Amend previous commit](../../images/github-amend.png "Amend previous commit")
![Amend previous commit](../images/github-amend.png "Amend previous commit")

Если вы хотите отредактировать сообщение о вашем последнем коммите или добавить / удалить изменения, нажмите кнопку "Undo". Он вернется к состоянию непосредственно перед тем, как вы нажмете кнопку фиксации.

![Undo previous commit](../../images/github-undo.png "Undo previous commit")
![Undo previous commit](../images/github-undo.png "Undo previous commit")

#### View commits
**Посмотреть коммиты**

После того, как вы сделали некоторые коммиты, нажмите на сообщение коммита в списке недавних коммитов, чтобы увидеть полный Diff и сообщение о коммите, связанное с каждым:

![View commit detai](../../images/github-commit-detail.png "View commit detai")
![View commit detai](../images/github-commit-detail.png "View commit detai")

#### Publish and push
**Опубликовать и продовить**

Когда вы будете готовы поделиться своими изменениями с членами вашей команды, нажмите кнопку **Publish** в Status Bar. Это подтолкнет вашу локальную ветку к удаленному хранилищу. После того, как вы сделаете больше коммитов, вы также можете **Push** их из Status Bar.

![Publish and push commits](../../images/github-publish-push.png "Publish and push commits")
![Publish and push commits](../images/github-publish-push.png "Publish and push commits")


#### Fetch and pull
**Получить и вытащить**

Время от времени хорошей идеей будет нажимать на кнопку **Fetch**, чтобы посмотреть, не изменил ли кто-либо другой член команды. Если это так, нажмите **Pull**, чтобы объединить изменения с вашей локальной веткой.

![Fetch and pull commits](../../images/github-fetch-pull.png "Fetch and pull commits")
![Fetch and pull commits](../images/github-fetch-pull.png "Fetch and pull commits")

Если вы предпочитаете делать **rebase** при извлечении, вы можете настроить Git, чтобы сделать его поведением по умолчанию:

```
git config --global --bool pull.rebase true
```

Узнайте больше о [merge vs. rebase](https://mislav.net/2013/02/merge-vs-rebase/).

#### Resolve conflicts
**Разрешить конфликты**

Иногда могут возникнуть конфликты при попытке слияния. Файлы с конфликтами при слиянии будут отображаться в списке "Merge Conflicts". Нажмите на файл, чтобы открыть редактор. Там вы можете **resolve** конфликт путем выбора версии или внесения дополнительных изменений. Как только вы закончите, подготовьте файл и зафиксируйте его.

![Resolve conflicts](../../images/github-resolve-conflicts.png "Resolve conflicts")
![Resolve conflicts](../images/github-resolve-conflicts.png "Resolve conflicts")


#### Create a Pull Request
**Создать запрос на извлечение**

Когда ваши изменения будут готовы для проверки членами вашей команды, откройте панель "GitHub" <kbd>Ctrl+8</kbd> и нажмите **Open new pull request**. Откроется браузер, в котором вы можете продолжить создание запроса. Если коммиты не были отправлены или ветка еще не опубликована, пакет GitHub сделает это автоматически для вас.

![Create a Pull Request](../../images/github-create-a-pull-request.png "Create a Pull Request")
![Create a Pull Request](../images/github-create-a-pull-request.png "Create a Pull Request")


#### View Pull Requests

Once the pull request is created, it will appear under **Current pull request** at the top of the panel. Underneath is a list of **Open pull requests**. It lets you quickly find a pull request by avatar, title or PR number. It also lets you keep an eye on the CI status. Clicking on a pull request in the list opens a center pane with more details, the timeline and conversations.

![View Pull Requests](../../images/github-view-pull-requests.png "View Pull Requests")
![View Pull Requests](../images/github-view-pull-requests.png "View Pull Requests")


#### Open any Issue or Pull Request

You can open issues or pull requests from any repo on GitHub. To do so, run the `GitHub: Open Issue Or Pull Request` command and paste the URL from an issue or pull request. Then press the **Open Issue or Pull Request** button and it will open a center pane. This lets you keep an issue or pull request as a reference, when working in another repo.

![Open Issue or Pull Request](../../images/github-open-issue-or-pull-request.png "Open Issue or Pull Request")
![Open Issue or Pull Request](../images/github-open-issue-or-pull-request.png "Open Issue or Pull Request")


#### Checkout a Pull Request

To test a pull request locally, open it in the workspace center by clicking on the pull request in the "open pull requests" list from the GitHub tab, then click on the **Checkout** button. It will automatically create a local branch and pull all the changes. If you would like to contribute to that pull request, start making changes, commit and push. Your contribution is now part of that pull request.

![Checkout a pull request](../../images/github-checkout.png "Checkout a pull request")
![Checkout a pull request](../images/github-checkout.png "Checkout a pull request")

#### View Pull Request review comments

To view review comments on a Pull Request, open the Reviews Tab from the **See Reviews** button from the footer of a Pull Request Pane. Alternatively, if the pull request has already been checked out, Reviews Tab can also be open from the same button on GitHub Tab.

![Open review tab from footer](../../images/github-see-review-footer.png "Open review tab from footer")
![Open review tab from footer](../images/github-see-review-footer.png "Open review tab from footer")

#### Navigate Pull Request review comments

You can see all the review summaries and comments of a pull request in the Reviews Tab. The comment section has a progress bar to help you keep track of how close are you to finish addressing the Pull Request comments (i.e. marking all comment threads on a Pull Request as "resolved"). Comment threads are greyed out after they have been resolved.

![Review tab](../../images/github-review-tab.png "Review tab")
![Review tab](../images/github-review-tab.png "Review tab")

After the pull request branch has been checked out, you can click **Jump To File** to open the commented on file and make changes as per the review comment right in the editor. If you would like to get the full context of the review comment, click **Open Diff** to open the diff view with line highlighting.

![Jump to file from review tab](../../images/github-review-jump-to-file.png "Jump to file from review tab")
![Jump to file from review tab](../images/github-review-jump-to-file.png "Jump to file from review tab")

Conversely, in-editor comments are indicated by the comment icon in the gutter. Clicking the icon, either from within the editor or the diff view, will take you back to the Reviews Tab.

![Open review tab from diff](../../images/github-open-review-from-diff.png "Open review tab from diff")
![Open review tab from diff](../images/github-open-review-from-diff.png "Open review tab from diff")

#### Respond to a Pull Request review comment

To respond to a Pull Request review comment, type your message and click **Comment**; a single line comment will be created in the same thread as the comment you responded to. After addressing a Pull Request review comment, click **Resolve conversation** to mark the whole thread as "resolved". The progress bar in the "Comments" section will update accordingly.

![Respond to a Pull Request review comment](../../images/github-review-reply.png "Respond to a Pull Request review comment")
![Respond to a Pull Request review comment](../images/github-review-reply.png "Respond to a Pull Request review comment")
