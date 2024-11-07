import random
import time as t

record = []

def checker():
    # guessloop
        ranguess = random.choice(questions)
        if ranguess not in record:
                guess1 = input(ranguess)
                
                # index
                index = [i for i,question in enumerate(questions) if question == ranguess]
                answer = answers[index[0]]
                checkguess(guess1, answer)
                record.append(ranguess)
        else:
            checker()
        
            
        record.append(ranguess)
# checkguess
def checkguess(guess, answer):
    global score
    if guess.lower() == answer.lower():
        print('Correct!')
        score = score + 1
    else:
        print('Oh dear! Incorrect!')
        score = score - 1
# question list
questions = ['What is the name for a fast-flowing mudflow caused by volcanic ash mixing with rainwater? ', 'What is the maximum recorded speed for Pyroclastic flows? ', 'What is the volcanic gas responsible for global cooling? ', 
             'What is the most reactive gas released by volcanic eruptions? ', 'What gas is released in the largest quantity during volcanic eruptions? '
             ]
# answer list
answers = ['Lahar', '700kmph', 'sulphur dioxide', 'Flourine', 'Water vapour', ]
# record
record = []
# start
score = 0
print('Let\'s revise!')
print('Just type the right answer to incease your score! If you want to stop, just type yes at the prompt')
stop = input('Stop? ')
while stop != 'yes':
    print('Okay! Let\'s go!')
    t.sleep(1)
    for counter in range(0,4):
        checker()
        print('Your score is', str(score))
        t.sleep(1)
    if score < 0:
        print('Oh no! you ran out of lives! \n Bye!')
        t.sleep(2)
        exit()
    stop = input('Stop? ')
    
else:
    print('Thanks for playing!')
    t.sleep(2)
    exit()
