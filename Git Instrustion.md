![Logo](Git-Logo-1788C.png)
# Работа с Git #

## 1. Проверка наличия установленного Git
В терминале выполнить команду `git version`
Если Git установлен, появится сообщение с указанием информациии о версии программы. Иначе будет сообщение об ошибке.

## 2. Установка Git
Загружаем последнюю версию Git с сайта https://git-scm.com/dounloads. Устанавливаем с настройками поумолчанию.

## 3. Инициализация Git, создание репозитория

Инициализация/создание репозитория Git  возможно двумя способами:необходимо использовать команду 
### 3.1. Создание.
 В терминали переходим к папке , в которой хотим создать репозиторий.
```
git init
```
В исходной папке появится скрытая папка - файл   *.git*

### 3.2. Клонирование.
Клонировать существующий репозиторий. Для этого используется команда:
```
git clone <адрес репозитория>
```
Файлы, которые должны быть использованы Git, создаются с раширением .md.

## 4. Настройка Git
При первомм использовании Git необходимо представиться. Для этого нужно ввести две команды:
```
 git config --global user.name «Ваше имя английскими буквами»

git config --global user.email ваша почта@example.com
```

## 5. Сохранение репозитория, отслеживание состояния файла/репозитория

Для сохранения текущей версии файла использовать команду 
```
git add 
```
Для отслеживания статуса файла/репозитория использовать команду 
```
git status.
```

## 6. Фиксация изменений репозитория, создание коммитов

### 6.1. Для фиксации (записи) изменений репозитория используется команда:
```
git commit -m <описание изменений, которые надо зафиксировать>
```
### 6.2. Можно использовать команду, которая  позволяет одновременно формировать коммит и сохранять текущую версию файл:
```
git commit -am <описание изменений, которые надо зафиксировать>
```
Такой вариант сокращает количество операций.

### 6.3. Отслеживание версий (commit) при помощи логирования (log)
Для получения в терминале инфомрации о сохраненных версиях файла используем команду 
```
git log
или
git log --oneline
```
Для получения наглядной картины можно использовать графическое представление версий файл с помощью команды 
```
git log --graph
```
Возможно использование комбинированной команды для наглядного представления версионности файла
```
git log --graph --oneline
```
Для получения информации одновременно о версиях файла и о том, на каких ветках они выполнялись,используем команду:
 ```
git reflog
```
## 7. Работа с изображениями

### 7.1. Вставка файла с изборажением
Чтобы вставить изображения (логотип в начале текста) надо написать следующую команду:
```
 ![Лого](Git-Logo-1788C.png) 
```
В квадратных скобках - текст, который отобразится, в круглых скобках - имя файла с изображением.
Если все правильно будет картинка, если нет - то слово в квадратных скобках (в данном случае Лого)

### 7.2. Отключение функции отслеживания файла (в т.ч. c изображением) (игнорирование).

Для игнорирования файла необходимо создать в репозитории файл `_.gitignore.`
Указать внутри файла `_.gitignore` имя файла, который не надо отслеживать.
Если в файле `_.gitignore`указать <*.pgn>, то все файлы с этим расширением будут игнорированы.


## 8. Создаение новой ветки в репозитории

Для создания новой ветки в репозитории следует использовать команду _"git branch имя ветки"_.
Для отслеживания с какой веткой работаем надо использовать команду _"git branch"_.

## 9. Переход между ветками/версиями (commit) файла

Для перехода между ветками следует использовать команду
```
git checkout имя ветки/имя (номер log) commit
```
Можно использовать комбинированные команды с помощью которых одновременно создается ветка и выполняется на нее переход:
```
git checkout -b <имя ветки> 
или
git switch -c <имя ветки>
```

## 10. Объединение веток

Для объединения веток использовать команду
```
git merge <имя присоединяемой ветки>
```
При этом важно находиться в основной ветке (в которую надо добавить изменения).

## 11. Удаление ненужной ветки

После объединения веток для удаления ненужной ветки, информация из которой уже перенесена в основную ветку, использовать команду 
```
git branch -d <имя файла>
```

## 12. Выделение текста.

### 12.1 Выделение текста курсивом и полужирным.
Для выделения текста курсивом следует выделяемый текст с двух сторон заключить в (*) (*пример*) или в (_) (_пример_).

Для выделения текста полужирным выделяемый текст с двух сторон заключить в (**) (**пример**) или в (__) (__пример__).
Если надо курсив сделать полужирным то используем знаки следующим образом:
__*пример*__
или **_пример_**.

### 12.2. Выделение текста в рамке
Для выделения текста в рамка выделяемый текст следует с двух сторон заключить в (```). Пример:
```
Выделяемый текст
```

### 12.3 Выделение текста цветом
Для выделения текста цветом необходимо нужный текст с двух сторон заключить в (`):

