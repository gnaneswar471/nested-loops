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
