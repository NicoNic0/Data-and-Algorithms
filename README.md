# Data-and-Algorithms
Contains the Solutions to various Data &amp; Algorithms problems posed on HackerRank and LeetCode between January 2023 - April 2024

#Since the only online help I used to solve these questions was looking at libraries and command codes online, alot of the code may be unorganized, messy and inefficient

#------------------------------------------------------------------------------Factorial------------------------------------------------------------------------------
def fact(n):
    while (n >= 1):
        return (n * fact(n-1))
    else:
        return 1
    
print(fact(5))

#-------------------------------------------------------------------------------Fiboancci------------------------------------------------------------------------------
list = [0,1] 
fib = input("type number")
fib = int(fib)
x = 07
while fib >= 0:
    x = list[0] + list[1]
    list[0] = list[1]
    list[1] = x
    fib = fib - 1
    if fib >= 0:
      print(list[1])

#-------------------------------------------------------------------------------Binary Gap------------------------------------------------------------------------------

def check_is_digit(input_str):
    if input_str.strip().isdigit():
        print("User input is Number")
    else:
        print("User input is string")

binarynum = input("input number")
binarynum = int(binarynum)

bin_a = format(binarynum, 'b')

list = [int(x) for x in str(bin_a)]
print(list)

loop = 0
count = len(list)
list1 = [int(0)]*count
zero = 0

while loop < len(list):
  if list[loop] == 0:
    loop = loop+1
    list1[zero] = list1[zero] + 1
  
  elif list[loop] > 0:
    loop = loop+1
    zero = zero + 1 
    
list1.sort()
print(list1[-1])
        
#-------------------------------------------------------------------------------Plus Minus---------------------------------------------------------------------

import math
arr = [1,2,0,-2,-9]
x = len(arr) + 1
c = 0
while (x > 1):
  if arr[c] > 0:
    arr[c] = 1
    c = c + 1
    x = x - 1
  elif arr[c] == 0:
    arr[c] = 0
    c = c + 1
    x = x - 1
  else:
    arr[c] = -1
    c = c + 1
    x = x - 1

print (arr)
y = len(arr) + 1
arr1 = [int(0)]*3
c1 = 0

while y > 1:
  if arr[c1] > 0:
    arr1[0] = arr1[0] + 1
    c1 = c1 + 1
    y = y - 1
  elif arr[c1] == 0:
    arr1[1] = arr1[1] + 1
    c1 = c1 + 1
    y = y - 1
  elif arr[c1] < 0:
    arr1[2] = arr1[2] + 1
    c1 = c1 + 1
    y = y - 1
    
print (arr1)
value1 = (arr1[0]/len(arr))
value2 = (arr1[1]/len(arr))
value3 = (arr1[2]/len(arr))
print(format(value1, '.6f'))
print(format(value2, '.6f'))
print(format(value3, '.6f'))

#-------------------------------------------------------------------------------Maximum and Minimum---------------------------------------------------------------------

arr = [1,3,5,13,9]

arr.sort()
print(arr)

x = ((arr[0])+(arr[1])+(arr[2])+(arr[3]))
y = ((arr[1])+(arr[2])+(arr[3])+(arr[4]))
print(x)
print(y)

#-------------------------------------------------------------------------------Time Conversion---------------------------------------------------------------------

#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'timeConversion' function below.
#
# The function is expected to return a STRING.
# The function accepts STRING s as parameter.
#

def timeConversion(s):
    s = str(s)
    x = s.find('PM')
    size = len(s)

    if x > 0:
        if int(s[0:2]) == 12:
            time = s[:len(s) - 2]
            print(time)
        elif int(s[0:2]) == 11:
            twe = ('23')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 10:
            twe = ('22')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 9:
            twe = ('21')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 8:
            twe = ('20')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 7:
            twe = ('19')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 6:
            twe = ('18')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 5:
            twe = ('17')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 4:
            twe = ('16')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 3:
            twe = ('15')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 2:
            twe = ('14')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 1:
            twe = ('13')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
    elif x == -1:
        if int(s[0:2]) == 12:
            twe = ('00')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        else:
            time = s[:len(s) - 2]
            print(time)

if __name__ == '__main__':

    s = input()

    result = timeConversion(s)

#-------------------------------------------------------------------------------FizzBuzz----------------------------------------------------------------

