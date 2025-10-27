# mkdocs-wiki

[Dockwatch wiki](https://dockwatch.wiki) source.

## Local Build

### macOS

```
brew install python3
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
mkdocs serve
```

### Windows

```
winget install Python.Python.3.14
python3 -m venv .venv
call venv\Scripts\activate
python3 -m pip install -r requirements.txt
mkdocs serve
```

### Linux

```
sudo apt install python3 || sudo yum install python3
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
mkdocs serve
```