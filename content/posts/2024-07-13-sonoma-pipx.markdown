---
title: "MacOS и установка Python пакетов"
date: 2024-07-13T12:49:04+0300
image: https://static.juev.org/2024/07/pipx.png
tags: 
  - macos
  - python
---

Про настройку питона для корректной работы с сетью я описывал в
[Python SSL error](https://www.juev.org/2024/06/17/python-certifi/).
Теперь же расскажу про то, как можно довольно просто устанавливать python-пакеты в систему.

Достоточно установить с помощью homebrew [pipx](https://pipx.pypa.io):

```bash
brew install pipx
```

И затем добавить директорию `~/.local/bin` в PATH.

Далее устанавливаем нужную программу в систему:

```bash
$ pipx install pycowsay
  installed package pycowsay 0.0.0.2, installed using Python 3.12.4
  These apps are now globally available
    - pycowsay
  These manual pages are now globally available
    - man6/pycowsay.6
done! ✨ 🌟 ✨

$ pycowsay hello world

  ----------
< hello world >
  ----------
   \   ^__^
    \  (oo)\_______
       (__)\       )\/\
           ||----w |
           ||     ||
```

Для каждого пакета подготавливается отдельное окружение, и эти окружения не пересекаются друг с другом.
Все просто и удобно.