def fizzBuzz(n):
    x = 0
    list = range(n)
    
    while n > 0:
        x = x + 1
        if list[x]%3 == 0 and list[x]%5 == 0:
            if list[x] == 1:
                print(1)
            else:
                print('FizzBuzz')
                n = n - 1
        elif list[x] % 3 == 0:
            print ('Fizz')
            n = n - 1
        elif list[x] %5 == 0: 
            print ('Buzz')
            n = n - 1
        else:
            print(list[x])
            n = n - 1

fizzBuzz(15)

def fizzBuzz(n):
    length = len(n)
    x = 0
    
    while length > 0:
        if (n[x] % 3) == 0 and (n[x] % 5) == 0:
            if n[x] == 1:
                print (1)
                lentgh = length - 1
                x = x + 1
            else:
                print('FizzBizz')
                lentgh = length - 1
                x = x + 1
        elif n[x] % 3 == 0:
            print ('Fizz')
            lentgh = length - 1
            x = x + 1
        elif n[x] % 5 == 0:
            print ('Buzz')
            lentgh = length - 1
            x = x + 1
        else:
            print (n[x])
            lentgh = length - 1
            x = x + 1
        
        return n

#-------------------------------------------------------------------------------Lonely Integer---------------------------------------------------------------

#a.sort()
 #   x = len(a)
  #  count = 0
   # while x > 0:
    ###      x = x - 1
       # elif a[count] < (a[count + 1]):
        #    count = count + 1
         ##      x = x - 1
        #else:
         #   print (a[count])
          #  break

def lonelyinteger(a):
    for number in a:
        if(a.count(number) == 1):
            return(number)
        
#-------------------------------------------------------------------------------Diagonal Difference---------------------------------------------------------------

def diagonalDifference(arr):
    x = arr[0][0] + arr[1][1] + arr[2][2]
    y = arr[0][2] + arr [1][1] + arr [2][0]
    z = [x ,y]
    z.sort(reverse=True)
    result = (z[0]-z[1])
    return(result)
        
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    arr = []

    for _ in range(n):
        arr.append(list(map(int, input().rstrip().split())))

    result = diagonalDifference(arr)

    fptr.write(str(result) + '\n')

    fptr.close()
    
#-------------------------------------------------------------------------------Diagonal Difference # 2---------------------------------------------------------------

a = 0
b = 0
x = 0
loop = (len(arr))
while loop > 0:
        x = (arr[a][b]) + x
        a = a + 1
        b = b + 1
        loop = loop - 1

c = 0 
d = (len(arr)-1)
y = 0
loop2 = len(arr)
while loop2 > 0:
        y = (arr[c][d]) + y
        c = c + 1
        d = d - 1
        loop2 = loop2 - 1
        
z = [x ,y]
z.sort(reverse=True)
result = (z[0]-z[1])






#------------------------------------------------------------------------------Factorial------------------------------------------------------------------------------
def fact(n):
    while (n >= 1):
        return (n * fact(n-1))
    else:
        return 1
    
print(fact(5))

#-------------------------------------------------------------------------------Fiboancci------------------------------------------------------------------------------
list = [0,1] 
fib = input("type number")
fib = int(fib)
x = 07
while fib >= 0:
    x = list[0] + list[1]
    list[0] = list[1]
    list[1] = x
    fib = fib - 1
    if fib >= 0:
      print(list[1])

#-------------------------------------------------------------------------------Binary Gap------------------------------------------------------------------------------

def check_is_digit(input_str):
    if input_str.strip().isdigit():
        print("User input is Number")
    else:
        print("User input is string")

binarynum = input("input number")
binarynum = int(binarynum)

bin_a = format(binarynum, 'b')

list = [int(x) for x in str(bin_a)]
print(list)

loop = 0
count = len(list)
list1 = [int(0)]*count
zero = 0

while loop < len(list):
  if list[loop] == 0:
    loop = loop+1
    list1[zero] = list1[zero] + 1
  
  elif list[loop] > 0:
    loop = loop+1
    zero = zero + 1 
    
list1.sort()
print(list1[-1])
        
#-------------------------------------------------------------------------------Plus Minus---------------------------------------------------------------------

import math
arr = [1,2,0,-2,-9]
x = len(arr) + 1
c = 0
while (x > 1):
  if arr[c] > 0:
    arr[c] = 1
    c = c + 1
    x = x - 1
  elif arr[c] == 0:
    arr[c] = 0
    c = c + 1
    x = x - 1
  else:
    arr[c] = -1
    c = c + 1
    x = x - 1

