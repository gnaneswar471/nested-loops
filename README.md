# nested-loops
#nested loops
n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        print('^',end=' ')
    print()
enter the size of n 4
^ ^ ^ ^ 
^ ^ ^ ^ 
^ ^ ^ ^ 
^ ^ ^ ^

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        print(i,end=' ')
    print()
0 0 0 0 
1 1 1 1 
2 2 2 2 
3 3 3 3 

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        print(j,end=' ')
    print()
enter the size of n 4
0 1 2 3 
0 1 2 3 
0 1 2 3 
0 1 2 3 

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(i):
        print('*',end=' ')
    print()
enter the size of n 4

* 
* * 
* * *

#right angled triangle using a single loop
for i in range(5):
    print("*" *i)
*
**
***
****

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        if  i==0 or i==n-1 or j==0 or j==n-1:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()
enter the size of n 5
* * * * * 
*       * 
*       * 
*       * 
* * * * * 

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        if  i==0 or i==n-1 or j==0 or j==n-1 or i==j or i+j==n-1:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()

enter the size of n 7
* * * * * * * 
* *       * * 
*   *   *   * 
*     *     * 
*   *   *   * 
* *       * * 
* * * * * * * 

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        if j==0 or j==n-1 or i==j or i+j==n-1:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()

enter the size of n 7
*           * 
* *       * * 
*   *   *   * 
*     *     * 
*   *   *   * 
* *       * * 
*           *

n=int(input("enter the size of n"))
for i in range(n):
    for j in range(n):
        if  i==0 or i==n-1 or i==j or i+j==n-1:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()

enter the size of n 7
* * * * * * * 
  *       *   
    *   *     
      *       
    *   *     
  *       *   
* * * * * * *

n=int(input("enter the size of n"))
for i in range(5):
    for n in range(n):
        print('*',end=' ')
    print()
enter the size of n 5
* * * * * 
* * * * 
* * * 
* * 
*

n=int(input("enter the size of n"))
for i in range(1, 2*n):
    s=i if i<n else 2*n-i
    for j in range(s):
        print('*',end=' ')
    print()
enter the size of n 5
* 
* * 
* * * 
* * * * 
* * * * * 
* * * * 
* * * 
* * 
*

n=int(input())
for i in range(1,n+1):
    for s in range(n-i):
        print(' ',end=' ')
    for st in range(2*i-1):
        print('*',end=' ')
    print()
 5
        * 
      * * * 
    * * * * * 
  * * * * * * * 
* * * * * * * * *

n=int(input())
for i in range(n):
    for s in range(n-i-1):
        print(' ',end=' ')
    num=1
    for j in range(i+1):
        print(f"{num}  ",end=' ')
        num=num*(i-j)//(j+1)
    print()
 7
            1   
          1   1   
        1   2   1   
      1   3   3   1   
    1   4   6   4   1   
  1   5   10   10   5   1   
1   6   15   20   15   6   1 

n=int(input())
for i in range(n):
    for s in range(n-i-1):
        print(' ',end=' ')
    num=1
    for j in range(i+1):
        print(f"{num}  ",end=' ')
        num=num+1
    print()

 5
        1   
      1   2   
    1   2   3   
  1   2   3   4   
1   2   3   4   5 

n=int(input("enter the size of n"))
num=1
for i in range(1,n+1):
    for j in range(i):
        print(num,end=' ')
        num=num+1
    print()

enter the size of n 4
1 
2 3 
4 5 6 
7 8 9 10 

n=int(input())
for i in range(1,n+1):
    print(' '*(n-i)+'*'*(2*i-1))
 5
    *
   ***
  *****
 *******
*********

n=int(input("Enter the size"))
matrix=[[0]*n for _ in range(n)]
top,left=0,0
right,bottom=n-1,n-1
num=1
while top<=bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=num
        num+=1
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=num
        num+=1
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=num
        num+=1
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=num
        num+=1
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:3}",end=" ")
    print()

OUTPUT:
Enter the size 6
  1   2   3   4   5   6 
 20  21  22  23  24   7 
 19  32  33  34  25   8 
 18  31  36  35  26   9 
 17  30  29  28  27  10 
 16  15  14  13  12  11 

n=int(input("Enter the size"))
matrix=[[1,2,3,4,5],[6,7,8,9,10],[11,12,13,14,15],[16,17,18,19,20],[21,22,23,24,25]]
rows=len(matrix)
cols=len(matrix[0])
top,left=0,0
right,bottom=cols-1,rows-1
num=1
while top<=bottom and left<=right:
    for i in range(left,right+1):
        print(matrix[top][i],end=" ")
    top+=1
    for i in range(top,bottom+1):
        print(matrix[i][right],end=" ")
    right-=1
    for i in range(right,left-1,-1):
        print(matrix[bottom][i],end=" ")
    bottom-=1
    for i in range(bottom,top-1,-1):
        print(matrix[i][left],end=" ")
    left+=1
OUTPUT:
Enter the size 5
1 2 3 4 5 10 15 20 25 24 23 22 21 16 11 6 7 8 9 14 19 18 17 12 13 

n=int(input("Enter the size"))
matrix=[[0]*n for _ in range(n)]
top,left=0,0
right,bottom=n-1,n-1
num=ord('A')
while top<=bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=chr(num)
        num+=1
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=chr(num)
        num+=1
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=chr(num)
        num+=1 
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=chr(num)
        num+=1
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:3}",end=" ")
    print()
OUTPUT:
Enter the size 5
A   B   C   D   E   
P   Q   R   S   F   
O   X   Y   T   G   
N   W   V   U   H   
M   L   K   J   I   
