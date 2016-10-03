#Commnon letter is there or not between two words:
def common_words():
    word1 = 'mithun'
    word2 = 'abcd'

    lst_word1 = ' '.join(word1).split()
    lst_word2 = ' '.join(word2).split()

    for i in range(len(lst_word1)):
        for j in range(len(lst_word2)):
            if lst_word1[i] == lst_word2[j]:
                return 'There are common words'
    else:
        return 'There are no common words'

#Output:

'There are no common words'