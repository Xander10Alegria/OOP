top.geometry("500x500")

answer = Text(width=35, height =2)
answer.place(x=100, y=100)

CreateQ = button(top, text="Create Queue", width=10, height=5, command=lambda: show("1"))
CreateQ.place(x=100, y=150)

enqueue = button(top, text="Enqueue", width=10, height=5, command=lambda: show("1"))
enqueue.place(x=100, y=150)

dequeue =button(top, text="dequeue", width=10, height=5, command=lambda: show("1"))
dequeue.place(x=100, y=150)

displayQueue =button(top, text="display queue", width=10, height=5, command=lambda: show("1"))
displayQueue.place(x=100, y=150)




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

class Stack:
    def __init__(self):
        self.element = []
    def push(self):
        self.element.append((stack.get(1.0, "end-1c")))
    def pop(self):
        self.element.pop()
    def displayStack(self):
        print("Element in stack:")
        for i in self.element:
            print(i)

s1 = Stack()
s2 = Stack()

s1.push()
s1.push
s1.pop()
s1.displaystack()
