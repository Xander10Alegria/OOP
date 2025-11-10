import tkinter as tk
from tkinter import*

top = Tk()
top.geometry("500x500")

answer = Text(width = 35, height =2)
answer.place(x=100, y=100)

def show(x):
    try:
        if x == "=":
            final_answer = eval(answer.get(1.0, "end-1c"))
            answer.insert(tk.INSERT, x)
            answer.insert(tk.INSERT, final_answer)
        else:
            answer.insert(tk.INSERT, final_answer)
                if x == "C":
                    answer.delete(1.0, END)
except:
    answer.delete(1.0, END)

B1 = Bott

class Queue:
    def __init__(self):
        self.element = []
    def enqueue(self):
        self.element.append(input("enter"))

    def dequeue(self):
        self.element.remove(0)

    def display_Queue(self):
        print("Elements in Queue:")
        for i in self.element:
            print(i)

#main code
q1 = Queue()
q2 = Queue()
