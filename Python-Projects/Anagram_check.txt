#Method 1
def is_anagram(s1,s2):
    s1 = s1.replace(' ','').lower()
    s2 = s2.replace(' ','').lower()
    return sorted(s1) == sorted(s2)

#Method 2

def is_anagram2(s1,s2):
    s1.replace(' ','').lower()
    s2.replace(' ','').lower()

    count={}
    
    if len(s1) != len(s2):
        return False
    
    for item in s1:
        if item in count:
            count[item] = count[item] + 1
        else:
            count[item] = 1
            
    for item in s2:
        if item in count:
            count[item] = count[item] -1
        else:
            count[item] =1
            
    for k in count:
        if count[k] != 0:
            return False
        
    return True

#Output:

is_anagram('rose','Eros')
True