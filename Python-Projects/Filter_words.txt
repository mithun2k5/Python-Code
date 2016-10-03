def filter_words(word_lst,s):
    lst=word_lst.split()
    for word in lst:
        new_word = word
        length_new_word = len(word)
        for letter in new_word:
            if letter==s:
                print new_word
                break
    