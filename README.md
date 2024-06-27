# text_to_speak
import tkinter as tk
from tkinter import StringVar, LabelFrame, Label, Entry, Button
import pyttsx3

# Initialize the text-to-speech engine
engine = pyttsx3.init()

def speaknow():
    """Function to convert text to speech"""
    engine.say(textv.get())
    engine.runAndWait()
    engine.stop()

# Create the main window
root = tk.Tk()

# StringVar to hold the text input
textv = StringVar()

# Create a labeled frame
obj = LabelFrame(root, text="Text to speech", font=("Arial", 20), bd=1)
obj.pack(fill="both", expand="yes", padx=10, pady=10)

# Label for text entry
lbl = Label(obj, text="Text", font=("Arial", 14))
lbl.grid(row=0, column=0, padx=5, pady=10)

# Entry widget for text input
text = Entry(obj, textvariable=textv, font=("Arial", 14), width=25, bd=5)
text.grid(row=0, column=1, padx=10, pady=10)

# Button to trigger speech
btn = Button(obj, text="Speak", font=("Arial", 14), bg="black", fg="white", command=speaknow)
btn.grid(row=0, column=2, padx=10, pady=10)

# Configure the main window
root.title("Text to Speech")
root.geometry("400x200")
root.resizable(False, False)

# Run the main loop
root.mainloop()