print (arr)
y = len(arr) + 1
arr1 = [int(0)]*3
c1 = 0

while y > 1:
  if arr[c1] > 0:
    arr1[0] = arr1[0] + 1
    c1 = c1 + 1
    y = y - 1
  elif arr[c1] == 0:
    arr1[1] = arr1[1] + 1
    c1 = c1 + 1
    y = y - 1
  elif arr[c1] < 0:
    arr1[2] = arr1[2] + 1
    c1 = c1 + 1
    y = y - 1
    
print (arr1)
value1 = (arr1[0]/len(arr))
value2 = (arr1[1]/len(arr))
value3 = (arr1[2]/len(arr))
print(format(value1, '.6f'))
print(format(value2, '.6f'))
print(format(value3, '.6f'))

#-------------------------------------------------------------------------------Maximum and Minimum---------------------------------------------------------------------

arr = [1,3,5,13,9]

arr.sort()
print(arr)

x = ((arr[0])+(arr[1])+(arr[2])+(arr[3]))
y = ((arr[1])+(arr[2])+(arr[3])+(arr[4]))
print(x)
print(y)

#-------------------------------------------------------------------------------Time Conversion---------------------------------------------------------------------

#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'timeConversion' function below.
#
# The function is expected to return a STRING.
# The function accepts STRING s as parameter.
#

def timeConversion(s):
    s = str(s)
    x = s.find('PM')
    size = len(s)

    if x > 0:
        if int(s[0:2]) == 12:
            time = s[:len(s) - 2]
            print(time)
        elif int(s[0:2]) == 11:
            twe = ('23')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 10:
            twe = ('22')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 9:
            twe = ('21')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 8:
            twe = ('20')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 7:
            twe = ('19')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 6:
            twe = ('18')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 5:
            twe = ('17')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 4:
            twe = ('16')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 3:
            twe = ('15')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 2:
            twe = ('14')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        elif int(s[0:2]) == 1:
            twe = ('13')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
    elif x == -1:
        if int(s[0:2]) == 12:
            twe = ('00')
            res = s.replace(s[0:2], twe, 1)
            time = res[:len(res) - 2]
            print(time)
        else:
            time = s[:len(s) - 2]
            print(time)

if __name__ == '__main__':

    s = input()

    result = timeConversion(s)

#-------------------------------------------------------------------------------FizzBuzz----------------------------------------------------------------

def fizzBuzz(n):
    x = 0
    list = range(n)
    
    while n > 0:
        x = x + 1
        if list[x]%3 == True and list[x]%5 == True:
            if list[x] == 1:
                print(1)
            else:
                print(list[x],'FizzBuzz')
                n = n - 1
        elif list[x] % 3 == True:
            print (list[x],'Fizz')
            n = n - 1
        elif list[x] %5 == True: 
            print (list[x],'Buzz')
            n = n - 1
        else:
            print(list[x])
            print(x)
            n = n - 1

fizzBuzz(15)

def fizzBuzz(n):
    length = len(n)
    x = 0
    
    while length > 0:
        if (n[x] % 3) == 0 and (n[x] % 5) == 0:
            if n[x] == 1:
                print (1)
                lentgh = length - 1
                x = x + 1
            else:
                print('FizzBizz')
                lentgh = length - 1
                x = x + 1
        elif n[x] % 3 == 0:
            print ('Fizz')
            lentgh = length - 1
            x = x + 1
        elif n[x] % 5 == 0:
            print ('Buzz')
            lentgh = length - 1
            x = x + 1
        else:
            print (n[x])
            lentgh = length - 1
            x = x + 1
        
        return n

#-------------------------------------------------------------------------------Lonely Integer---------------------------------------------------------------

#a.sort()
 #   x = len(a)
  #  count = 0
   # while x > 0:
    ###      x = x - 1
       # elif a[count] < (a[count + 1]):
        #    count = count + 1
         ##      x = x - 1
        #else:
         #   print (a[count])
          #  break

def lonelyinteger(a):
    for number in a:
        if(a.count(number) == 1):
            return(number)
        
#-------------------------------------------------------------------------------Diagonal Difference---------------------------------------------------------------

def diagonalDifference(arr):
    x = arr[0][0] + arr[1][1] + arr[2][2]
    y = arr[0][2] + arr [1][1] + arr [2][0]
    z = [x ,y]
    z.sort(reverse=True)
    result = (z[0]-z[1])
    return(result)
        
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    arr = []

    for _ in range(n):
        arr.append(list(map(int, input().rstrip().split())))

    result = diagonalDifference(arr)

    fptr.write(str(result) + '\n')

    fptr.close()
    
