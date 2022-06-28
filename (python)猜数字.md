from random import randint

#print(x)
print("Guess the number below 100,")
x = randint(1,99)
guess = -1
time = 0
max = 99
min = 1

setting = int(input("please set the times you want:"))
while guess != x and time < setting:
    print()
    if setting - time > 1:
        print("you have", setting - time,"times")
    else:
        print("you only have 1 time. Be careful and pay more attention.")
    guess = int(input("Guess(from " + str(min) + " to " + str(max) + "):"))
    #guess = (max + min) // 2
    #print("the number computer guesses:", guess)

    time += 1
    print('Number of attempts:' + str(time))
    if guess > x:
        print("Your guess is too big")
        max = guess
    elif guess < x:
        print("Your guess is too small")
        min = guess
    else:
        print("Guessed correctly")
if time == setting:
    print()
    print("the correct number is", x)

print("The Game End")