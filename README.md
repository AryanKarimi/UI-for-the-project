# UI-for-the-project
The codes for our program UI
import tkinter as tk
from tkinter import filedialog, messagebox, ttk

root = tk.Tk()
root.title("Windows Scheduler")
root.geometry("420x220")

lbl_instructions = tk.Label(root, text="Select a text file with datetime (YYYY-MM-DD HH:MM):")
lbl_instructions.pack(pady=10)

btn_select = tk.Button(root, text="Select File", command=read_datetime_from_file)
btn_select.pack(pady=5)

# Action dropdown
lbl_action = tk.Label(root, text="Choose Action:")
lbl_action.pack(pady=5)

action_var = tk.StringVar(value="Hibernate")
action_menu = ttk.Combobox(root, textvariable=action_var, values=["Hibernate", "Shutdown", "Sleep"], state="readonly")
action_menu.pack(pady=5)

lbl_status = tk.Label(root, text="No schedule set yet.")
lbl_status.pack(pady=20)

root.mainloop()

<img width="423" height="248" alt="Capture333" src="https://github.com/user-attachments/assets/c30eaa25-2d88-4f91-93fd-38daab1a7256" />
