#import mysql connector module
import mysql.connector

#make connection with local mysql server and storing in variable
mydb = mysql.connector.connect(host = 'localhost', user = 'myuser', password = 'myuser', database = 'librarydb')
#create cursor to go to next 
mycursor = mydb.cursor()
#creating of function to insert into database
def insertBook():
    bookID = int(input("Please enter the book ID: "))#input from user
    bookTITLE = input("Pleaes enter the book TITLE: ")#input from user
    bookAUTHOR = input("Pleae enter the book AUTHOR: ")#input from user
    bookQTY = int(input("Pleae enter the book STOCK: "))#input from user
    #creating of mysql query and storing it into a variable
    sqlINSERT = 'INSERT INTO books(id, title, author, qty) VALUES (%s,%s,%s,%s)'
    #storing input from user into tuple
    bookINSERT =(bookID, bookTITLE, bookAUTHOR, bookQTY)
    #execute of mysql query and printing it out
    print(mycursor.execute(sqlINSERT, bookINSERT))
    #updating the database 
    mydb.commit()
#creating of function to update database with different options
def updateBook():
    print("PLEASE PICK OPTION:\n"#output for user
          "1.Update book ID\n"
          "2.Update book TITLE\n"
          "3.Update book AUTHOR\n"
          "4.Update book QTY\n")
    updateOPTION = int(input("Please enter your option: "))#input for user

    if updateOPTION == 1:#if statement to update id of book
        bookID = int(input("Please give ID of book you want to change: "))#input from user
        newBookID = int(input("Please enter new ID of book: "))#input from user
        #creating of mysql query and storing it in variable
        sqlUPDATE = 'UPDATE books SET id =' + str(newBookID) + ' WHERE id =' + str(bookID)
        #execute of mysql query and printing it out
        print(mycursor.execute(sqlUPDATE))
        #updating the database
        mydb.commit()
    elif updateOPTION == 2:#else if statement to update title of book
        bookID = int(input("Please give ID of book you want to change: "))#input from user
        newBookTITLE = input("Please enter new TITLE of book: ")#input from user
        #creating of mysql query and storing it in variable
        sqlUPDATE = 'UPDATE books SET title =' + '"' + newBookTITLE + '"' + ' WHERE id =' + str(bookID)
        #execute of mysql query and printing it out
        print(mycursor.execute(sqlUPDATE))
        #updating the database
        mydb.commit()
    elif updateOPTION == 3:#else if statement to update author of book
        bookID = int(input("Please give ID of book you want to change: "))#input from user
        newBookAUTHOR = input("Please enter new AUTHOR of book: ")#input from user
        #creating of mysql query and storing it in variable
        sqlUPDATE = 'UPDATE books SET author =' + '"' + newBookAUTHOR + '"' + ' WHERE id =' + str(bookID)
        #execute of mysql query and printing it out
        print(mycursor.execute(sqlUPDATE))
        #updating the database
        mydb.commit()
    elif updateOPTION == 4:#else if statement to update the stock qty
        bookID = int(input("Please give ID of book you want to change: "))#input from user
        newBookQTY = int(input("Please enter new stock QTY of book: "))#input from user
        #creating of mysql query and storing it in variable
        sqlUPDATE = 'UPDATE books SET qty =' + str(newBookQTY) + ' WHERE id =' + str(bookID)
        #execute of mysql query and printing it out
        print(mycursor.execute(sqlUPDATE))
        #updating the database
        mydb.commit()
    else:#else statement if wrong option is picked
        print("Wrong option")#output for user
#function to delete a row out of database        
def deleteBook():
    bookID = int(input("Please enter book ID you which to delete: "))#input from user
    #creating of mysql query and storing it in variable
    sqlDELETE = 'DELETE FROM books WHERE id =' + str(bookID)
    #execute of mysql query and printing it out
    print(mycursor.execute(sqlDELETE))
    #updating the database
    mydb.commit()
#function to show all entries in the database
def showLibrary():
    mycursor.execute("SELECT * FROM books")
    myresult = mycursor.fetchall()
    for row in myresult:
         print(myresult)
            
option = ""#creating of option variable to store option in

while option !=0:#while loop to stay in program until you want to exit
    print("PLEASE PICK OPTION:\n"#output for user
      "1.Enter Book\n"
      "2.Update Book\n"
      "3.Delete Book\n"
      "4.Show Book\n"
      "0.Exit")
    option = int(input("Enter Option: "))#input from user
    if option == 1:#if statement if option is equel to one to start insert function
        insertBook()#calling of function
    elif option == 2:#else if statement if option is equel to one to start update function
        updateBook()#calling of function
    elif option == 3:#else if statement if option is equel to one to start delete function
        deleteBook()#calling of function
    elif option == 4:#else if statement if option is equel to one to start select function
        showLibrary()#calling of function
    elif option == 0:#else if statement to exit program
        print("You have exit the program")
    else:#else statement for wrong option
        print("Wrong option please pick again")
