#read and count words in a file
fname = open("mithun.txt",'r')

num_words = 0
num_lines = 0
num_chars = 0
for line in fname:
    num_lines = num_lines + 1
    num_words = num_words + len(line.split())
    num_chars = num_chars + len(line)
    
print num_lines
print num_words
print num_chars
