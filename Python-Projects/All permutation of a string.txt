#All permutation of a string:

def all_perms(str1):
    if len(str1) <=1:
        yield str1
    else:
        for perm in all_perms(str1[1:]):
            for i in range(len(perm)+1):
                #nb str[0:1] works in both string and list contexts
                yield perm[:i] + str1[0:1] + perm[i:]
                
all_perms('xyz')

Output:

for i in all_perms('xyz'):
    print i