# Julia_tutorial_rus
Введение в язык программирования Julia на русском

Julia: руководство для начинающих

**Julia** - высокоуровневый, высокопроизводительный язык программирования с динамической типизацией для математических вычислений. Синтаксис похож на матлабово семейство, язык написан на Си, С++ и Scheme, есть возможность вызова Сишных библиотек. 

Это весьма новый язык, и у российской аудитории пока не очень популярный. Одной из возможных причин является скудность руководств на русском языке, что мы и попытаемя исправить.

Обучалка выполнена на Jupyter, так что питонисты будут чувствовать себя как рыба в воде, ну, или питон в своих джунглях. С другой стороны, всё так просто и интерактивно, что даже у людей плохо знакомых с программированием данный материал не должен вызвать трудностей. Приступим к самой трудной части:

### Установка

Julia была разработана в знаменитом MIT. Первый релиз увидел свет в 2012 году. На момент написания этих строк текущей версией является v1.1.0 Загрузить дистрибутив, найти документацию или посмотреть видеоуроки можно на официальном сайте http://julialang.org/. 

Пользователи *Windows 7/Windows Server 2012* также должны установить: 
+ [TLS easy_fix](https://support.microsoft.com/en-us/help/3140245/update-to-enable-tls-1-1-and-tls-1-2-as-a-default-secure-protocols-in "мне помог Method 2: Microsoft Update Catalog") Чтоб узнать детали смотрите [Discourse thread](https://discourse.julialang.org/t/errors-for-git-pkg/9351 "тут всё на нерусском").
+ [Windows Management Framework 3.0 or later](https://docs.microsoft.com/en-us/powershell/wmf/overview).

Скачав фиксер, лучше обеспечьте ограничение на выход в интернет, а уж потом обновляйте, не то все узнают какая у вас недействительная копия Windows. Это обновление нужно, чтоб предотвратить проблемы с системой контроля версий *git*, иначе не будет возможности докачивать дополнительные пакеты, а без них будет тяжко.

После установки можно сразу приступать к работе: Вам будет доступен интерпретатор (REPL) в котором всё будет происходить в консольном режиме. 

Но нам нужен Jupyter
* [Подробно об установке](https://devpractice.ru/python-lesson-1-install/)
* [Работа с Jupyter Notebook](https://devpractice.ru/python-lesson-6-work-in-jupyter-notebook/)
* [Как настроить Jupyter Notebook для Python 3](https://tproger.ru/translations/jupyter-notebook-python-3/)
### 1
Использовать [IJulia](https://github.com/JuliaLang/IJulia.jl). Для этого запустите *julia* и в открывшейся консоли наберите команды
```
using Pkg
Pkg.add("IJulia")
```
или
```
]add IJulia
```
затем
```
]build IJulia
```
### Возможные проблемы
- Не удается установить соединение - проверьте свои права доступа (нет ли у вас ограничений на запись в папки на C:\, зайдите как админ или запустите Джулию в режиме администратора), если используете прокси, [убедитесь](http://savvateev.org/blog/44/), что оно настроено не только для браузера
- Нехватает какого-нибудь пакета - читайте сообщение об ошибке, там укажется, потом качайте. Например
```
]add PyCall
```
### 2
Вы можете установить Jupyter в комплекте [Anaconda](https://www.anaconda.com/distribution/). После установки Вам будет доступен только питон. Затем выполняйте пункт **1**, просто теперь *IJulia* не будет устанавливать Вам миниконду, а подружится с уже существующей.
### 3
На сайте https://juliacomputing.com доступны продукты, основой для которых послужил этот язык. **JuliaPRO** последней версии предоставляет **Juno** - красивую IDE с окошком для графиков и рабочим пространством, где можно смотреть содержимое всех объектов.
Но также можно скачать старую версию 0.6.4, там присутствует Jupyter, с которым вы можете поженить свою Юльку выполнив пункт **1**

Всё, теперь запускайте Jupyter либо используя ярлык в Пуск либо вбив в консоль Джулии
```
using IJulia
notebook()
```
Скачав файлы туториала, открывайте их с помощью своего Юпитера (по умолчанию в папке Downloads) и всё, можете начинать изучение!
