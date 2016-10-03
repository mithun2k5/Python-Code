#Bulb Switcher:

num_round = 3

num_bulb = 3
cond_bulb = []
for i in range(num_bulb):
    cond_bulb.append(False)

for i in range(num_round):
    if i == 0:
        for j in range(i,num_bulb):
            cond_bulb[j] = not(cond_bulb[j])
    else:
            cond_bulb[i] = not(cond_bulb[i])

#Output:

[True, False, False]