#-------------------------------------------------------------------------------Diagonal Difference # 2---------------------------------------------------------------

a = 0
b = 0
x = 0
loop = (len(arr))
while loop > 0:
        x = (arr[a][b]) + x
        a = a + 1
        b = b + 1
        loop = loop - 1

c = 0 
d = (len(arr)-1)
y = 0
loop2 = len(arr)
while loop2 > 0:
        y = (arr[c][d]) + y
        c = c + 1
        d = d - 1
        loop2 = loop2 - 1
        
z = [x ,y]
z.sort(reverse=True)
result = (z[0]-z[1])

#-------------------------------------------------------------------------------Test 2---------------------------------------------------------------



matrix = ([112,45,67,43],[45,87,42,98],[53,12,56,97],[43,67,9,87])

swapvar = 0
i = 6
print("testing")

matrix1 = [ matrix[i:i+4] for i in range(0,len(matrix),4) ]
for l in matrix:
    print ("original", l)

while i > 0:
    # left top down  
    if ((matrix[0][0]) + (matrix[1][0])) < ((matrix[2][0]) + (matrix[3][0])):
        swapvar = (matrix[0][0])
        (matrix[0][0]) = matrix[3][0]
        matrix[3][0] = swapvar
            
        swapvar = (matrix[1][0])
        (matrix[1][0]) = matrix[2][0]
        matrix[2][0] = swapvar
        i = i - 1
    #left2 top down
    if ((matrix[0][1]) + (matrix[1][1])) < ((matrix[2][1]) + (matrix[3][1])):
        swapvar = (matrix[0][1])
        (matrix[0][1]) = matrix[3][1]
        matrix[3][1] = swapvar
            
        swapvar = (matrix[1][1])
        (matrix[1][1]) = matrix[2][1]
        matrix[2][1] = swapvar
        i = i - 1
    #left3  top down
    if ((matrix[0][2]) + (matrix[1][2])) < ((matrix[2][2]) + (matrix[3][2])):
        swapvar = (matrix[0][2])
        (matrix[0][2]) = matrix[3][2]
        matrix[3][2] = swapvar
        
        swapvar = (matrix[1][2])
        (matrix[1][2]) = matrix[2][2]
        matrix[2][2] = swapvar
        i = i - 1
    #left4 top down
    if ((matrix[0][3]) + (matrix[1][3])) < ((matrix[2][3]) + (matrix[3][3])):
        swapvar = (matrix[0][3])
        (matrix[0][3]) = matrix[3][3]
        matrix[3][3] = swapvar
            
        swapvar = (matrix[1][3])
        (matrix[1][3]) = matrix[2][3]
        matrix[2][3] = swapvar
        i = i - 1
    else:
        break

i = 6

while i > 0:
    # top1 left right
    if ((matrix[0][0]) + (matrix[0][1])) < ((matrix[0][2]) + (matrix[0][3])):
        swapvar = (matrix[0][0])
        (matrix[0][0]) = matrix[0][3]
        matrix[0][3] = swapvar
            
        swapvar = (matrix[0][1])
        (matrix[0][1]) = matrix[0][2]
        matrix[0][2] = swapvar
        i = i - 1
    #top2 left right
    if ((matrix[1][0]) + (matrix[1][1])) < ((matrix[1][2]) + (matrix[1][3])):
        swapvar = (matrix[1][0])
        (matrix[1][0]) = matrix[1][3]
        matrix[1][3] = swapvar
            
        swapvar = (matrix[1][1])
        (matrix[1][1]) = matrix[1][2]
        matrix[1][2] = swapvar
        i = i - 1
    #top3  left right
    if ((matrix[2][0]) + (matrix[2][1])) < ((matrix[2][2]) + (matrix[2][3])):
        swapvar = (matrix[2][0])
        (matrix[2][0]) = matrix[2][3]
        matrix[2][3] = swapvar
            
        swapvar = (matrix[2][1])
        (matrix[2][1]) = matrix[2][2]
        matrix[2][2] = swapvar
        i = i - 1
    #top4 left right
    if ((matrix[3][0]) + (matrix[3][1])) < ((matrix[3][2]) + (matrix[3][3])):
        swapvar = (matrix[3][0])
        (matrix[3][0]) = matrix[3][3]
        matrix[3][3] = swapvar
            
        swapvar = (matrix[3][1])
        (matrix[3][1]) = matrix[3][2]
        matrix[3][2] = swapvar
        i = i - 1
    else:
        break
    
        
