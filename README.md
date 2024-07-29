# Shut-Down-App-Using-python




# Computer Shut Down App

This is a simple Tkinter-based GUI application that allows users to restart, log out, or shut down their computer with the click of a button.

## Features

- **Restart:** Restarts the computer immediately.
- **Restart with Timer:** Restarts the computer with a delay (currently set to 1 second).
- **Log Out:** Logs out the current user.
- **Shut Down:** Shuts down the computer immediately.

## Prerequisites

- Python 3.x
- Tkinter (should be included with Python)

## Installation

1. Clone the repository or download the `shutdown_app.py` file.
2. Ensure you have Python installed on your system.

## Usage

1. Open a terminal (or Command Prompt on Windows).
2. Navigate to the directory where the `shutdown_app.py` file is located.
3. Run the script using Python:

    ```sh
    python shutdown_app.py
    ```

4. A window will open with buttons to restart, log out, or shut down your computer.

## Code Overview

```python
from tkinter import *
import os

def restart():
    os.system("shutdown /r /t 1")

def restart_time():
    os.system("shutdown /r /t 1")

def logout():
    os.system("shutdown /l")

def shutdown():
    os.system("shutdown /s /t 1")

st = Tk()
st.title("Computer Shut Down App")
st.geometry("500x500")
st.configure(bg="gray")

r_button = Button(st, text="Restart", font=("Time New Roman", "20", "bold"), relief=RAISED, cursor="plus", command=restart)
r_button.place(x=150, y=60, height=50, width=200)

rt_button = Button(st, text="Restart time", font=("Time New Roman", "20", "bold"), relief=RAISED, cursor="plus", command=restart_time)
rt_button.place(x=150, y=170, height=50, width=200)

lg_button = Button(st, text="Log Out", font=("Time New Roman", "20", "bold"), relief=RAISED, cursor="plus", command=logout)
lg_button.place(x=150, y=270, height=50, width=200)

sd_button = Button(st, text="Shut Down", font=("Time New Roman", "20", "bold"), relief=RAISED, cursor="plus", command=shutdown)
sd_button.place(x=150, y=370, height=50, width=200)

st.mainloop()
```

## Notes

- Be cautious when using this application, as it will execute system shutdown commands.
- Modify the time delay as needed in the `shutdown` commands.

