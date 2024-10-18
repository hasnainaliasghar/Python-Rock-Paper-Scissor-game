import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

list = [rock,paper,scissors]
turn = random.randint(0,2)

#user game
print("Enter 1 for rock, 2 for paper, 3 for Scissors")
user_turn = int(input(""))
if user_turn == 1:
    print(f"Your Choice\n Rock\n{rock}")
elif user_turn == 2:
    print(f"Your Choice\n paper\n{paper}")
else:
    print(f"Your Choice\n scissors \n{scissors}")
#computer's game
print("computer Chooses:\n")
if turn == 0:
    print(f"rock\n{rock}")
elif turn == 1:
    print(f"paper\n{paper}")
else:
    print(f"scissors\n{scissors}")

#logic to win game
if turn == user_turn-1:
    print("It's a Draw")
elif turn == 0 and user_turn == 2:
    print("You win")
elif turn == 0 and user_turn ==3:
    print("You loose")
elif turn == 1 and user_turn == 1:
    print("You loose")
elif turn == 1 and user_turn == 3:
    print("You win")
elif turn == 2 and user_turn == 1:
    print("You win")
else:
    print("You loose")
