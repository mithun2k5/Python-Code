n = int(raw_input().strip())
for i in range (1,n+1):
    for j in range(1,n+1-i):
        print ''",
    print i*'# '
print ''

5
    # 
   # # 
  # # # 
 # # # # 
# # # # # 

n = int(raw_input().strip())
for i in range (1,n+1):
    for j in range(1,n+1-i):
        print ' ',
    print i*' #'
print ''

5
         #
       # #
     # # #
   # # # #
 # # # # #

n = int(raw_input().strip())
for i in range (1,n+1):
    print ' '*(n-i) + '#'*i

5
    #
   ##
  ###
 ####
#####