a = matrix[0][0]
s = matrix [0][1]
d = matrix [1][0]
f = matrix [1][1]

sum = a + s + d + f
print (sum)

matrix1 = [ matrix[i:i+4] for i in range(0,len(matrix),4) ]
for l in matrix:
    print ("edited", l)
        


#-------------------------------------------------------------------------------zig zag sequence (unfinished)---------------------------------------------------------------

 a.sort()
    mid = len(a)//2
    mid_num = max(a)
    length = len(a)
    last = len(a) - 1
    del a[last]
    
    
    s_half = a[:mid]
    e_half = a[mid:] 
    s_half.sort()
    e_half.sort(reverse = True)
    result = [0]*length
    
    num = 0
    while num < len(s_half):
        result[num] = s_half[num]
        num += 1
    result[num] = mid_num
    num += 1
    num1 = 0
    while num1 < len(e_half):
        result[num] = e_half[num1]
        num += 1
        num1 += 1
    print (result)
#-------------------------------------------------------------------------------Tower Breakers---------------------------------------------------------------

def towerBreakers(n, m):
    x = 0
    if m == 1 or n % 2 == 0:
        x = 2
    else:
        x = 1
    return (x)
    
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    t = int(input().strip())

    for t_itr in range(t):
        first_multiple_input = input().rstrip().split()

        n = int(first_multiple_input[0])

        m = int(first_multiple_input[1])

        result = towerBreakers(n, m)

        fptr.write(str(result) + '\n')

    fptr.close()

#-------------------------------------------------------------------------------Caesar Cipher---------------------------------------------------------------
from collections import deque
s = ("middle-Outz")
k = 2

alph = ["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"]
alph1 = deque(["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"])
ALPH = ["A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"]
ALPH1 = deque(["A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"])
alph1.rotate(k)
ALPH1.rotate(k)
loop = 0

x = []
new = []

while loop < len(s):
    if s[loop] == "-":
        new.append("-")
        loop = loop + 1
    elif s[loop].isupper():
        x = ALPH1.index(s[loop])
        new.append(ALPH[x])
        loop = loop + 1
        x = 0
    else:
        x = alph1.index(s[loop])
        new.append(alph[x])
        loop = loop + 1
        x = 0
        

print(new)

#-------------------------------------------------------------------------------Test 3---------------------------------------------------------------------

def check_is_digit(input_str):
    if input_str.strip().isdigit():
        print("User input is Number")
    else:
        print("User input is string")

def createList(r1, r2):
  if (r1 == r2):
    return r1
  else:
    res = []
    while(r1 < r2+1 ):
      res.append(r1)
      r1 += 1
    return res

def Convert(string):
    list1 = []
    list1[:0] = string
    return list1

s = [  "ccco","baab", "aaaa", "baaa", "baa", "cccco","abcba"]
x = len(s)
var = 0


#--------------------------------if s[var] is all same == 0-----------------------
while x > 0:
    if (len(set(s[var]))==1):
      conv = Convert(s[var])
      length = len(s[var])
      print(-1, var)
      var = var + 1
      x = x - 1
  #--------------------------------if len(s[var])% 2 == 0-----------------------
    else:
      conv = Convert(s[var])
      length = len(s[var])
      if length % 2 == 0:
        length1 = len(conv)
        y = 0
  #--------------------------------if s[var] == 0:len() -----------------------
        half = length/2
        end = len(s[var]) - 1
        i = 0
        while conv[0 + i] == conv[end - i] and i != half:
          i = i + 1
          if i == half:
            print(-1, var)
  #--------------------------------if s[var] != 0:len() -----------------------
        else:
          while y != length1 and i != half:
            if s[var][y] == s[var][y + 1]:
              y = y + 1
            elif s[var][y] != s[var][y + 1]:
              if 0 <= y + 2 < length1:
                if s[var][y + 1] != s[var][y + 2]:
                  print(conv.index(conv[y + 1]), var)
                  del conv[y + 1]
                  s[var] = conv
                  y = length1
                elif s[var][y + 1] == s[var][y + 2]:
                  print(conv.index(conv[y + 1]), var)
                  del conv[y]
                  s[var] = conv
                  y = length1
              else:
                print(conv.index(conv[y + 1]), var)
                del conv[y + 1]
                s[var] = conv
                y = length1

