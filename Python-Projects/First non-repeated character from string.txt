#First non-repeated character from string:
from collections import OrderedDict
string = 'mthunmm'

dictionary = OrderedDict()

for i in string:
    if i not in dictionary:
        dictionary[i] = 1
    else:
        dictionary[i] = dictionary[i] + 1

for i in dictionary.keys():
    if dictionary[i] == 1:
        print i
        break

Output:
t