# rock-paper-scissor__game.py
  import random 

def game_win(comp,user_selection):
    if comp== user_selection:
        return None
    elif comp == 1:
        if user_selection == 3:
            return False
        elif user_selection == 2:
            return True
    elif comp == 2:
        if user_selection == 1:
            return False
        elif user_selection == 3:
            return True
    elif comp == 3:
        if user_selection == 1:
            return False
        elif user_selection == 2:
            return True

computer_selection=["rock","paper","scissors"]
randomnumber=random.randint(1,3)
if randomnumber==1:
    comp= 1
elif randomnumber==2:
    comp= 2
elif randomnumber==3:
    comp= 3
user_selection=int(input("Enter  1 for rock, 2 for paper, 3 for scissors: \n"))


a= game_win(comp,user_selection)

print("computer choice ")
if comp == 1:
    print ("\nRock")
elif comp == 2:
    print("\npaper")
else:
    print("\nscissors")
print(f"\n\nyour choice 1 for rock, 2 for paper, 3 for scissors  {user_selection}")
if a == None:
    print("\n\nthe game is tie!")
elif a== True: 
    print("\n\nyou win!")
else: 
    print("\n\nyou lose!")
