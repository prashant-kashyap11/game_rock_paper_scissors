# game_rock_paper_scissors
import random
choices = ["rock","paper","scissor"]
computer= random.choice(choices)
player= False
comp_score= 0
player_score=0
while True:
    player=input("Rock,Paper or Scissors?").capitalize()
    if player==computer:
        print("Tie!")
    elif player=="paper":
        if computer=="scissors":
            print("you lose!",computer,"cut",player)
            comp_score += 1
        else :
            print("you win!",player,"covers",computer)
            player_score += 1
    elif player=="rock":
        if computer=="paper":
            print("you lose!",computer,"covers",player)
            comp_score += 1
        else :
            print("you win!",player,"smashes",computer)
            player_score += 1
    elif player=="scissors":
        if computer=="rock":
            print("you lose!",computer,"smashes",player)
            comp_score += 1
        else :
            print("you win!",player,"cut",computer)
            player_score += 1
    elif player =='End':
        print("Final Scores:")
        print(f"computer Total score is: {comp_score}")
        print(f"your Total score is:{player_score}")
        break
