#Remove invalid paranthesis:

string = "()(()"
lst = ' '.join(string).split()
lst1 = []

i= 0

while(i<len(lst)):
    if (ord(lst[i]) == 40 and ord(lst[i+1]) == 41):
        lst1.append(lst[i])
        lst1.append(lst[i+1])
        lst.remove(lst[i])
        lst.remove(lst[i])
    else:
        tmp = lst[i]
        for j in range(i+1,len(lst)):
            if (ord(lst[i]) == 40 and ord(lst[j]) == 41) or (ord(lst[i]) == 41 and ord(lst[j]) == 40):
                lst1.append(lst[i])
                lst1.append(lst[j])
                lst.remove(lst[j])
                lst.remove(lst[i])
                break
        i = i + 1

#Output:

['(', ')', '(', ')']