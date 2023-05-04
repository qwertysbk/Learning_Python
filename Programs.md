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
a['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z',
'A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
x = input("Enter your Code: ")
y = []
for i in x:
    if i.isalpha():
        index = a.index(i)
        j = (index + 5) % 26
        y.append(a[j])
    else:
        y.append(i)
z = ''.join(y)
print("Encrypted Code:",z)
```