#--------------------------------if len(s[var])% 2 == 1-----------------------
      else:
        half = length/2 - 0.5
        end = len(s[var]) - 1
        i = 0
#--------------------------------2 if s[var] == 0:len()-----------------------
        while conv[0 + i] == conv[end - i] and i != half:
          i = i + 1
          if i == half:
            print(-1, var)

#--------------------------------2 if s[var] != 0:len()-----------------------
        y = 0 
        length1 = len(conv)
        while y != length1 and i != half:
            if (len(set(s[var]))==1):
              conv = Convert(s[var])
              length = len(s[var])
              print(-1)
              var = var + 1
              x = x - 1
            elif s[var][y] == s[var][y + 1]:
              y = y + 1
            elif s[var][y] != s[var][y + 1]:
              if 0 <= y + 2 < length1:
                if s[var][y + 1] == s[var][y + 2]:
                  print(conv.index(conv[y + 1]), var)
                  del conv[y]
                  s[var] = conv
                  y = length1
                else:
                  print(conv.index(conv[y + 1]), var)
                  del conv[y + 1]
                  s[var] = conv
                  y = length1
              else:
                  print(conv.index(conv[y + 1]), var)
                  del conv[y + 1]
                  s[var] = conv
                  y = length1

      var = var + 1
      x = x - 1
      

#-------------------------------------------------------------------------------Intro to Def and Rand---------------------------------------------------------------------

import random
 
def add_numbers(num1, num2):
  add_result = num1 + num2
  return add_result
def mult_numbers(num1, num2):
  mul_result = num1 * num2 
  return mul_result

num1 = random.randint(1,9)
num2 = random.randint(1,9)

add_numbers(num1, num2)
add_result = add_numbers(num1, num2)
print(add_result)
mul_result = mult_numbers(num1, num2)
print(mul_result)
    
#------------------------------------------------------merge sort ----------------------------------------------------------------------------------------------
def merge_sort(array):
    if len(array) <= 1:
        return array
  
    midpoint = int(len(array)/2)

    left = merge_sort(array[:midpoint])
    right = merge_sort(array[midpoint:])

    return merge(left, right)

def merge(left, right):

  result = []
  left_pointer = right_pointer = 0


  while left_pointer < len(left) and right_pointer < len(right):

    if left[left_pointer] < right[right_pointer]:

      result.append(left[left_pointer])
      left_pointer += 1

    else:

      result.append(right[right_pointer])
      right_pointer += 1

  result.extend(left[left_pointer:])
  result.extend(right[right_pointer:])

  return result

def main():
  array = [5, 4, 3, 2, 1]
  print(array)

  result = merge_sort(array)
  print(result)

if __name__ == "__main__":
  main()
#-------------------------------------------------------------Binary Search---------------------------------------------------------------------------------------

def bin_search(array, x, half):
    
  
  if len(array) < 1:
    result = "none"
    return result
  elif len(array) == 1 and array[0] != x:
    result = "none"
    return result
  elif len(array) == 1 and array[0] == x: 
    result = x
    return result


  loop = half
  while loop > 0:
    half = int(len(array)/2)
    if x > array[half]:
      array = array[half:]
      loop +- 1
    elif x < array[half]:
      array = array[:half]
      loop +- 1
    elif x == array[half]:
      result = array[half]
      return result
  result = "none"
  return result
    


array = [20, 30, 50, 60, 80, 110, 130, 140, 170]
x = 170
length = int(len(array))
half = int(length/2)

bin_search(array, x, half)
result = bin_search(array, x, half)
print(result)



#-------------------------------------------------------------Failed Personal Merge Sort 1---------------------------------------------------------------------------
import random
rand_list=[]
n=10
for i in range(n):
    rand_list.append(random.randint(1,9))
arr = [6, 8, 5, 3, 4, 7]
#[arr.append(x) for x in rand_list if x not in arr]

def divide(arr):
  if len(arr) == 1:
    return 
  
  mid = int(len(arr)/2)

  left = arr[:mid]
  right = arr[mid:]
  left.sort()
  right.sort()

  return (left, right)

