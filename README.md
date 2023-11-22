# library-managemnet-system
PPS mini project by vennela reddy and khushi kumari
//For MySQL:
create database library_app;
use library_app

//create table books 
(bname varchar (50),
author varchar (50), 
bcode varchar (50), 
total int(50),
subject varchar(50));

//create table issue 
(name varchar(50),
regno varchar(50), 
bcode int(50), 
issue_date varchar(50));

//create table return
(name varchar (50),
regno varchar(50),
bcode int(50),
return_date varchar(50));

//For Python:
import mysql.connector as a
con=a.connect(host='localhost',user='root',passwd='9586',data
base='library_app')

def addbook():
bn=input("Enter Book Name: ") cantinEnter book ode
t=int(input("Total Books: "'))
s=input("Enter Subject: ") data=(bn,ba,c,t,s)
sql='insert into books values(%s,%s,%s,%s,%s);' c=con.cursor),
c.execute(sql,data)
con.commit().
print|"\n\n \n\nBook Added Successfully...
In\n|n\n")

wait = input|"\n\n \nPress enter to continue..
main()

def issueb():
n=input("Enter Student Name: ") r=int(input("Enter Reg No.: "))
co=int(input("Enter Book Code: "))
d=input("Enter Date: ")
a="insert into issue values(%,%s,%s, %s);" data=(n,r,co,d)
c=con.cursor()
c.execute(a,data)
con.commit().
print'"\n\n\n\nBook issued successfully to: ",n)

wait = input("\n\n\nPress enter to continue.... \n\n\n\n\n\n')
bookup(co,-1)
main()

def returnb():
n=input("Enter Student Name:")
r=int(input("Enter Reg no.:"))
co=int(input("Enter Book Code:"))
d=input("Enter  date:")
a="insert into return_values(%s,%s,%s,%s);"
data=(n,r,co,d)
c=con.cursor()
c.execute(a,data)
con.commit()
print("Book returned by:",n)

wait = input('\n\n\nPress enter to continue.......\n\n\n\n\n\n')
bookup(co,1)
main()

def bookup(co,u):
a="select total from books where bcode=%;"
data=(co,)
c=con.cursor()
c.execute(a,data)
myresult=c.fetchone()
t=my[0]result+u
sql= "update books set total-%s where bcode-%s;"
d=(t,co)
c.execute(sql,d)
con.commit()

wait = input/"In\n\nPress enter to continue.....\n\n\n\n\n\n')
main()

def dbook):
ac=int(input("Enter Book Code: "))
a="delete from books where bcode=%s;"
data=(ac,)
c=con.cursor()
c.execute(a,data)
con.commit)
print ("Book deleted successfully")

wait = inputl('\n\n\nPress enter to
continue.......\n\n\n\n\n\n\n\n\n\n\n)
main()

def dispbook():
a="select * from books;"
c=con.cursor()
c.execute(a)
myresult=c.fetchall()
for i in myresult:
print("Book name:",i[0])
print("Book Author:",i[1])
print("Book code:",i[2])
print("Total:",i[3]))
print("Subject:",|[4])
print('\n\n')

wait = input('\n\n\nPress enter to
continue…\n\n\n\n\n\n\n\n\n\n\n\n')
main()

def repot_issued_books():
a="select* from issue;"
c=con.cursor()
c.execute(a)
myresult=c.fetchall()
for i in myresult:
print(myresult)

wait = input('\n\n\nPress enter to
continue…\n\n\n\n\n\n\n\n')
main()

def report_return_books():
a="select * from return_;"
c=con.cursor()
c.execute (a)
myresult=c.fetchall()
for i in myresult:
print (myresult)

wait=input('\n\n\nPress enter to continue....\n\n\n\n\n\n\n\n')
main()

def main():
LIBRARY MANAGEMENT APPLICATION
1. ADD BOOK
2. ISSUE OF BOOK
3. RETURN OF BOOK
4. DELETE BOOK
5. DISPLAY BOOKS
6. REPORT MENU
7. EXIT PROGRAM
  choice=input("Enter Task No:.......")
print('\n\n\n\n\n\n\n')
if(choice=='1'):
addbook()
elif(choice=='2'):
issueb()
elif(choice=='3'):
returnb()
elif(choice=='4'):
dbook()
elif(choice=='5'):
dispbook()
elif(choice=='6'):
print("' R E P O R T M E N U
1. ISSUED BOOKS
2. RETURNED BOOKS
3. GO BACK TO MAIN MENU
   \n\n\n
   "')
   choice =input("Enter Task No:.....")
   print('\n\n\n\n\n\n\n')
   if choice=='1':
   report_issued_books()
   elif choice=='2':
   report_return_books()
   elif choice=='3':
   main()
   else:
   print("Please try again.......\n\n\n\n\n\n\n\n\n\n")
   main()
   elif(choice=='7'):
   print('\n\n\n\n\n\n\n\n\n\n\n\nThank you and have a great day ahead..............\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\")
   else:
   print("please try again.......\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n")
   main()
   main()

