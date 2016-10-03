#Word Pattern

pattern = 'aaaa'
string = 'fish cat cat cat'
lst_pattern = list(pattern)
lst_string = string.split()
new_lst2 = []
new_lst1 = []
i = 1
count = 1
if len(set(lst_pattern)) == len(set(lst_string)):

    while (i<len(lst_pattern)):
        if lst_pattern[i] == lst_pattern[i-1]:
            count = count + 1
        else:
            new_lst1.append(count)
            count = 1
            i = i + 1
    new_lst1.append(count) 

    i = 1
    count = 1
    while (i<len(lst_string)):
        if lst_string[i] == lst_string[i-1]:
            count = count + 1
        else:
            new_lst2.append(count)
            count = 1
        i = i + 1
    new_lst2.append(count) 

    if new_lst1 == new_lst2:
        print 'TRUE'
    else:
        print 'FALSE'
else:
    print 'FALSE'

#Output
FALSE