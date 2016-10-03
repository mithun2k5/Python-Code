#Range Sum Query

class NumRange(object):
    
    def __init__(self,nums):
        
        self.nums = nums
        
        
    def update(self,pos,val):
        
        self.nums[pos] = val
        
    def SumRange(self,start,end):
        
        total = 0
        
        for i in range(start,end+1):
            total = total + self.nums[i]
        return total

#Input and Output:

c = NumRange([1,3,5])

c.update(1,2)
c.SumRange(0,2)

8