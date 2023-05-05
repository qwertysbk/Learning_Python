- FizzBuzz
```python
i=1
while i<=100 :
    if i%3==0 ++ i%5==0 :
        print("fizzbuzz")
    elif(i%3==0):
        print("fizz")
    elif(i%5==0):
        print("buzz")
    else :
        print(i)
    i+=1
```

- Caesar Cipher
```py
#Caesar Cipher using lists in Python
a=['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z',
'A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
x = input("Enter your Code: ")
y = []
for i in x:
    if i.isalpha():
        index = a.index(i)
        j = (index + 5) % 52
        y.append(a[j])
    else:
        y.append(i)
z = ''.join(y)
print("Encrypted Code:",z)
```

- Guess Random Numbers
```py
#Generating Random Numbers and Guessing those numbers by user input
import random
def new_rand():
    z = random.randint(0,100)
    print(z)
    return z

def save_rand(r):
    with open("rand_generated.txt", "w") as f:   # Save the random number to a file
        f.write(str(r)+"\n")

def key(r):
    while True:
        x = int(input("Guess the number between 0 and 100: "))
        if x == r:
            save_rand(r)
            print("Congratulations, you guessed the number!")
            break
        elif x > r:
            print("Your guess is greater than the number.")
        else:
            print("Your guess is smaller than the number.")

while True:
    r = new_rand()
    key(r)
    y = input("Do you want to play again? (1/0): ")
    if y == "0":
        break
```

- Login System
```py
# Simple Login System
x={}

def menu():
    y=str(input("\n Do you already have an Account ? (Y/N) : "))
    while True:
        if(y.upper() == "Y"):
            old()
            break
        elif(y.upper() == "N"):
            i=str(input("\n Do you want to Create an Account ? (Y/N) : "))
            if i.upper()=="Y":
                new()
                break
            else:
                print("Thanks for Checking the Portal")
                exit()
        else:
            print("\n Enter a valid answer -- (Y/N) :")

def old():
    a=str(input("Enter Account Name : "))
    b=str(input("Enter Password : "))
    c=0
    while c < 5:
        if a in x and x[a]== b:
            print("\n Login Successful !!!")
            return
        else:
            c+=1
            print("Enter Correct Account Name and Password")
            a=str(input("Enter Account Name : "))
            b=str(input("Enter Password : "))
    print("\n Too many Trials , Closing the Login Portal")
    exit()
    
def new():
    a=str(input("Enter Account Name : "))
    b=str(input("Enter Password : "))
    c=str(input("Confirm Password : "))
    while a in x:
        a=str(input("User Name already exists , Please Enter a New User Name :"))
    while c!=b:
        c=str(input("Enter Correct Password to Confirm :"))
    if c==b:
        x[a]=b
        print("\n Account Successfully Created !!!")    
    
while True:
    menu()
    z=str(input("\n Do you want to continue ? (Y/N) : "))
    if(z.upper() == "N"):
        exit()
```
