#Find K pairs with smallest sum,list will be given in ascending order

num1 = [1,7,11]
num2 = [2,4,6]

k =3

lst_sum = []
lst_pair = []
for i in range(len(num1)):
    for j in range(len(num2)):
        lst_sum.append(num1[i] + num2[j])
        lst_pair.append((num1[i],num2[j]))
print lst_sum
print lst_pair
print '\n'
for i in range(k):
    print lst_pair[i]

Output:

[3, 5, 7, 9, 11, 13, 13, 15, 17]
[(1, 2), (1, 4), (1, 6), (7, 2), (7, 4), (7, 6), (11, 2), (11, 4), (11, 6)]


(1, 2)
(1, 4)
(1, 6)