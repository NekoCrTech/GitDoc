---
icon: square-terminal
---

# Terminal Crash Curse



```bash
ls
```

* Lists the names of files and directories in the current directory.
* Hidden files (those starting with `.`) are not displayed by default.

{% code fullWidth="false" %}
```bash
ls Folder
```
{% endcode %}

(Folder = name of a folder in this directory)

* Lists the names of files and directories in the Folder

```
start .
```

* is used in the **Windows Command Prompt (cmd)** to open the current directory in **File Explorer**.

```bash
pwd
```

* Print Working Directory (pwd) prints out current directory

```bash
cd Folder
```

* Change Directory (cd) enters the folder

```bash
cd ..
```

* Gets out of the directory to the parent folder

```bash
touch file.txt
```

* Creates an empty file named file.txt if it doesn’t already exist.
* A single touch can create multiple files of different types in a single line.  (touch file.txt red.pdf)
* It can also create files inside folders if given the directory. (touch Folder/rocky.png)

```bash
mkdir Plants
```

* Creates a folder named Plants in the directory
* It can create multiple folders as touch

```bash
rm file.txt
```

* Deletes file.txt.

```bash
rm -rf Plants
```

* Deletes folder
