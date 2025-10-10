class Author:
    def __init__(self, name):
        self.name = name

    def display_author(self):
        print("Author:", self.name)

class Book:
    def __init__(self, book_id, title, author):
        self.book_id = book_id
        self.title = title
        self.author = author  # Author object

    def display_book(self):
        print(f"Book ID: {self.book_id}")
        print("Book Title:", self.title)
        self.author.display_author()

class LibraryUser:
    def __init__(self):
        self.user_id = ""
        self.name = ""
        self.borrowed_books = []

    def add_user(self):
        self.user_id = input("Enter your User ID: ")
        self.name = input("Enter your name: ")

    def borrow_book(self, book):
        self.borrowed_books.append(book)

    def display_user_info(self):
        print(f"\nUser ID: {self.user_id}")
        print(f"User Name: {self.name}")
        print("Borrowed Books:")
        for book in self.borrowed_books:
            book.display_book()

# Sample authors and books
author1 = Author("J.K. Rowling")
author2 = Author("E.B. White")
author3 = Author("Jane Austen")
author4 = Author("F. Scott Fitzgerald")
author5 = Author("Harper Lee")

book1 = Book("B001", "Harry Potter and the Sorcerer's Stone", author1)
book2 = Book("B002", "Charlotte's Web", author2)
book3 = Book("B003", "Pride and Prejudice", author3)
book4 = Book("B004", "The Great Gatsby", author4)
book5 = Book("B005", "To Kill a Mockingbird", author5)

# User interaction
user = LibraryUser()
user.add_user()

print("\nAvailable Books:")
print("1. Harry Potter and the Sorcerer's Stone")
print("2. Charlotte's Web")
print("3. Pride and Prejudice")
print("4. The Great Gatsby")
print("5. To Kill a Mockingbird")

while True:
    choice = input("Select a book to borrow by entering its number (or type 'done' to finish): ").strip()
    if choice.lower() == 'done':
        break
    elif choice == "1":
        user.borrow_book(book1)
        print(f"Added '{book1.title}' to your borrowed books.")
    elif choice == "2":
        user.borrow_book(book2)
        print(f"Added '{book2.title}' to your borrowed books.")
    elif choice == "3":
        user.borrow_book(book3)
        print(f"Added '{book3.title}' to your borrowed books.")
    elif choice == "4":
        user.borrow_book(book4)
        print(f"Added '{book4.title}' to your borrowed books.")
    elif choice == "5":
        user.borrow_book(book5)
        print(f"Added '{book5.title}' to your borrowed books.")
    else:
        print("Invalid choice. Please enter a number from 1 to 5 or 'done'.")

# Display borrowed books and user info
user.display_user_info()
