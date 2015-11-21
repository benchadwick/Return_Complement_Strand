# Return_Complement_Strand
This python script accepts a single string as input and will return the complementary DNA sequence.

##########
##Script##
##########

#/usr/bin/env python
import re
input=raw_input("Please enter your DNA sequence.\n")
incaps=input.replace('a', 'A').replace('t', 'T').replace('g', 'G').replace('c',
'C')
if re.search("^[ATGC]+$", incaps):
print "your input sequence is", (incaps)
temp=incaps.replace('A', 'W').replace('T', 'X').replace('G', 'Y').replace('C',
'Z')
output=temp.replace('W', 'T').replace('X', 'A').replace('Y', 'C').replace('Z',
'G')
print "your output sequence is", (output)
else:
print "It appears you have entered characters other then A,T,G,C. Perhaps your
sequence is RNA or you might just be a dismal failure"