def sum(left, right):
    
    final = [0]*len(arr)
    left_pointer = right_pointer = final_pointer = 0
    print(len(final))

    for i in final:
          if final_pointer == len(final):
            print("here")
            return
          else:
            if right_pointer >= len(right):
                final[final_pointer] = left[left_pointer]
                print(left_pointer, "left point")
                del left[left_pointer]
                left_pointer = left_pointer + 1
                final_pointer += 1
                print(left, right)
                print(final)
            elif left_pointer >= len(left):
                final[final_pointer] = right[right_pointer]
                right_pointer = right_pointer + 1
                final_pointer += 1
                print(left, right)
                print(final)

            elif left[left_pointer] > right[right_pointer]:
                print(right_pointer, "right point")
                final[final_pointer] = right[right_pointer]
                #del right[right_pointer]
                right_pointer = right_pointer + 1
                final_pointer += 1
                print(left, right)
                print(final)
            elif left[left_pointer] < right[right_pointer]:
                final[final_pointer] = left[left_pointer]
                print(left_pointer, "left point")
                #del left[left_pointer]
                left_pointer = left_pointer + 1
                final_pointer += 1
                print(left, right)
                print(final)

print(arr, "original")
divide(arr)
left, right = divide(arr)
print(left,right)

sum(left, right)

#------------------------------------------------------Failed Personal Island Problem------------------------------------------------------------------------------------
grid = [
  ["1","1","0","1","1"],
  ["1","1","0","0","0"],
  ["0","0","1","0","0"],
  ["0","0","0","1","1"]
]

#formula for finding coordinates:
# (row num) * (num of colomns) + colomn = index
# (index) / (num of colomns) = Row 
# (index) % (num of colomns) = Colomn

def computing_position(row_num, num_col, col):
  index = row_num * num_col + col 
  print(index)
  row = index / num_col
  col = index % num_col
  print("row is", row, "col is", col)


def counting_islands(grid):
  grid.append(["0","0","0","0","0"])
  x = i = j = 0
  num = num1 = 1
  length = len(grid[i]) + 1
  islands = []
  loop = len(grid)
  
  while loop > 0:
    while j + 1 < len(grid[x]):
      print("i is", i, "j is", j, "grid[x]", len(grid[x]))

      if int(grid[i][j]) == 0:
        j = j + 1
        print("i is", i, "j is", j, "grid[x]", len(grid[x]))
      else:
        grid[i][j] = 0

        while length > 1:
          print(grid[x])
          x += 1
          length = length - 1
        x = 0
        length = len(grid[i]) + 1
        print("------------------------------")
        print("i is", i, "j is", j, "grid[x]", len(grid[x]))

        #checking right 1 down all loop
        while int(grid[i][j+num]) == 1:
          grid[i][j+num] = 0

          while length > 1:
              print(grid[x])
              x += 1
              length = length - 1
          x = 0
          length = len(grid[i]) + 1
          print("------------------------------")
          print("i is", i, "j is", j, "grid[x]", len(grid[x]))

          while int(grid[i+num1][j+num]) == 1:
            grid[i+num1][j+num] = 0
            num1 = num1 + 1

            while length > 1:
              print(grid[x])
              x += 1
              length = length - 1
            x = 0
            length = len(grid[i]) + 1
            print("------------------------------")
            print("i is", i, "j is", j, "grid[x]", len(grid[x]))

          num1 = 1
          num = num + 1
        num = 1

        #checking down 1 right all loop
        while int(grid[i+num][j]) == 1:
          grid[i+num][j] = 0

          while length > 1:
            print(grid[x])
            x += 1
            length = length - 1
          x = 0
          length = len(grid[i]) + 1
          print("------------------------------")
          print("i is", i, "j is", j, "grid[x]", len(grid[x]))

          while int(grid[i+num][j+num1]) == 1:
            grid[i+num][j+num1] = 0
            num1 = num1 + 1

            while length > 1:
              print(grid[x])
              x += 1
              length = length - 1
            x = 0
            length = len(grid[i]) + 1
            print("------------------------------")
            print("i is", i, "j is", j, "grid[x]", len(grid[x]))
            
          num1 = 1
          num = num + 1
        num = 1

      j = j + 1
  
    i += 1
    j = 0
    loop = loop - 1
    print("loop is", loop)
  
  while length > 1:
      print(grid[x])
      x += 1
      length = length - 1

counting_islands(grid)



#--------------------------------------------------------------------------------------Breadth First Search Easy--------------------------------------------------------
from queue import Queue

graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}

visited = []
queue = []

def bfs(visited, graph, node):
  visited.append(node)
  queue.append(node)

  while queue:
    m = queue.pop(0)
    print (m, end = "")

    for neighbour in graph[m]:
      if neighbour not in visited:
        visited.append(neighbour)
        queue.append(neighbour)
        
