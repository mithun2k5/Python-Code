#Right Circular rotation:

n = raw_input('').strip()
new = map(int,n.split())
matrix = raw_input()
new_mat = map(int,matrix.split())
k = new[1]
if k>new[0]:
    k = k%new[0]
k = new[0] - k
right = new_mat[k::]
left = new_mat[:k:]
new_mat1 =  right + left

m = []
for i in range(new[2]):
    m.append(input())

for j in m:
    print new_mat1[j]

#Output:

3 2 3
1 2 3
0
1
2
2
3
1