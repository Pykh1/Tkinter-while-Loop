# Tkinter-while-Loop
random lines with diffrent width and diffrent colors

from random import*
from tkinter import*
def random_color_code():
    hex_chars=["0","1","2","3","4","5","6","7","8","9","a","b","c","d","e","f"]
    color_code="#"
    for i in range(0,6):
        color_code=color_code+choice(hex_chars)
    return color_code
my_window=Tk()
my_canvas=Canvas(my_window,width=400,height=400,background="white")
my_canvas.grid(row=0,column=0)
while True:
    x1=randint(0,400)
    y1=randint(0,400)
    x2=randint(0,400)
    y2=randint(0,400)
    my_canvas.create_line(x1,y1,x2,y2,fill=random_color_code(),width=10)
    my_canvas.update()
my_window.mainloop()
