import random

game_over = False
score = 0

while not game_over:
    print("You are in a dark room.")
    print("There is a door in front of you.")
    print("Door options:")
    print("A) Open door")
    print("B) Check door for traps")
    print("C) Ignore door and search room")

    choice = input("Enter your choice: ")

    if choice.lower() == "a":
        print("You open the door and find yourself in a long hallway.")
        print("The hallway has doors on either side of you, and there is an exit sign at the far end.")
        print("Do you:")
        print("A) Go through the door on the left")
        print("B) Go through the door on the right")
        print("C) Head towards the exit sign")
        next_choice = input("Enter your choice: ")
        if next_choice.lower() == "a":
            print("You go through the door on the left and find a room with a treasure chest.")
            print("Inside the chest, you find a key that fits perfectly in your hand.")
            score += 1
            print(f"Your current score is {score}")
            continue
        elif next_choice.lower() == "b":
            print("You go through the door on the right and find a room filled with spikes.")
            print("You take damage and lose 2 points from your score.")
            score -= 2
            print(f"Your current score is {score}")
            continue
        else:
            print("You head towards the exit sign and leave the building.")
            game_over = True
    elif choice.lower() == "b":
        print("You check the door for traps and find a hidden mechanism.")
        print("You disarm the mechanism and gain 3 points.")
        score += 3
        print(f"Your current score is {score}")
        continue
    else:
        print("You ignore the door and search the room instead.")
        print("You find a small item that might be useful later.")
        continue

if game_over:
    print("Congratulations, you have completed the game! Your final score is", score)
else:
    print("Game over! You did not complete the game.")

