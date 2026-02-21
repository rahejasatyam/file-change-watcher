#  File Change Watcher

> A simple tool that keeps an eye on a file and tells you the moment something changes in it.

---

##  What Is This?

Imagine you have a text file on your computer, and someone (or some program) edits it while you're not looking. This tool acts like a **security camera for your file** — it watches it 24/7 and immediately tells you:

- ✅ Which line was changed
- ✅ Which lines were added
- ✅ If any lines were removed

You don't have to keep opening the file manually to check. Just run this tool once, and it will alert you automatically.

---

##  Who Is This For?

This tool is useful for:

- **Developers** who want to track changes in config or log files
- **Anyone** who needs to monitor a file for unexpected changes

---

##  What You Need Before Starting

You only need **one thing** installed on your computer:

###  Python 3

Python is a free programming language. Here's how to check if you already have it:

1. Open your **Terminal** (Mac/Linux) or **Command Prompt** (Windows)
2. Type this and press Enter:
   ```
   python --version
   ```
3. If you see something like `Python 3.x.x`, you're good to go! 
4. If not, download Python for free from [python.org](https://www.python.org/downloads/)

---

##  How to Set It Up (Step by Step)

### Step 1 — Download the project

Download the files from this page. You should have:
- `file_change_watcher.py` — the main script
- `README.md` — this guide

Put both files in the **same folder** on your computer.

---

### Step 2 — Create the file to watch

The tool watches a file called `file_changes.txt`. You need to create it yourself.

**Easy way:**
1. Open Notepad (Windows) or any text editor
2. Type anything (or leave it blank)
3. Save it as `file_changes.txt` **in the same folder** as the script

>  The name must be exactly `file_changes.txt` — spelling and capitalization matter!

---

### Step 3 — Open your Terminal or Command Prompt

- **Windows:** Press `Win + R`, type `cmd`, press Enter
- **Mac:** Press `Cmd + Space`, type `Terminal`, press Enter
- **Linux:** Press `Ctrl + Alt + T`

---

### Step 4 — Navigate to the folder

In your terminal, go to the folder where your files are saved. For example:

```bash
cd Desktop/file-change-watcher
```

>  `cd` means "change directory" — it's how you move between folders in the terminal.

---

### Step 5 — Run the script

Type the following and press Enter:

```bash
python file_change_watcher.py
```

You should see a message like:
```
Watching file_changes.txt for changes...
Main Thread is running....
Please enter value:
```

The tool is now **running and watching your file**! 🎉

---

##  How to Test It

1. While the script is running, open `file_changes.txt` in any text editor
2. Add a new line or change some text
3. Save the file
4. Look back at your terminal — it will print what changed!

**Example output:**
```
File changed!!!
Line 3 changed or added : Hello, this is a new line!
```

---

##  The Number Feature

While the watcher is running, you'll also notice it asks:
```
Please enter value:
```

This is a bonus feature — you can type any number and it will add 100 to it and print the result. For example, type `50` and it will print `150`.

---

##  How to Stop the Tool

To stop the script, go to your terminal and press:

```
Ctrl + C
```

This safely stops the program.

---

##  Common Problems & Fixes

| Problem | Fix |
|---|---|
| `python: command not found` | Try `python3` instead of `python` |
| `No such file or directory` | Make sure `file_changes.txt` is in the same folder as the script |
| Nothing happens when I edit the file | Make sure you **saved** the file after editing |
| `ValueError` when entering a value | Only enter whole numbers (like `5` or `200`), not text |

---

##  Project Files Overview

```
📂 your-folder/
 ├── file_change_watcher.py   ← The main Python script (don't edit this)
 ├── file_changes.txt         ← The file being watched (you create this)
 └── README.md                ← This guide
```

---

##  Built With

- **Python 3** — the programming language used
- **threading** — built-in Python tool that lets the watcher and the number feature run at the same time
- **os** — built-in Python tool used to detect file changes
- **time** — built-in Python tool used to check the file every 5 seconds
