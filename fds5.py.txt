
def shell_sort():
 l=[]
 n=int(input("Enter the number of items in a list :"))
 for i in range (n):
        a=int(input("Enter the values of the list :"))
        l.append(a)
 print("The sorted list is :")
 print(l)
 gap=n//2
 while(gap>=1):
    for i in range (gap,n):
        cur=l[gap]
        j=i-gap
        if((l[j]>l[i]) and j>=0):
            l[j],l[i]=l[i],l[j]
            j=j-1
    gap=gap-1
 print(l)
def insertion_sort():
 l=[]
 n=int(input("Enter the number of items in a list :"))
 for i in range (n):
        a=int(input("Enter the values of the list :"))
        l.append(a)
 print(l)

 for i in range (1,n):
    current=l[i]
    j=i-1
    while(l[j]>current and j>=0):
       l[j],l[j+1]=l[j+1],l[j]
       j=j-1
 print("The sorted list is :")
 print(l)
while(True):
 print("press 1 : Shell sort \npress 2 : Insertion sort")
 a=int(input("Enter your choice :"))
 if(a==1):
  insertion_sort()
 if(a==2):
  shell_sort()
 if(a>=3):
     print("Your choice is wrong")
     break
