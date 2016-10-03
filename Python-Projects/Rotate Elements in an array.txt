lst = raw_input("Enter array with space:: ")
lst = map(int,lst.split())

k = int(raw_input("Give input of k:: "))
length = len(lst)
for j in range(k):
    i = length
    temp = lst[length - 1]
    while(i>= 0):
        if i == 0:
            lst[i] = temp
        else:
            lst[i-1] = lst[i-2]
        i = i - 1
lst

#Output:
Enter array with space:: 1
Give input of k:: 5
Out[3]:
[1]