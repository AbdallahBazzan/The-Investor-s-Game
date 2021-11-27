# The-Investor-s-Game
Text Adventure Game using Python
# import numpy for list sum function in playerScore
import numpy as np
#importing random
import random
#Defining the investors game function
#including docstring

def investors_game():
    """
    This function defines the game. This game is based on a fiction story that is based upon real life situations.
    Throughout the game, you will pass through 4 different stages of decision making. 
    Your decision making is based on what you value the most. 
    You accumulate a prize at the start of the game and decide what to do with it later on.
    Your investment and lovescore is calculated at each stage. They could help you make the better decision. 
    This game is for educational and entertainment purposes.
    This game is not based on a movie or story. It is from the creation of my own mind. 
    """
    #printing the introduction
    
    print(f"""
Welcome to the Investor's Game. This game is based on a fiction story that is based upon real life situations.
You are in the quest for achieving success in your life through making investment decisions.
You are great at your work as an employee and you always think if you're going to be able to open your own business.
You are currently engaged and you are living in Miami,FL with your family. 
You value Wealth and Love the most.
You will start the game accumulating a big prize!
        """)
    #input any key to start the game
    input(prompt="<Press Any Key to Start>: ")
    
    #input your name to start playing
    name = input(prompt = "<Enter your name to collect your prize> : ")
    
    #printing the first part of the game's story 
    print(f"""\nCongratulations {name}, you just won the Mega Millions Lottery 2nd prize for 1 million dollars.\n
After you went home, your mother congratulates you saying that you can finally buy your dream house.
Your father advices you to be smart and responsible with this blessing. 
Your brother is the happiest man on earth, now that you can get the brand new Lamborghini Hurracan 2021.
Your fiance is joyful as she mentions that you can now get her that wedding dress with the diamond necklace and earings.
You are overwhelmed and happy being the first millionaire in your family!
    """)
    
#defining player's choice function needed to use in main function 
#conditional statement for each stage-decision, iDecision is the index number of each of the 4 stages: 0,1,2,3
def playerChoice(iDecision):
    
    #this is the docstring for this function
    """This function includes is used to help the user make choice at each stage. It has the different choices needed 
    to be taken at each stage. It includes 4 stages along with their conditional statements for each stage index."""
    
    #First conditional statement for input stage 1
    #putting randomization in the game at the first stage 
    #the first stage always give 3 random possibilities out of the 7 choices
    if iDecision == 0:
        choice1= "Buying your dream house in the Miami Beach for $500,000"
        choice2= "Buying a dream house in the mountains in Boulder, Colorado for 500,000"
        choice3= "Buying a dream house in New York for $500,000"
        choice4= "Opening a new business Resto-pub in Miami embracing hardships  for $500,000"
        choice5= "Opening a new business in Miami embracing the hardships for $500,000"
        choice6= "Living the life by buying the brand new 40ft Meridian yacht for $500,000"
        choice7= "Buying a brand new Bugatti Veyron car 2022 for $500,000"
        random_choices_1= [choice1,choice2,choice3]
        random_choices_2= [choice4,choice5]
        random_choices_3= [choice6,choice7]
        randInt1          = random.randint(0,len(random_choices_1)-1)
        randInt2          = random.randint(0,len(random_choices_2)-1)
        randInt3          = random.randint(0,len(random_choices_3)-1)
        
        #printing the text needed to prompt for first stage
        print(f"""\nYou are thinking about what to do with your money , but the first decision is not yours in this game.
Your investment decisions will start taking action after the first decision that is taken randomly. This is for 
entertainment purposes that you will not have control over the first $500,000.
Four weeks have already passed and you're now making the decision for:\n
1){random_choices_1[randInt1]}             
2){random_choices_2[randInt2]}
3){random_choices_3[randInt3]}""")
        
    #Second conditional statement for input stage 2
    elif iDecision == 1:
        print(f"""\nYou are the happiest as you are living the best time of your life. You are living your dreams.
After 2 weeks, your brother takes you to show you the brand new Lamborghini Huracan. You're amazed by its yellow color. 
You test drive it and you're convinced this is the best car. You were also thinking about other plans...
You're about to:
1) Buy the brand new Lamborghini Huracan for $200,000
2) Invest the $200,000 in cryptocurrencies 
        """)
        
    #Third conditional statement for input stage 3
    elif iDecision == 2:
        print(f"""\nWhile you are thinking about what to do next, you are now planning for your marriage.
Its Friday night and you're out with your fiance enjoying dinner as she is too excited for your
upcoming marriage. She mentions that marriage only happens once in your life and she wants it to be the best.
Later during the day, she was with the wedding planner in the Four Seasons Miami Beach Hotel discussing the decorations.
She tells you the marriage will only cost 200,000$ since it is all about luxury.
Her diamond necklace, earings and ring will cost $75000 only. Her wedding dress along with the best make-up artist in 
town will cost $25000. So the wedding along with everything would only cost you $300,000.
You're now a millionaire, and she expects to have the best night of her life. 
However, you were thinking about other plans for the future. 
You then decide to:\n
1)Live the best night of your life and do the marriage for $300000 
2)Negotiate the wedding,diamonds and dress for $200,000
3)Invest $300,000 in the Stock Market and break up with your fiance because she is making you nervous
        """)
        
    #Fourth conditional statement for input stage 4
    elif iDecision == 3: 
        print(f"""\nYou are now at the end of your decisions. Your decision is based on the current economy. 
A housing deppression might start according to CNBC.Also, the competitive industry have made it hard for the progress of
any business. You want to escape and live freely. You are thinking of traveling around the world for the next 10 years
with your partner to enjoy every moment of your life. You are also thinking about the future of your childrens'
education and wellbeing. You come to a point that you can no longer wait and want to take a decision.\n
1) Travel around the world for the next 10 years for $100,000
2) Buy gold for 10% of your original account which is for $100,000
        """)
        
