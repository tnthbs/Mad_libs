# Mad_libs
#!python 3
import sys,os,re

def replace(strs,keyword,repl):
    """subsition '' or keyword """
    import re
    newstrRegex = re.compile(keyword)
    newstr = newstrRegex.sub(repl,strs,1)
    return newstr

#filePath = input('please enter the original file path [c:\documents]')
#To Do import the path
fileName = input('please enter the file name [instance.txt]')
mabFile = open(fileName) 
content = mabFile.read()
print(content)
#get the new words
newAdj = input('Enter an adjective: '+ '\n')
newNoun1 = input('Enter an noun: '+ '\n')
newVerb = input('Enter an verb: '+ '\n')
newNoun2 = input('Enter an noun: '+ '\n')
    
#replace 
content = replace(content,'ADJECTIVE',newAdj)
content = replace(content,'NOUN',newNoun1)
content = replace(content,'VERB',newVerb)
content = replace(content,'NOUN',newNoun2)
print(content)
mabFile.close()
#write content
newFile = open('newFile.txt','w')
newFile.write(content)
newFile.close()

#save 
