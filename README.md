# Password-Generator-python
random password generator with the help of python
#password Generated

import random


#for password required alphabet

lower_case = "a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u,v,w,x,y,z"
Upper_case= "A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,V,W,X,Y,Z"

#number and special character for strong password

number = "0,1,2,3,4,5,6,7,8,9"
special_character = "@#$%^&*?\/!Ï€"

#password

password = lower_case + Upper_case + number + special_character

try:
    while True:
        password_length = int(input("Enter password length: "))
       
       #if else use for print password
       
        if password_length < 2:
            print("Length should be more than 2 characters.")
        else:
            pass2 = "".join(random.sample(password, password_length))
            print("Your generated password:", pass2)
            
           #chose choice for more password
           
            exit_choice = input("Do you want to exit? (y/n): ").lower()
            if exit_choice == 'y':
                break  
except ValueError:
    print("Please enter an integer value.")
except:
    print("exception occured..")
