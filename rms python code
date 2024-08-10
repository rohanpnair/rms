import mysql.connector as my
try:
     con=my.connect(host='localhost',user='root',password='ncs',database='RMS',charset='utf8')
     cur=con.cursor()
     qry='''create table if not exists Menu (Food_code integer primary key, Name varchar(30), Availability varchar(20), Type varchar(10), cost integer , offer_available varchar(40))'''
     cur.execute(qry)
     print("Menu table created successfully..")
     print("The table structure is :")
     print()
     cur.execute("desc Menu")
     print('-'*60)
     print("FIELD NAME \t \tDATA TYPE")
     print('-'*60)
     for c in cur:
         print(c[0].upper(), '\t\t', c[1])
    
     cur.close()
     con.close()
except Exception as e:
     print('Error message - ',e)

def INSERT():
    try:
        con=my.connect(host='localhost',user='root',password='ncs',database='RMS',charset='utf8')
        cur=con.cursor()
        while True :
            a=int(input("Enter the food code::"))
            b=input("Name of food:")
            c=input("Availabilty:")
            d=input("Type of food::")
            e=int(input("Cost:"))
            f=input("offers available :")
            qry="insert into Menu values({},'{}','{}','{}',{},'{}')".format(a,b,c,d,e,f)
            cur.execute(qry)
            con.commit()
            print("One record added to database")
            print()
            ans=input("Do you want to add another record(y/n):")
            if ans =='n':
                break
                cur.close()
                con.close()
    except Exception as e:
             print('Error message - ',e)

def SEARCH():
    try:
        con=my.connect(host='localhost',user='root',password='ncs',database='RMS',charset='utf8')
        cur=con.cursor()
        while True:
            item=input("Enter the item to search for:")
            qry="select * from menu where Name='{}'".format(item)
            #print(qry)
            cur.execute(qry)
            cols=cur.column_names
            rec=cur.fetchone()
            if rec==None:
                print("Sorry! Record for ",item,"not found")
            else:
                print("-"*20)
                for i in range(len(rec)):
                    print(cols[i].upper(),'\t:',rec[i])
                print("-"*20)
            print()
            ans=input("Do you want to continue(y/n):")
            if ans =='n':
                break
                cur.close()
                con.close()
    except Exception as e:
        print(e)

def MODIFY():
    try:
        con=my.connect(host='localhost',user='root',password='ncs',database='RMS',charset='utf8')
        cur=con.cursor()
        while True:
            Food_code=input("Enter the food code to update:")
            qry="select * from menu where Food_code={}".format(Food_code)
            cur.execute(qry)
            rows=cur.fetchall()
            if rows==[]:
                print("Sorry! Record for",Food_code, "not found")
            else:
                cost=int(input("Enter the new cost for the item:"))
                qry="update menu set cost= {} where Food_code={}".format(cost,Food_code)
                print(qry)
                cur.execute(qry)
                con.commit()
                print("Cost for food code",Food_code, "has been updated")
            ans=input("Do you want to update another record(y/n):")
            if ans =='n':
                break
        cur.close()
        con.close()
    except Exception as e:
        print(e)








def DELETE():
    try:
        con=my.connect(host='localhost',user='root',password='ncs',database='RMS',charset='utf8')
        cur=con.cursor()
        while True:
            Bid=int(input("Enter the  id to delete:"))
            qry="select * from menu where food_code={}".format(Bid)
            cur.execute(qry)
            rows=cur.fetchall()
            if rows==[]:
                print("Sorry!Record for food code",Bid,"not found")
            else:
                ans=input("Are you sure you want to delete this record(y/n)?")
                if ans=='y':
                    qry="delete from menu where food_code={}".format(Bid)
                    cur.execute(qry)
                    con.commit()
                    print("Record for food code",Bid, "has been deleted")
            print()
            ch=input("Do you want to delete another record(y/n):")
            if ch=='n':
                break
        cur.close()
        con.close()
    except Exception as e:
        print(e)

def SHOWTABLE():
     try:
          con=my.connect(host='localhost',user='root',password='ncs',database='RMS',charset='utf8')
          cur=con.cursor()
          qry='''select * from menu'''
          cur.execute(qry)
          rows=cur.fetchall()
          for i in rows:
               print(i)
          cur.close()
          con.close()
     except Exception as e:
          print('Error message - ',e)

while True:
     print('------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------')
     print('Welcome to the RMS or Restaurant management system \n')
     print('Please select you choice from the options: \n')
     print('1. Input food items \n 2.modify food item\'s  cost \n 3.search food items \n 4. Delete an item \n 5. Display table \n6. Exit  ')
     print('------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------')
     ch = int(input('Select your choice(1/2/3/4/5/6):'))
     if ch==1:
          INSERT()
     elif ch==2:
          MODIFY()
     elif ch==3:
          SEARCH()
     elif ch==4:
          DELETE()
     elif ch==5:
          SHOWTABLE()
     elif ch==6:
          break




