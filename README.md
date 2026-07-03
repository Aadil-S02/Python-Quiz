# Python-Quiz

# Here is my code

# This part is a module which I call into the main code

import random 

def get_question():
    questions = [("What is the name of the best lecturer?", "Katia Punter"),
                 ("What is the name of the best course?", "Intensive Foundations of Computer Science & Programming"),
                 ("What is the best Programming Language?", "Python"),
                 ("What is the best university?", "Northeastern University London"),
                 ("What mark will this formative get?", "100 (hopefully😅)"),
                 ("Which team is the best at football?", "Liverpool FC"),
                 ("Is this quiz enjoyable?", "Yes"),
                 ("What is the best laptop?", "Macbook")]
    return random.choice(questions)


# This is my main code

from random_question import get_question

print("Hello, welcome to the Opiniated Quiz - where the questions may seem like opinions but the answers are all facts!")
u_name = input ("Before we begin, what is your name?")
print("Great! Let's get started " + u_name)

score = 0

for i in range (3):
    q = get_question()
    ans = input (q[0])
    if ans == q[1]:
        print ("Amazing! That was correct 🎉🎉🎉")
        score = score + 1
    else:
        print ("Incorrect 😢, the right answer is: " + q[1])

print ("You scored " + str(score) + " points") 

if score == 3:
    print ("Congratulations!!! You have done a brilliant job! Here is your medal 🥇")
elif score == 2:
    print ("Good job! You were unlucky to get 1 wrong - but here is a medal for you 🥈")
elif score == 1:
    print ("Good try! Better luck next time. Here is a medal for you 🥉")
else:
    print ("You need some practice! Maybe you'll get a medal next time 🙂")

print ("Thank you for playing " + u_name + "! Hope to see you again soon 😃")
