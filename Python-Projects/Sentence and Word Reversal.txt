#Sentence reversal
#First Method::
string = raw_input("Give string input:: ")
reversed_string = string[::-1]
print "\n"
print "Reversed string is::",reversed_string


Give string input:: mithun talukder


Reversed string is:: redkulat nuhtim


#Sentence reversal
#Second Method:
string = raw_input("Give string input:: ")
reversed_string = "".join(reversed(string))
print "\n"
print "Reversed string is::",reversed_string

Give string input:: mithun talukder


Reversed string is:: redkulat nuhtim

#Word reversal
#First Method:
string = raw_input("Give string input:: ")
reversed_word = " ".join(reversed(string.split()))
print "\n"
print "Reversed words is::",reversed_word

Give string input:: mithun talukder


Reversed words is:: talukder mithun

#Word reversal
#First Method:
string = raw_input("Give string input:: ")
reversed_word = " ".join(reversed(string.split()))
print "\n"
print "Reversed words is::",reversed_word

Give string input:: mithun talukder


Reversed words is:: talukder mithun


#Word reversal
#Second Method:
string = raw_input("Give string input:: ")
reversed_word = " ".join(string.split()[::-1])
print "\n"
print "Reversed words is::",reversed_word

Give string input:: mithun talukder


Reversed words is:: talukder mithun