#defining output function needed to use in for loop in the main function
#this function includes both variables
def decisionOutput(iDecision,choice):

    #output stage 1
    if iDecision == 0:
        if isinstance(choice,str):
            if "house" in choice or "dream" in choice:
                choice = 1
            elif "business" in choice or "hardships" in choice or "new" in choice:
                choice = 2
            elif "yacht" in choice or "car" in choice or "buying" in choice:
                choice =3
       #first conditional statement stage 1
        if choice == 1:
            print("""\nCongratulations on buying your dream house, it is a good decision that you bought your home 
especially that you are about to get married. You are a safe smart investor.
            """)
        #second conditional statement stage 1
        elif choice == 2:
            print("""\nCongratulations on taking the harder decisions. Its going to be a tough road, but with hardwork
and dedication towards making the business succeed, you made the best investment decision. Remember to always 
perform your best and keep the business going regardless of the obstacles you might face.""")
        #third conditional statement stage 1
        elif choice ==3:
            print("""\nCongratulations on choosing to live the good life. Enjoy your time now as you live your life with
no regrets. You are doubtful of your decision as you are thinking that this might not be the best decision
for you. Be aware! WINTER IS COMING!!!""")
        
            
    #output stage 2
    elif iDecision == 1:
        if isinstance(choice,str):
            if "lamborghini" in choice or "Huracan" in choice or "brand new" in choice:
                choice = 1
            elif "invest" in choice or "cryptocurrencies" in choice:
                choice = 2
                
        #first conditional statement stage 2
        if choice == 1: 
            print("""\nCongratulations on buying the brand New Lamborghini Huracan. You should enjoy every moment and 
embrace the future. Drive safely and embrace what is coming!""")
        #second conditional statement stage 2
        elif choice == 2: 
            print("""\nCongratulations on being patient with your possessions. You should work hard in order to have a
good investment. Cryptocurrencies is a risky huge market and a great place to invest and learn.""")
    #output stage 3
    #first conditional statement stage 3
    elif iDecision == 2:
        if isinstance(choice,str):
            if "best night" in choice or "marriage" in choice:
                choice = 1
            elif "negotiate" in choice or "200000" in choice:
                choice = 2
            elif "stock market" in choice or "break up" in choice:
                choice =3
        if choice == 1:
            print("""\nGoodluck next time. This was indeed a risky decision. You lost all of your original money.
Your father adviced you to be responsible with your money. Eventhough you have your home or business, and you are
married. However, you have failed to accumulate and multiply your wealth which is too important for you.
Hope you enjoyed playing!""")
        #second conditional statement stage 3
        elif choice == 2:
            print("""\nCongratuations on dealing with this issue the best. You are best having a beautiful wedding
and a happy marriage and leaving some money for future investments and decisions.""")
        #third conditional statement stage 3
        elif choice == 3: 
            print("""\nGoodluck next time. This decision cost you what you value the most: Love! Even though you also
value wealth;however, you were incapable of staying with the love of your life. This stage of the game is an
exaggerated money wise event which might happen with anyone through their life. Hope you enjoyed playing!""")

    #output stage 4
    elif iDecision == 3:
        if isinstance(choice,str):
            if "travel" in choice or "10 years" in choice:
                choice = 1
            elif "gold" in choice or "buy" in choice or "10%" in choice:
                choice = 2
        #first conditional statement of stage 4
        if choice == 1: 
            print("""\nGoodluck next time. You have failed to maintain all of your money and you value wealth the most.
Even though traveling is a wonderful life decision, but not in this case since it was better buying gold and 
staying safe for what the future holds.Although you had a good score from previous decisions, but it was necessary 
to invest in  gold to save money for the future... Hope you enjoyed the game!""")
        #second conditional statement of stage 4
        elif choice == 2:
            print("""\nYou chose the best decision for this stage. Owning gold is the safest investment
to make,and it is necessary for future's uncertainties. It is good in the face of inflation and it saves your
money safely.""")

