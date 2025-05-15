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
