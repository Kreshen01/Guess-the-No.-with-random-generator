import random
Number=random.randint(1,1000)
print("\033[36m""GUESS THE NUMBER""\033[0m")
print("")
count=0
while True:
  print("Pick a number between 0 and 1000")
  Guess=int(input(">"))
  if Guess < 0:
    print("You have to pick a number between 0 and 1000. Minus numbers are not allowed")
    exit()
  if Guess > 1000:
    print("Numbers over 1000 are not allowed")
    continue
  if Guess<Number:
    print("\033[31m""Too low","\033[0m")
    count+=1
  elif Guess>Number:
    print("\033[34m","Too high","\033[0m")
    count=count+1
  elif Guess==Number:
    print("\033[32m","You got it","\033[0m")
    count+=1 
  if Guess==Number:
    print("You got it in", count, "tries.Thanks for playing")
    exit()
