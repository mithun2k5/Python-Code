#clean bad word:

string = 'This is a crap Who does this shit'
def filter_word(string):
    bad_word = ['crap','shit','stupid']
    lst_str = string.split()
    for i in range(len(bad_word)):
        for j in range(len(lst_str)):
            if lst_str[j] == bad_word[i]:
                lst_str[j] = 'BAD_WORD'
    string = ' '.join(lst_str)
    return string

#Output
filter_word(string)
'This is a BAD_WORD Who does this BAD_WORD'