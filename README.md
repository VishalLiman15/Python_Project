# Python_Project

# Number Guessing Game

import random    # Importing Random Module

def guess():                          # Defining Function For Guessing Number
    print("*****  Number Guessing Game  *****\n")
    print("1.User Have 6 Chances\n2.Please Enter Number Only\n3.Choose Number From 1 To 50\n")
    
    random_number=random.randint(1,50)    # Generating Random Number
    
    guesses=0
    max_guess=6                            # User Will Have 6 Chances To Win The Game
    
    user = input("Enter Your Name : ")
    
    while guesses<max_guess:
        
        n=int(input("Choose The Number :"))        # Taking User Input
        
        if n>random_number:
            print("Please Enter Lower Number....\n")
            guesses+=1
        elif n<random_number:
            print("Please Enter Bigger Number....\n")
            guesses+=1
        else:
            print(f"{user} Wins...With {guesses} Guessess\n")
            break                                   # Break The Loop If Answer Is Correct
            
    if guesses==max_guess:
        print(f"{user} Losses...With {max_guess} Guessess\n")
        

Output :- 

guess()

*****  Number Guessing Game  *****

1.User Have 6 Chances
2.Please Enter Number Only
3.Choose Number From 1 To 50

Enter Your Name : Vishal
Choose The Number :40
Please Enter Lower Number....

Choose The Number :30
Please Enter Bigger Number....

Choose The Number :35
Please Enter Lower Number....

Choose The Number :33
Please Enter Lower Number....

Choose The Number :32
Vishal Wins...With 4 Guessess	