#defining the input for the try except clause to be used for the user's input
def input_tryexcept(iDecision,nChoices):
    """This function is mainly used for the try/except clause. It is used to handle the code 
    not to break if the user enters a string or anything else than in integer."""
    #changing the input into integer for the loop to work in this function          
    choice = input(prompt = " What do you decide to do? ")

    #The try except clause is used to handle the code from breaking
    #nChoices is a list defined later, I used it to avoid invalid user input (integers greater than number of choices)
    #for example integer 4 or 5 or 1999...
    #listing keywords for allowed strings in input
    keywords = ["house","dream","business","hardships","car","yacht","new","lamborghini","invest","cryptocurrencies",
               "invest","best night", "marriage", "negotiate", "$200000", "stock market", "break up", "travel", 
               "10 years", "gold", "buy", "10%"]
    try: 
        choice= int(choice)
        if choice > nChoices[iDecision]:
            print(" Invalid entry, please try again.")
    except:
        if choice.lower() not in keywords:
            print(" Invalid entry, please try again.")
            choice = False
    return choice
            
#defining playerDecision function including the index of stage(iDecision) and playerscore and savings
def playerDecision(iDecision,nChoices,playerScore,savings):
    
    #docstring for playerDecision function
    """This function includes the indices of each stage decision, the player score and the savings for each stage
    It has in it the input of player's choice of decision."""
    
    #input of choice of player for each stage
    #defining input function for try and except clause to try the code and keep it working
    #the code was able to handle strings or any input by using not isinstance meaning not integer
    #when entering  number greater than our number of choices, e.g. 4, 5 ..or 3 in the cases where there is 2 choices.
    choice = input_tryexcept(iDecision,nChoices)
    while choice == False:
        choice = input_tryexcept(iDecision,nChoices)
    if isinstance(choice,str):
        choice.lower()
    decisionOutput(iDecision,choice)    
        
    #output stage 1
    if iDecision == 0:
        #savings for stage 1
        savings = savings - 500000                  
        if choice == 1: #first conditional statemento sum the new player score
                        #the player score in the list = [investmentScore,loveScore]
            playerScore = playerScore + [25,25]
        elif choice == 2: #second conditional statement
            playerScore = playerScore + [25,25]
        else: #third conditional statement
            playerScore = playerScore + [0,0]

    #output stage 2
    elif iDecision == 1:
        #savings for stage 2
        savings = savings - 200000
        if choice == 1: #first conditional statement to sum the new player score
                        #the player score in the list = [investmentScore,loveScore]
            playerScore = playerScore + [0,0]
        elif choice == 2: #second conditional statement
            playerScore = playerScore + [25,25]
    #output stage 3
    elif iDecision == 2:
        if choice == 1: #first conditional statement with playerscore and savings
            playerScore = playerScore + [0,25]
            savings = savings - 300000
        elif choice == 2: #second conditional statement with playscore and savings
            playerScore = playerScore + [25,25]
            savings = savings - 200000
        else: #third conditional statement with playscore and savings
            playerScore = playerScore + [25,0]
            savings = savings - 300000
    #output stage 4
    elif iDecision == 3:
        #savings for stage 4 which should be equal to 0
        savings = savings - 100000
        if choice == 1: 
            playerScore = playerScore

        elif choice == 2: #second conditional statement
            playerScore = playerScore + [25,0]
    
    #returning investment score and player score from playerScore
    investmentScore = playerScore[0]
    loveScore = playerScore[1]
    
    #printing the results after each stage.
    print(f"""\nThis is your new player score! It adds up after each decision if you earned points.
It includes both your investment score and your love score.
Your investment score is {investmentScore}/100 and your love score is {loveScore}/100.
Your savings so far is ${savings}""")
    
    return [playerScore,savings]
        
