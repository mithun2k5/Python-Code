lst = [2,3,4,5,6]

def can_partitions(lst):
    lst1 = []
    lst2 = []
    if sum(lst)%2 != 0:
        return False
    else:
        
        lst.sort()
        length = len(lst)
        for i in range(length):
            lst1.append(lst.pop())
            if sum(lst1) == sum(lst):
                for i in range(len(lst)):
                    lst2.append(lst.pop())
                return lst1,lst2
            elif sum(lst1) > sum(lst):
                lst.insert(0,lst1.pop())
                
        return False