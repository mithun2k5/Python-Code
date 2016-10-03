str1 = 'AABBCCDDEEFFGFZZZZZZ'
lst1 = [word for word in str1]
i = 0 
while (i<len(lst1)-1):
    if lst1[i] != lst1[i+1]:
        (x,y) = (lst1[i],lst1[i+1])
        print (x,y)
        lst1.remove(lst1[i])
        lst1.remove(lst1[i])
        i = 0
    else:
        i = i + 1

#Result:
('A', 'B')
('A', 'B')
('C', 'D')
('C', 'D')
('E', 'F')
('E', 'F')
('G', 'F')