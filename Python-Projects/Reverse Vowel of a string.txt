#Reverse Vowel of a string:
string = 'hello'
string = ' '.join(string.lower())
string_lst = string.split()
lst_vow = []
lst_index = []
for i in range(len(string_lst)):
    if string_lst[i] in ['a','e','i','o','u']:
        lst_vow.append(string_lst[i])
        lst_index.append(i)
lst_vow = lst_vow[::-1]
for i in range(len(lst_index)):
    string_lst[lst_index[i]] = lst_vow[i]
string_lst = ''.join(string_lst)
string_lst

Output
'holle'