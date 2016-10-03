str1 = raw_input('').strip()
alphabet = "abcdefghijklmnopqrstuvwxyz" 
alphabet = set(alphabet)
str1_alphabet = set(str1.lower().replace(" ",""))
if str1_alphabet == alphabet:
    print 'pangram'
else:
    print 'not pangram'

#Output:

We promptly judged antique ivory buckles for the next prize
pangram