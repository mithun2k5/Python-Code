#Palindrome Pairs:

words = ['bat','tab','cat']
lst = []

for i in range (len(words)):
    new_words = words[i]
    for j in range (len(words)):
        if new_words != words[j]:
            join_words = new_words + words[j]
            if join_words == join_words[::-1]:
                lst.append([i,j])
lst

#Output:

[[0, 1], [1, 0]]