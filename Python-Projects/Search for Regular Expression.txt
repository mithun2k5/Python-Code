#Search for regular expression:
import re
import urllib

data = urllib.urlopen('mail.html')

new_lst = []
for i in data:
    new_lst.append(i)
search_term = '@'
new_lst1 = []
for i in new_lst:
    val = re.split(search_term,i)
    new_lst1.append(val[0])

import glob
for filename in glob.glob('*.txt'):
    print filename

#Output:
Animal_Name.txt
mithun.txt
New_Document.txt
pima_data.txt
Speed.txt