`например`.

## 13. Сравнение версий файла.

Для сравнения двух версий (сохраненной и текущей) следует использовать команду 
```
git diff
```

## 14. Создание заголовков и подзаголовков

Для создания основного заголовка следует использовать символ __#__ перед заголовком. Для создания подзаголовков следует перед подзаголовком использовать знак __##__.

# Пример
## Подпример
### Подподпример

## 15. Создание ненумерованных и нумерованных списков

Для создания ненумерованного списка перед каждым пунктом/элементом надо ставить знак (*) или (+):
* элемент 1
* элемент 2
* элемент 3
+ элемент 4
+ элемент 5

Для создания нумерованных списков перед каждым пунктом ставим номер:
1. элемент
2. элемент
3. элемент.

## 16. Удаление файла в репозитории
Для удаления файла из репозитория используется команда:
```
git rm <имя файла>
```

## 17. Помощь

Для получения справки в случае затруднения можно вызвать подсказку Git с помощью:
```
git --help
```

## 18. РАБОТА В УДАЛЕННОМ РЕПОЗИТОРИИ GITHUB.

Удаленные репозитории на GitHub используются для организации совместной работы нескольких исполнителей с одним репозиторием на портале GitHub. Для работы на портале GitHub (далее - GH) следует зарегистрироваться (создать аккаунт) следуя подсказкам портала.

### 18.1. Cоздание локального репозитория

Для работы необходимо инициализировать, при необходимости воспользовавшись подсказками GH, локальный репозиторий (см.раздел Инициализация репозитория).

### 18.2. Cоздание удаленного репозитория на GitHub.

Создание репозитория на GH (`https://github.com/`)осуществляется с помощью опции `New repository` на личной странице пользователя. При создании указывается название, присваивается признак (личный/публичный), также указывается ряд параметров, позволяющих в т.ч. создать файлы *Readme* (описание содержания репозитория), "*.ignore*".
Далее использовать команду `Creat repository`

### 18.3. Привязка удаленного и локального репозитория.

Используем подсказки GH и выполняем следующие действия.
* Переименовываем ветку Master в ветку Main с помощью команды:
```
git branch -M main
```
* Далее связываем репозитории с помощью команды (GH предлагает ее после создания удаленного репозитория)
```
git remote add origin <имя репозитория> <url-адрес репозитория>
```
При помощи команды `git remote` или `git remote -v`можно проверить, что локальный репозиторий привязан к удаленному.

### 18.4. Отправка изменений в удаленный репозиторий

Для отправки инфомрации из локального репозитория в удаленный репозиторий на GH используем команду: 
```
git push -u origin main
```

### 18.5. Клонирование удаленного репозитория

Для того, чтобы скопировать (склонировать) удаленный репозиторий GH на локальный компьютер для работы следует использовать команду 
```
git clone <имя репозитория> <url-адрес репозитория>
```
При последующей работе с "чужим" репозиторием следует создать новую свою ветку, в которую вносить дополнения/изменения.

### 18.6. Скачивание и одновременное слияние информации из удаленного репозитория с локальным репозиторием.

Для скачивания всей инфомрации из текущего удаленного репозитория GH в локальный следует использовать команду 
```
git pull
```
Внимание: эта команда одноверменно автоматически "сливает" информацию локального и удаленного репозитория (делает merge).

### 18.7. Работа с "чужим" удаленным репозиторием. PULL Request

При скачивании информации из чужого удаленного репозитория GH следует:
* сделать "fork" репозитория (кнопка `fork` в верхнем правом углу на странице GH)
* сформирован клон (своя версия) чужого репозитория в своем аккаунте на GH
* в своем локальном репозитории на создать клон своей версии репозитория (команда `git clone`)
* создать новую ветку в своей локальной версии репозитория и изменения вносить в эту созданную ветку
* зафиксировать изменения в своей локальной версии репозитория (`git commit`)
* отправить свою локальную версию репозитория в свой удаленный репозиторий на GitHub (`git push`)
* в своем удаленном репозитории в GH с помощью кнопки `pull reguest` отправить в чужой репозиторий. 
* при использовании команды GH будет проведена проверка на корректность слияния версий в своем репозитории в разных его ветках. После этого информацию можно отправить в чужой удаленный репозиторий на GH. В случае выявления конфликтов в информации конфликты должны быть устранены в своем удаленном репозитории.

Примечание: Pull Reqest возможнос использовать и в собственном удаленном репозитории на GH при работе с ветками. Процесс происходит также: проверка на отсутствие конфликтов и возможность слияния ифнормации, объединение веток (через `merge`) и последующее удаление присоединенной ветки.


__**УДАЧИ В РАБОТЕ!**__