def gameEnding(playerScore,savings):
#This is the docstring for gameEnding function
    """This function is used for ending the game which includes and prints the player score at the end along with 
    the savings at the end."""

    investmentScore = playerScore[0]
    loveScore = playerScore[1]
    
    #setting conditional statements for winning and losing
    #the winner should have a value > 75 for investment score and a value >=75 in love score
    if investmentScore> 75 and loveScore >= 75:
        print(f"""\nCongratulations you've survived the whole game and played well. Your decisions took into account
your valuation of wealth and love. You are in investment expert and a good lover. 
Your investment score is {investmentScore} and your love score is {loveScore}.
You Won!""")
    #if the user had less than 75 in investment score and less in love score he loses
    elif investmentScore <= 75 and loveScore <=50:
        print("""\nYou Lost!You have survived to the last level. However, your decisions weren't taking into 
        consideration both wealth and love. You had a bad score...Goodluck next time...""")
    #else cause to losing case
    else:
        print("""\nYou Lost! Goodluck next time...""")

#Insert playGame variable to allow user to play investor's game multiple times
#setting the variable equals True to stay doing it when user inputs [y] to play again
playGame = True        
while playGame:
  
    #Running the investor's game function
    investors_game()        

    #Setting variables to use in collecting savings
    savings = 1e06

    #The player's score is both the investment's score and the love Score
    #This game includes decisions relative to the player's valuation of Love and Wealth
    investmentScore = 0
    loveScore = 0
    playerScore = np.array([investmentScore,loveScore])

    #defining the list being used with the indexes which are the 4 stages of decision in the game
    #index 0 is for stage 1, index 1 for stage 2 ...
    list = [0,1,2,3]
    #defining the list corresponding to the number of choices at each stage of decision in the game
    #to avoid invalid user input (integers greater than number of choices)
    nChoices = [3,2,3,2]

    #setting for loop in list of stages 
    #setting while loop as long as it is above $0 which the player can still continue to play and not fail.    
    for iDecision in list:
        if savings > 0:

            #this is the user input function which is used to describe the different choices at each stage
            playerChoice(iDecision)

            #defining the variables to be concluded from the main function playerDecision.
            #the function includes the indices of decisions, the playerscore and the savings at each stage
            [playerScore,savings] = playerDecision(iDecision,nChoices,playerScore,savings)

    #this is the function used to end the game when it finishes along with playscore and savings
    gameEnding(playerScore,savings)
    
    #input prompt to play again and the input should be [y] to play
    #any other input will stop the game from playing again
    play_again = input(prompt = "\nIf you don't like your scores and want to play again, press [y], if not, press any key.\n")
    
    #conditional statements for play_again variable defining them True or False
    if play_again == "y":
        playGame = True
    else:
        playGame = False
        print("\nThank you for playing! Hope you enjoyed.") 
