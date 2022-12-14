<h1>pip command</h1>
<h2>Библиотека для выполнения команд pip</h2>

***
<h2>Установка</h2>

    pip install pip_command
***


<h2>install | installs | install_requirements</h2>

<code>install</code> - установка библиотеки<br>
Параметр <code>version</code> отвечает за версию библиотеки, изначально None - последняя версия

<code>installs</code> - установка нескольких библиотек

<code>install_requirements</code> - установка requirements.txt


```python
from pip_command import install, installs, install_requirements

install("requests")  # установка библиотеки requests
install("requests", version="2.25.1")  # установка библиотеки requests версии 2.25.1
installs("requests", "bs4")  # установка библиотек requests и bs4
install_requirements("requirements.txt")  # установка библиотек из файла requirements.txt
```

<h2>update | update | update_requirements</h2>

<code>update</code> - обновление библиотеки 

<code>updates</code> - обновление нескольких библиотек

<code>update_requirements</code> - обновление библиотек по файлу requirements.txt

```python
from pip_command import update

update("requests")  # обновляет requests до последней версии
update("requests", "bs4")  # обновляет requests и bs4 до последней версии
```

<h2>uninstall | uninstalls | uninstall_requirements</h2>

<code>uninstall</code> - удаление библиотеки

<code>uninstalls</code> - удаление нескольких библиотек

<code>uninstall_requirements</code> - удаление библиотек по requirements.txt


```python
from pip_command import uninstall, uninstalls, uninstall_requirements

uninstall("requests")  # удаление библиотеки requests
uninstalls("requests", "bs4")  # удаление библиотек requests и bs4
uninstall_requirements("requirements.txt")  # удаление библиотек из файла requirements.txt
```

<h2>freeze</h2>

<code>freeze</code> - создание файла формата requirements.txt
  
Параметр <code>requirements_file</code> отвечает за название создаваемого файла, изначально:  requirements.txt

```python
from pip_command import freeze

freeze()  # создание файла requirements.txt
freeze("file_name.txt")  # создание файла формата requirements.txt с названием file_name.txt
```


<h2>plist</h2>

<code>plist</code> - возвращает список всех установленных библиотек

```python
from pip_command import plist

print(plist())  # >> ["requests", "bs4]
```


<h2>inspect</h2>

<code>inspect</code> - возвращает инспекцию среды python

```python
from pip_command import inspect

print(inspect())  # >> 
```

