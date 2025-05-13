# 🧠 Statix – Final UI with System Stats, Commands, and Calendar

Linux Assistant is a Python-based graphical assistant for Linux users, offering an elegant, real-time overview of system performance, interactive command execution, file operations, and a built-in calendar — all in one smart, bold UI.

---

## 🔧 Features

- 📊 **Live Resource Monitoring**: 
  - Multi-ring donut chart showing CPU, RAM, and Disk usage
  - Live updating CPU & RAM line charts
- 🖥️ **Terminal Output Pane**: 
  - Execute system commands (CPU, RAM, Disk, Network)
  - See real-time results in a built-in terminal
- 🧾 **File & Directory Management**:
  - Create/Delete files and directories from GUI
- 🎨 **Theme Selector**:
  - Choose from: Dark, Light, Hacker, Glass
- 📆 **Calendar Viewer**:
  - Displays a monthly calendar popup
- 🧵 **Threaded Command Execution**:
  - UI stays responsive while running commands
- 🔁 **Reboot Option**:
  - Safely reboot system with confirmation

---

## 📂 Upload Files to Assistant Directory

Want to upload a file from another directory into the Linux Assistant working directory? Use this additional method:

```python
def _upload_file(self):
    from tkinter import filedialog
    src = filedialog.askopenfilename()
    if src:
        import shutil
        dest = os.path.join(os.getcwd(), os.path.basename(src))
        try:
            shutil.copy(src, dest)
            messagebox.showinfo("Upload", f"File uploaded to {dest}")
        except Exception as e:
            messagebox.showerror("Error", f"Failed to upload: {e}")
