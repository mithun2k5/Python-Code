#Twitter Design:

class Twitter(object):
    
    def __init__(self):
        self.tweet = {}
        
    def postTweet(self,userid,tweet):
        if userid not in self.tweet:
            self.tweet[userid] = []
            self.tweet[userid].insert(0,tweet)
        else:
            self.tweet[userid].insert(0,tweet)
        
    def getNewsFeed(self,userid):
            return self.tweet[userid]
        
    def follow(self,followerid,followeeid):
        for i in self.tweet[followeeid][::-1]:
            self.tweet[followerid].insert(0,i)
    
    def unfollow(self,followerid,followeeid):
        for i in self.tweet[followeeid]:
            self.tweet[followerid].remove(i)

Input and Output:

t = Twitter()
t.postTweet(2,20)
t.postTweet(2,25)
t.follow(1,2)

t.getNewsFeed(1)
[25, 20, 15, 10]

t.unfollow(1,2)

t.getNewsFeed(1)
[15,10]
