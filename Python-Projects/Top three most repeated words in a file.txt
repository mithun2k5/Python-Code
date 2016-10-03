from collections import defaultdict
dictionary = defaultdict(lambda:0)
data = open('data.txt','r')

for line in data:
    for word in line.split():
        dictionary[word] = dictionary[word] + 1

mostcommon = dictionary.items()
mostcommon = sorted(mostcommon,key = lambda value:value[1],reverse = True)

for i in range(3):
    print mostcommon[i]

