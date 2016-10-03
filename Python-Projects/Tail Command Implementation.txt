def tail(num=3):
    file1 = open('New_Document.txt','r')
    lst = []
    num_line = 0
    for line in file1:
        lst.append(line)
        num_line = num_line + 1
    max_num = num_line

    while(num_line-num != max_num):
        print lst[num_line-num]
        num_line = num_line + 1