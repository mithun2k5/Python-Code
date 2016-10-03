#Time Conversion:

time = raw_input().strip()
if time[8] == 'P':
    new_time = time[0:8]
    new_time1 = new_time.split(':')
    if new_time1[0] == '12':
        new_time2 = int(new_time1[0])
    else:
        new_time2 = int(new_time1[0]) + 12
    print str(new_time2) +':'+ str(new_time1[1]) + ':' + str(new_time1[2])

else:
    new_time = time[0:8]
    new_time1 = new_time.split(':')
    if int(new_time1[0]) == 12:
        new_time1[0] = '00'
    print str(new_time1[0]) +':'+ str(new_time1[1]) + ':' + str(new_time1[2])
    
Output:
12:45:54PM
12:45:54
