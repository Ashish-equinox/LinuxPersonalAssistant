
# 🧠 Linux Assistant(Statix)

[![Python 3](https://img.shields.io/badge/python-3.x-blue.svg)](https://www.python.org/)  
[![Tkinter GUI](https://img.shields.io/badge/GUI-Tkinter-yellowgreen.svg)](https://wiki.python.org/moin/TkInter)  
[![License: MIT](https://img.shields.io/badge/license-MIT-orange.svg)](LICENSE)

---

## 🚀 Project Overview

**Linux Assistant** is an all-in-one intelligent desktop utility for Linux users.  
Packed in a bold and responsive UI, it blends **system monitoring**, **terminal integration**, **file operations**, and even a built-in **calendar** — all within one interactive dashboard.

This tool empowers you with:

- 🔍 Real-time resource insights (CPU, RAM, Disk)  
- 🧮 Dynamic chart visualizations  
- 🖥️ Terminal command output in-app  
- 📁 File and directory creation/deletion  
- 🧭 Multiple built-in themes for a sleek experience  
- 📅 Integrated calendar view

---

## ✨ Key Features

- ⚙️ **System Resource Monitoring**  
  - Live donut chart (CPU, RAM, Disk)  
  - Live line graph for CPU & memory history  

- 🧾 **Command Execution & Output**  
  - Run system info commands from the UI  
  - View results in a styled terminal window  

- 🗂 **File Management Panel**  
  - Create/delete files and directories  
  - Upload files to working directory  

- 🎨 **Dynamic Theme Selector**  
  - Choose from: `Dark`, `Light`, `Hacker`, `Glass`  

- 📅 **Built-in Calendar Viewer**  
  - Quick-access calendar popup  

- 🔄 **System Control**  
  - Safe reboot with confirmation  
  - Clean UI exit and graceful shutdown  

---

## 🛠 Tech Stack

| Component         | Purpose                                 |
|-------------------|------------------------------------------|
| `Python 3.9+`      | Core scripting language                 |
| `Tkinter`         | GUI framework                           |
| `Matplotlib`      | Charting (donut + line graphs)          |
| `psutil`          | Resource monitoring (CPU, RAM, Disk)    |
| `numpy`           | Smooth graph plotting                   |
| `subprocess/os`   | Terminal execution + file management    |

---

## ⚙ Installation

1. **Clone the Repository**

```bash
git clone https://github.com/<your-username>/linux-assistant.git
cd linux-assistant
````

2. **Create Virtual Environment**

```bash
python3 -m venv venv
source venv/bin/activate
```

3. **Install Dependencies**

```bash
pip install -r requirements.txt
```

---

## 🧪 Run the Assistant

```bash
python3 linux_assistant.py
```

> Ensure you grant execution permission if needed:

```bash
chmod +x linux_assistant.py
```

---

## 📂 Upload Files to Working Directory

You can upload files from another directory directly into Linux Assistant’s workspace via the `Upload File` button (GUI option).
Internally, it uses:

```python
from tkinter import filedialog
import shutil
src = filedialog.askopenfilename()
dest = os.path.join(os.getcwd(), os.path.basename(src))
shutil.copy(src, dest)
```

---

## 📸 UI Screenshots

> ![Chart View](screenshots/charts.png)
> Real-time donut & line chart visualizations

> ![Terminal Output](screenshots/terminal.png)
> Terminal-style output panel

> ![Calendar Theme](screenshots/calendar.png)
> Built-in themed calendar popup

---

## 📁 Project Structure

```
linux-assistant/
├── linux_assistant.py
├── README.md
├── requirements.txt
├── screenshots/
│   ├── charts.png
│   ├── terminal.png
│   └── calendar.png
└── LICENSE
```

---

## 📃 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

> Inspired by classic Linux terminal tools, enhanced with modern Pythonic GUI design.

---
