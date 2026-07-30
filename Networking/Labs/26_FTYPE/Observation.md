# Observations – FTYPE Command

## 1. Display All File Types (`ftype`)

- Displayed all registered file types available on the system.
- Showed the command associated with each file type.
- Included file types for applications such as Python, Chrome, Edge, Office, and VLC.
- Useful for auditing Windows file execution behavior.

---

## 2. Help Menu (`ftype /?`)

- Displayed the syntax and usage of the FTYPE command.
- Explained how to view or modify file type associations.
- Showed the correct command format.
- Useful for learning available options.

---

## 3. Executable File Type (`ftype exefile`)

- Returned the command associated with executable files.
- Output was `exefile="%1" %*`.
- Indicates executable files run directly by Windows.
- Confirms the default execution behavior for `.exe` files.

---

## 4. Text File Type (`ftype txtfilelegacy`)

- Returned "File type not found".
- No command was associated with `txtfilelegacy`.
- Indicates that the file type is not registered in FTYPE.
- Demonstrates that not every ASSOC entry has an FTYPE mapping.

---

## 5. HTML File Type (`ftype htmlfile`)

- Displayed the command associated with HTML files.
- HTML files were configured to open with Internet Explorer.
- Showed the complete executable path.
- Demonstrated how browsers can be associated with file types.

---

## 6. JPEG File Type (`ftype jpegfile`)

- Returned "File type not found".
- No execution command was registered.
- Indicates Windows may manage image associations differently.
- Not all file types appear in FTYPE.

---

## 7. Python File Type (`ftype Python.File`)

- Displayed the Python launcher command.
- Python files were associated with `py.exe`.
- Confirms that Python scripts execute through the Python Launcher.
- Useful for verifying scripting environments.

---

## 8. Batch File Type (`ftype batfile`)

- Displayed the command associated with batch files.
- Output was `batfile="%1" %*`.
- Confirms batch scripts execute directly through Command Prompt.
- Important for understanding Windows script execution.
```
