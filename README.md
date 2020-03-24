# Py-Todo

## Overview
A CLI tool for keeping track of things! Written entirely in Python.

Serialized todo list objects are saved in ~/.local/share/py-todo/todo.dat by default. Serialization done by pickling.

## Installation
```bash
$ git clone https://github.com/jrao1724/py-todo.git
$ cd py-todo 
$ chmod +x todo && sudo cp todo /usr/bin/todo
```

## Usage
```bash
$ todo                                   # List all items.
$ todo -a                                # Add an item. (without Title / Expiry Date prompt)
$ todo -a <title> <expiry_date>          # Add an item. (with Title / Expiry Date prompt)
$ todo -e <index>                        # Edit an item. (without Title / Expiry Date prompt)
$ todo -e <index> <title> <expiry_date>  # Edit an item. (with Title / Expiry Date prompt)
$ todo -l --list                         # List all items.
$ todo -m --move <index> <new index>     # Move an item from one index to a new index.
$ todo -r <indices>                      # Remove one or more items.
$ todo -s --sort                         # Sort items by their remaining days.
$ todo -h                                # Display help message.
$ todo -v                                # Display version info.
$ todo -org <filename>                   # Adds TODOs from ORG files.
```

## Optional Configs
```bash
[PY-TODO]
color = true || false
detail_mode = true || false
week_start_day = <day of the week of your choosing>
```
Detail mode is for displaying the detailed time remaining:
```bash
Calculus Exam (Next Monday; 5 days left)     # detail_mode = true
Calculus Exam (5 days left)                  # detail_mode = false
```
