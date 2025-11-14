import tkinter as tk
from tkinter import *

top = Tk()
top.geometry("700x700")

# answer = Text(width=35, height =2)
# answer.place(x=100, y=100)

# def show(x): ###myfunction to display and calculate the answer####
#         try:
#             if x == "=":
#                 final_answer = eval(answer.get(1.0, "end-1c"))
#                 answer.insert(tk.INSERT, x)
#                 answer.insert(tk.INSERT, final_answer)
#             else:
#                 answer.insert(tk.INSERT, x)
#                 if x == "C":
#                     answer.delete(1.0, END)
#         except:
#             answer.delete(1.0, END)



class Queue:
    def __init__(self):
        self.element = []
    def enqueue(self):
        self.element.append(q_TextBox.get(1.0, END))
        self.display_Queue()

    def dequeue(self):
        self.element.pop(0)

    def display_Queue(self):
        print("Elements in Queue:")
        for i in self.element:
            q_answer.insert(tk.INSERT, i+";")

q_TextBox = Text(width=35, height=2)
q_TextBox.place(x=100, y=100)

q_answer = Text(width=35, height=2)
q_answer.place(x=100, y=400)

q1 = Queue()
q2 = Queue()

CreateQ = Button(top, text="Create Queue", width=10, height=5)
CreateQ.place(x=100, y=150)

enqueue = Button(top, text="Enqueue", width=10, height=5, command=lambda:q1.enqueue())
enqueue.place(x=100, y=250)

dequeue =Button(top, text="dequeue", width=10, height=5, command=lambda:q1.dequeue())
dequeue.place(x=100, y=350)

displayQueue =Button(top, text="display queue", width=10, height=5, command=lambda:q1.display_Queue())
displayQueue.place(x=100, y=450)





#main code

stack_TxtBox = Text(width=35, height =2)
stack_TxtBox.place(x=100, y=300)

stack_answer = Text(width=35, height =2)
stack_answer.place(x=100, y=300)

class Stack:
    def __init__(self):
        self.element = []

    def push(self):
        self.element.append((stack_TxtBox.get(1.0, "end-1c")))

    def pop(self):
        self.element.pop()

    def displayStack(self):
        print("Element in stack:")
        for i in self.element:
            stack_answer.insert(tk.INSERT, i+";")

    answer = Text(width=35, height=2)
    answer.place(x=100, y=100)


s1 = Stack()
s2 = Stack()

s1.push()
s1.push()
s1.pop()
s1.displayStack()

top.mainloop()
