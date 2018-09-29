# PoetryRemix
The code for our poetry remix project. 

import random 
from textblob import TextBlob

#Grabbing the file called "Rick.txt"
#Having a collection of varried text

with open ('Rick.txt', 'r') as file:
    text = file.read()

#Allowing textblob to store 2 empty list
#creating a text that uses adjectives and nouns and forming them into a list

blob = TextBlob(text)
adjectives = []
nouns = []
for word,pos in blob.tags:
    if (pos == 'JJ'):
        adjectives.append(word)
    if (pos == 'NN'):
        nouns.append(word)
        
   #gernerating a random list that prints out an output from the text file
   #containing both adjectives and nouns 

for i in range(12):
    a = random.choice(adjectives)
    n = random.choice(nouns)
    print(a,n)
