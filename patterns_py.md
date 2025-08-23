Solid Type Patterns

square 
def square(n):
    for i in range(1,n+1):
        for j in range(1,n+1):
            print("*",end=" ")
        print()
n= int(input("enter n:"))
square(n)

Increasing Triangle 
def triangle(n):
    for i in range(1,n+1):
        for j in range(1,i+1):
            print("*",end=" ")
        print()
n= int(input("enter n:"))
triangle(n)

Decreasing Triangle 

def dec_triangle(n):
    for i in range(n,0,-1):
        for j in range(1,i+1):
            print("*",end=" ")
        print()
n= int(input("enter n:"))
dec_triangle(n)

reverse Increasing Triangle 

def revinc_triangle(n):
    for i in range(1,(n-3)):
        for j in range(1,n+1):
            print(" "*(n-j)+"*"*j)
            
        print()
n= int(input("enter n:"))
revinc_triangle(n)

Reverse Decreasing 
def revinc_triangle(n):
    for i in range(1,n-3):
        for j in range(1,n+1):
            print(" "*(j-1)+"*"*(n-j+1))
            
        print()
n= int(input("enter n:"))
revinc_triangle(n)


K-Pattern 

def K_pattern(n):
    for i in range(n,0,-1):
        for j in range(1,i+1):
            print("*",end=" ")
        print()
    for i in range(1,n+1):
        for j in range(1,i+1):
            print("*",end=" ")
        print()
n= int(input("enter n:"))
K_pattern(n)


Perfect Triangle 

def Perfect_triangle(n):
    for i in range(1,(n-3)):
        for j in range(1,n+1):
            print(" "*(n-j)+"* "*j)
            
        print()
n= int(input("enter n:"))
Perfect_triangle(n)


Diamond Shape 

def Diamond_shape(n):
    for i in range(1,(n-3)):
        for j in range(1,n+1):
            print(" "*(n-j)+"* "*j)
    for i in range(1,n-3):
        for j in range(1,n+1):
            print(" "*(j-1)+"* "*(n-j+1))
        print()
n= int(input("enter n:"))
Diamond_shape(n)


Crown shape 

def Crown_shape(n):
    for i in range(n,0,-1):
        right_d="* "*i
        left_d="   "*(n-i)+"* "*i
        act_Left_d="   "*(n-i)+"* "*i
        print(right_d+""+left_d+""+act_Left_d)
    
n= int(input("enter n:"))
Crown_shape(n)


Upper crown shape
def upper_Crown_shape(n):
    for i in range(1,n+1):
        right_d= "  "*(n-i) + "* " *i
        left_d=  " "*(n-i) + "* " *i
        # act_Left_d="   "*(n-i)+"* "*i
        print(left_d + right_d + right_d )
    
n= int(input("enter n:"))
upper_Crown_shape(n)


Butterfly shape 

def Butterfly_shape(n):
    for i in range(1,n+1):
        left_d=  "*"*i
        right_part = "  "*((n)-i)+"*"*i
        print(left_d + right_part )
    for i in range(n,0,-1):
        right_d= "  "*(n-i) + "*" *i
        left_d=  "*"*i
        print(left_d + right_d)
n= int(input("enter n:"))
Butterfly_shape(n)



Hallow type patterns 

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if i==1 or i==n:
                print("* ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)


side striaght lines of square 

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if j==1 or j==n:
                print("* ",end='')
            else:
                print(" ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)

forward slash

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if i==j:
                print("* ",end='')
            else:
                print(" ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)


Backward Slash 

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if (i+(j-1)== n):
                print("* ",end='')
            else:
                print(" ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)

x symbol 

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if (i+(j-1)== n) or i==j:
                print("* ",end='')
            else:
                print(" ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)


hallow increasing triangle 

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n):
            if j==1 or i==j or i==n:
                print("* ",end='')
            else:
                print(" ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)


H pattern
def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if j==1 or j==n or i==3:
                print("* ",end='')
            else:
                print("  ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)

Swasthik Pattern 

def striaght_line(n):
    for i in range(1,n+1):
        for j in range(1, n+1):
            if j==1 or i==n:
                print("* ",end='')
            else:
                print("  ",end='')
        for j in range(1, n+1):
            if j==1 or i==n or i==1:
                print("* ",end='')
            else:
                print("  ",end='')
        print()
    for i in range(1,n+1):
        for j in range(1, n+1):
            if j==(n) or i==(n):
                print("* ",end='')
            else:
                print("  ",end='')
        for j in range(1, n+1):
            if j==(n) :
                print("* ",end='')
            else:
                print("  ",end='')
        print()
n=int(input("Enter n:"))
striaght_line(n)


