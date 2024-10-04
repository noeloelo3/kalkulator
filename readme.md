```python
import tkinter as tk
root = tk.Tk()
root.geometry("300x300")
root.title("appppl")
label1 = tk.Label(root, text = "podaj liczbe")
label1.pack(anchor = "w")
entry = tk.Entry(root)
entry.pack(anchor = "center")

label2 = tk.Label(root, text = "podaj liczbe")
label2.pack(anchor = "w")
entry1 = tk.Entry(root)
entry1.pack(anchor = "center")


wynik = tk.Label(root, text = "wynik: ")



def frazy():
    wynik.config(text="wynik to: " + str(float(entry.get())*float(entry1.get())))

def fdziel():
    wynik.config(text="wynik to: " + str(float(entry.get())/float(entry1.get())))

def fplus():
    wynik.config(text="wynik to: " + str(float(entry.get())+float(entry1.get())))

def fminus():
    wynik.config(text="wynik to: " + str(float(entry.get())-float(entry1.get())))


razy = tk.Button(root, text = "x", command=frazy)
razy.pack(pady = "10")

dziel = tk.Button(root, text = "/", command=fdziel)
dziel.pack(pady = "10")

plus = tk.Button(root, text = "+", command=fplus)
plus.pack(pady = "10")

minus = tk.Button(root, text = "-", command=fminus)
minus.pack(pady = "10")



wynik.pack()
root.mainloop()
```
