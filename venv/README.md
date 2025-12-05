# Python Virtual Environment Cheat Sheet

This guide covers how to **create**, **activate**, **verify**, and **deactivate** virtual environments in Python on **Windows** and **Linux/macOS**.

---

## ✅ 1. Create a Virtual Environment

```bash
# Inside your project directory
python -m venv venv
```
- This creates a folder named `venv` containing the isolated Python environment.

---

## ✅ 2. Activate the Virtual Environment

### **Linux/macOS**:
```bash
source venv/bin/activate
```

### **Windows (CMD)**:
```cmd
venv\Scriptsctivate.bat
```

### **Windows (PowerShell)**:
```powershell
venv\Scripts\Activate.ps1
```

After activation, your terminal prompt will show:
```
(venv) user@machine:~/project$
```

---

## ✅ 3. Verify Activation

### **Check Python Path**:
```bash
which python      # Linux/macOS
where python      # Windows
```
Should point to:
```
/path/to/project/venv/bin/python   # Linux/macOS
C:\path	o\projectenv\Scripts\python.exe   # Windows
```

### **Check Environment Variable**:
```bash
echo $VIRTUAL_ENV        # Linux/macOS
echo %VIRTUAL_ENV%       # Windows CMD
$env:VIRTUAL_ENV         # Windows PowerShell
```
If it prints the venv path, you’re inside the virtual environment.

### **Check Installed Packages**:
```bash
pip list
```
Should show only packages installed in the virtual environment.

---

## ✅ 4. Deactivate the Virtual Environment

```bash
deactivate
```
This returns you to the system Python environment.

---

## ✅ Notes
- Closing the terminal automatically deactivates the virtual environment.
- You **create once**, but **activate every time** you open a new terminal.
- For auto-activation in VS Code, set the Python interpreter to your venv in **Command Palette → Python: Select Interpreter**.

---

Happy coding! 🎯