bfs(visited, graph, '5')
#--------------------------------------------------------------------------------------Breadth First Search Complicated--------------------------------------------------------

from queue import Queue 

adj_list = {
    'a': ['b', 'd'],
    'b': ['a', 'c'],
    'c': ['b'],
    'd': ['a', 'e', 'f'],
    'e': ['d', 'f', 'g'],
    'f': ['d', 'e', 'h'],
    'g': ['e', 'h'],
    'h': ['g', 'f']
    }

visited = {}
level = {}
parent = {}
bfs_travel_output = []
queue = Queue()

for node in adj_list.keys():
  visited[node] = False
  parent[node] = None
  level[node] = -1

print (visited)
print (level)
print (parent)

s = "a"
visited[s] = True 
level[s] = 0
queue.put(s)

while not queue.empty():
  u = queue.get()
  bfs_travel_output.append(u)

  for v in adj_list[u]:
    if not visited[v]:
      visited[v] = True
      parent[v] = u
      level[v] = level[u] + 1
      queue.put(v)

print(bfs_travel_output)
print(level)

#shortest distance from source node
print(level['d'])

#shortest path from source code
v = 'g'
path = []
while v is not None:
  path.append(v)
  v = parent[v]
path.reverse()
print(path)



#----------------------------------------------------------------------------------------Depth First Search Easy----------------------------------------

graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}

visited = set()

def dfs(visited, graph, node):
  if node not in visited:
    print(node)
    visited.add(node)
    for neighbor in graph[node]:
      dfs(visited, graph, neighbor)

dfs(visited, graph, '5')

#----------------------------------------------------------------------------------------Depth First Search hard----------------------------------------
adj_list = {
    'a': ['b', 'c'],
    'b': ['d', 'e'],
    'c': ['b', 'f'],
    'd': [],
    'e': ['f'],
    'f': []
}

color = {}
parent = {}
trav_time = {}
dfs_travel_output = []

for node in adj_list.keys():
  color[node] = 'w'
  parent[node] = None
  trav_time[node] = [-1, -1]

print (parent)
print(trav_time)
time = 0

def dfs_util(u):
  global time
  color[u] = 'g'
  trav_time[u][0] = time
  dfs_travel_output.append(u)
  time += 1

  for v in adj_list[u]:
    if color[v] == 'w':
      parent[v] = u
      dfs_util(v)
  color[u] = 'b'
  trav_time[u][1] = time
  time += 1
  
dfs_util('a')
print (dfs_travel_output)
print (parent)
print (trav_time)

#tells us the travle time from each node (start time, end time)
for node in adj_list.keys():
  print(node, " -> ", trav_time[node])

#-----------------------------------------------------------------------Binary Search-------------------------------------------------------------
arr = [ -2, 3, 4, 7, 8, 9, 11, 13]

target = 11

def search(arr, target):
  left = 0
  right = len(arr) - 1
  while left <= right:
    mid = int((left + right) /2)
    if arr[mid] == target:
      return mid
    elif arr[mid] > target:
      right = mid - 1
    else:
      left = mid + 1

search(arr, target)
#----------------------------------------------------------------------hour glass 2 x 2---------------------------------------------------------------
a = 0
b = 1
c = 2

len_row = len(arr)
len_col = len(arr[0])
ans = []

while len_col >2:
    result1 = result2 = result3 = result = 0
    d = 0
    e = 1
    f = 2
    while len_row > 2:
        result1 = arr[a][d] + arr[a][e] + arr[a][f]
        result2 = arr[b][e]
        result3 = arr[c][d] + arr[c][e] + arr[c][f]
        ans.append (result1 + result2 + result3)
        d += 1
        e += 1
        f += 1
        len_row = len_row - 1
        
    a = a + 1
    b = b + 1
    c = c + 1
    len_col = len_col - 1
    len_row = len(arr)
#----------------------------------------------------------------------------------------------------------------------------------------------------

#----------------------------------------------------------------------------------------------------------------------------------------------------

#----------------------------------------------------------------------------------------------------------------------------------------------------

#----------------------------------------------------------------------------------------------------------------------------------------------------

#----------------------------------------------------------------------------------------------------------------------------------------------------

#----------------------------------------------------------------------------------------------------------------------------------------------------

#----------------------------------------------------------------------------------------------------------------------------------------------------

