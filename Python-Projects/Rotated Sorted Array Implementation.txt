#rotated sorted array:

lst = [1,2,3,4,5,0]
###wiggle sort:
for i in range(1,len(lst)-1):
    if lst[i]>lst[i-1] and lst[i]>lst[i+1]:
        val = i
        break
else:
    val = 0
    
left = lst[:val+1]
right = lst[val+1:]
sorted_lst = right + left