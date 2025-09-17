# AI Desktop Assistant Project

A collection of intelligent desktop tools including:
- **Sophia AI Assistant**: Voice-activated personal assistant with a web interface.
- **AI Virtual Mouse**: Control your mouse using hand gestures.
- **Use Eye as Mouse**: Control your mouse using eye movements.

---

## Table of Contents

- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Module Usage](#module-usage)
  - [Sophia AI Assistant](#sophia-ai-assistant)
  - [AI Virtual Mouse](#ai-virtual-mouse)
  - [Use Eye as Mouse](#use-eye-as-mouse)
- [Troubleshooting](#troubleshooting)
- [Credits](#credits)

---

## Project Structure

```
AI_desktop_assistant/
│
├── Sophia-AI-Assistant/
│   ├── main.py
│   ├── requirements.txt
│   ├── README.md
│   ├── engine/
│   ├── www/
│   └── ...
│
├── AI_Virtual_mouse/
│   ├── AiVirtualMouse.py
│   ├── HandTrackingModule.py
│   ├── requirements.txt
│   └── README.md
│
└── Use_eye_as_mouse/
    ├── eye_controlled_mouse.py
    ├── requirements.txt
    └── README.md
```

---

## Setup Instructions

### 1. Clone the Repository

```sh
git clone <your-repo-url>
cd AI_desktop_assistant
```

### 2. Install Python

Ensure you have Python 3.10+ installed.  
[Download Python](https://www.python.org/downloads/)

### 3. Install Dependencies

Each module has its own dependencies.  
**Install them separately for each module:**

#### Sophia AI Assistant

```sh
cd Sophia-AI-Assistant
pip install -r requirements.txt
```

#### AI Virtual Mouse

```sh
cd ../AI_Virtual_mouse
pip install -r requirements.txt
```

#### Use Eye as Mouse

```sh
cd ../Use_eye_as_mouse
pip install -r requirements.txt
```

---

## Module Usage

### Sophia AI Assistant

**Start the assistant:**

```sh
cd Sophia-AI-Assistant
python main.py
```

**Features:**
- Voice commands
- Web-based interface
- Plays startup sound
- Opens Chrome in app mode

**Note:**  
If you see an error like `Windows cannot find 'google'`, update the code to use the correct Chrome executable path.  
Example fix in `main.py` or `engine/features.py`:
```python
import os
os.system('start chrome')
```
Or use the full path:
```python
os.system(r'"C:\Program Files\Google\Chrome\Application\chrome.exe" --app="file:///path/to/www/index.html"')
```

### AI Virtual Mouse

**Run the virtual mouse:**

```sh
cd AI_Virtual_mouse
python AiVirtualMouse.py
```

**Features:**
- Hand gesture recognition
- Mouse control via webcam

### Use Eye as Mouse

**Run the eye-controlled mouse:**

```sh
cd Use_eye_as_mouse
python eye_controlled_mouse.py
```

**Features:**
- Eye movement tracking
- Mouse control via webcam

---

## Troubleshooting

- **Chrome not opening:**  
  Make sure Chrome is installed and the path is correct in your code.

- **Webcam not detected:**  
  Ensure your webcam is connected and accessible.

- **Missing dependencies:**  
  Double-check `requirements.txt` for each module and install all packages.

- **Permission issues:**  
  Run your terminal/command prompt as administrator if needed.

---

## Credits

- For educational and research purposes

---

## License

MIT License (or specify your license here)