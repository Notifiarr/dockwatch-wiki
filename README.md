# dockwatch-wiki

[Dockwatch wiki](https://dockwatch.wiki) source.  
Based on [Notifiarr/mkdocs-wiki](https://github.com/Notifiarr/mkdocs-wiki).

## Local Build

### macOS

```
brew install python3
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
mkdocs serve --livereload
```

### Windows

```
winget install Python.Python.3.14
python3 -m venv .venv
call .venv\Scripts\activate
python3 -m pip install -r requirements.txt
mkdocs serve --livereload
```

### Linux

```
sudo apt install python3 || sudo yum install python3
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
mkdocs serve --livereload
```
