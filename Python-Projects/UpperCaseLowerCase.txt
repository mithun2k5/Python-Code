def up_low(s):
    count_is_upper = 0
    count_is_lower = 0
    s = s.replace(" ","").replace("?","").replace(",","").replace(".","")
    for letter in s:
        if letter.isupper():
            count_is_upper = count_is_upper + 1
        else:
            count_is_lower = count_is_lower + 1
    print "Number of Upper case letter is::%s"%count_is_upper
    print "NUmber of Lower case letter is::%s"%count_is_lower