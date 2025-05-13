# 🧠 Linux Assistant (Statix)
[![Python 3.9+](https://img.shields.io/badge/python-3.9%2B-blue.svg)](https://www.python.org/)
[![Tkinter GUI](https://img.shields.io/badge/GUI-Tkinter-yellowgreen.svg)](https://wiki.python.org/moin/TkInter)
[![psutil](https://img.shields.io/badge/psutil-5.9.0-green.svg)](https://pypi.org/project/psutil/)
[![matplotlib](https://img.shields.io/badge/matplotlib-3.5.1-red.svg)](https://matplotlib.org/)
[![License: MIT](https://img.shields.io/badge/license-MIT-orange.svg)](LICENSE)

---

## 🚀 Project Overview
**Linux Assistant (Statix)** is an advanced desktop utility designed specifically for Linux users who demand powerful system monitoring and management in a sleek, intuitive interface. It seamlessly combines **real-time resource monitoring**, **integrated terminal functionality**, **file operations**, and **system management tools** into a single, customizable dashboard.

This comprehensive toolkit empowers you with:
- 🔍 Real-time CPU, RAM, and disk usage visualizations with historical trends
- 📊 Multi-layered interactive charts with precise metrics
- 🖥️ Embedded terminal with command execution and output capture
- 📁 Streamlined file and directory management operations
- 🎨 Five professionally designed themes for optimal visibility in any environment
- 📅 Integrated calendar system with event tracking capabilities
- 🌐 Network monitoring with bandwidth usage statistics
- 💾 User configuration persistence across sessions

---

## ✨ Key Features

### ⚙️ System Resource Monitoring
- **Dynamic Multi-Ring Donut Chart**
  - Concentric rings display CPU, RAM, and disk utilization
  - Color-coded segments with real-time percentage readouts
  - Smooth animations during state transitions
  
- **Dual Performance Line Charts**
  - Synchronized CPU and memory utilization trend lines
  - Configurable history length (30-120 seconds)
  - Interactive tooltips showing precise values at any point

### 🧾 Command Center
- **Integrated Terminal Environment**
  - Execute system commands directly from the interface
  - Full command history with searchable output
  - Syntax highlighting for common Linux commands
  - Command completion suggestions

### 🗂 File Management
- **Complete File Operations**
  - Create/delete files and directories with validation
  - Upload external files to working directory
  - Copy/move operations with progress tracking
  - Quick navigation to common system locations

### 🎨 UI Customization
- **Professional Theme System**
  - Choose from five meticulously crafted themes:
    - `Dark` - Elegant dark mode for reduced eye strain
    - `Light` - High-contrast clarity for daylight environments
    - `Hacker` - Classic terminal-inspired green-on-black aesthetic
    - `Glass` - Modern translucent blue tones for a fresh appearance
    - `Dracula` - Popular dark theme with vibrant accent colors
  - Theme settings persist between sessions

### 📅 Calendar & Scheduling
- **Interactive Calendar Widget**
  - Month view with current date highlighting
  - Event creation and management
  - Integration with system notifications
  
### 🔄 System Management
- **Advanced System Controls**
  - Safe system reboot with confirmation dialog
  - Service status monitoring and control
  - Resource usage alerts and notifications
  - Graceful application shutdown with state preservation

### 🌐 Network Monitoring
- **Real-time Network Diagnostics**
  - Current IP configuration display
  - Upload/download bandwidth graphs
  - Connected device discovery
  - Interface status monitoring

---

## 🛠 Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| Core Engine | `Python 3.9+` | Application framework and logic |
| User Interface | `Tkinter/ttk` | Cross-platform GUI components |
| Data Visualization | `Matplotlib` | Interactive charts and graphs |
| System Monitoring | `psutil` | Resource metrics collection |
| Mathematical Operations | `NumPy` | Data processing for visualizations |
| System Integration | `subprocess/os` | Command execution and file operations |
| Configuration | `json` | User preferences storage |
| Network Analysis | `socket/psutil` | Network metrics and diagnostics |

---

## ⚙ Installation

### Prerequisites
- Python 3.9 or higher
- Linux-based operating system
- Administrative privileges for system monitoring

### Setup Instructions

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/linux-assistant.git
cd linux-assistant
```

2. **Create Virtual Environment (Recommended)**
```bash
python3 -m venv venv
source venv/bin/activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Set Execution Permissions**
```bash
chmod +x linux_assistant.py
```

---

## 🧪 Usage Guide

### Starting the Application
```bash
./linux_assistant.py
```

### Command Line Options
```bash
./linux_assistant.py --theme=dark    # Start with specific theme
./linux_assistant.py --no-history    # Disable history tracking
./linux_assistant.py --debug         # Enable debug output
./linux_assistant.py --help          # Display usage information
```

### Keyboard Shortcuts
| Shortcut | Action |
|----------|--------|
| `Ctrl+T` | Switch theme |
| `Ctrl+R` | Refresh displays |
| `Ctrl+L` | Clear terminal |
| `F5` | Update system information |
| `F11` | Toggle fullscreen |
| `Esc` | Exit fullscreen/close dialogs |

---

## 📂 Working with Files

### Upload Files to Working Directory
Easily import files into your workspace:

1. Click the `Upload File` button in the Operations panel
2. Select any file from the file browser dialog
3. File will be copied to the current working directory

The application implements this functionality using:

```python
from tkinter import filedialog
import shutil

def upload_file():
    src = filedialog.askopenfilename(title="Select file to upload")
    if src:
        dest = os.path.join(os.getcwd(), os.path.basename(src))
        shutil.copy2(src, dest)  # copy2 preserves file metadata
        self.terminal_output(f"Uploaded: {os.path.basename(src)}")
```

### File Operations
- Create text files with optional templates
- Generate directories with proper permissions
- Delete files with secure confirmation dialogs
- Browse system directories with integrated file explorer

---

## 📸 UI Screenshots

> ![Dashboard View](screenshots/dashboard.png)
> Main dashboard with resource monitoring and terminal integration

> ![Theme Selection](screenshots/themes.png)
> Multiple professional themes for any working environment

> ![File Operations](screenshots/file_operations.png)
> Streamlined file management interface

> ![Calendar View](screenshots/calendar.png)
> Integrated calendar with event tracking

> ![Network Monitor](screenshots/network.png)
> Real-time network statistics visualization

---

## 📁 Project Structure

```
linux-assistant/
├── linux_assistant.py       # Main application file
├── README.md                # Project documentation
├── requirements.txt         # Dependencies list
├── resources/               # Application resources
│   ├── icons/               # UI icons
│   └── themes/              # Theme definitions
├── screenshots/             # UI screenshots
│   ├── dashboard.png
│   ├── themes.png
│   ├── file_operations.png
│   ├── calendar.png
│   └── network.png
├── docs/                    # Extended documentation
│   ├── user_guide.md
│   └── development.md
└── LICENSE                  # MIT License file
```

---

## 🛠 Configuration

The application stores user preferences in `~/.statix/config.json` with the following structure:

```json
{
  "theme": "Dark",
  "history_length": 60,
  "update_interval": 1000,
  "startup_commands": ["uptime", "free -m"],
  "default_directory": "~/Documents",
  "show_network_monitor": true
}
```

---

## 🔧 Development

### Building from Source
```bash
# Clone the repository
git clone https://github.com/yourusername/linux-assistant.git

# Install development dependencies
pip install -r requirements-dev.txt

# Run tests
pytest

# Build standalone package
pyinstaller --onefile linux_assistant.py
```

### Contributing
1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add new feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a Pull Request

---

## 📃 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements
- Inspired by classic Linux tools like `htop`, `glances`, and `bpytop`
- UI design influenced by modern dashboard frameworks
- Special thanks to contributors from the Linux sysadmin community
- Font icons provided by [Font Awesome](https://fontawesome.com/)

---

## 📬 Contact & Support
- Report issues on GitHub: [Issue Tracker](https://github.com/yourusername/linux-assistant/issues)
- Questions and discussion: [Discussions](https://github.com/yourusername/linux-assistant/discussions)
- Email: youremail@example.com

---
