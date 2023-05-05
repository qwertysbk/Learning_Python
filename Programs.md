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
