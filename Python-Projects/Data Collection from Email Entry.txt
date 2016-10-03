# Data Collection from Email Entry

lst = [ [ "John", "john@gmail.com", "john@fb.com"], 
[ "Dan", "dan@gmail.com", "+1234567"], 
[ "john123", "+5412312", "john123@skype.com"], 
[ "john1985", "+5412312", "john@fb.com"] ] 

lst1 = []
for i in range(len(lst)):
    lst1.append(lst[i][0].lower())

lst2 = []
for i in range(len(lst1)):
    name = ''.join(i for i in lst1[i] if not i.isdigit())
    lst2.append(name)

lst3 = list(set(lst2))
lst4 = []

for i in range(len(lst3)):
    a= lst3[i]
    lst5 = [i for (y,i) in zip(lst2,range(len(lst2))) if a == y]
    lst4.append(lst5)

lst4

#Output:

[[1], [0, 2, 3]]