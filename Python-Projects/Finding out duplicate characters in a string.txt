#Finding out duplicate characters in a string:

string = raw_input('Give your string: ')

unique_set = list(set(string))

unique_string = ''".join(unique_set)

print unique_string

for i in unique_string:
    count = 0
    for j in string:
        
        if i == j:
            count = count + 1
    print '%s : %s' %(i,count)


Give your string: mithunmithun
ihmnut
i : 2
h : 2
m : 2
n : 2
u : 2
t : 2