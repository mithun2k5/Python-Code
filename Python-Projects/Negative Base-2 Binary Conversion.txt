def neg_base2_binary(dec_num):
    lst = []
    while (dec_num != 0):
        x = dec_num % -2 
        dec_num = (dec_num/-2)
        if x < 0:
            lst.append(str(x+2))
            dec_num = dec_num + 1 
        else:
            lst.append(str(x))
    lst1 = lst[::-1]
    string = "".join(lst1)
    print string

#Output:

neg_base2_binary(34)
1100110