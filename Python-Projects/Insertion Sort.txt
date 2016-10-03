num = input()

arr = [int(i) for i in raw_input().strip().split()]

target = arr.pop()
if arr[num-2] > target:
    arr.append(arr[num-2])
    print ' '.join(map(str,arr))

    i = 0
    num = num - 1
    while(i<=num-2):
        if arr[num-2] > target:
            arr[num-1] = arr[num-2]
            print ' '.join(map(str,arr))
        else:
            arr[num-1] = target
            print ' '.join(map(str,arr))
            break
        num = num -1
    else:
        arr[num-1] = target
        print ' '.join(map(str,arr))
        
else:
    arr.append(target)
    print ' '.join(map(str,arr))

#Output

5
2 4 6 8 3
2 4 6 8 8
2 4 6 6 8
2 4 4 6 8
2 3 4 6 8