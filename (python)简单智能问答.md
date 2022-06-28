age = 18
count = 0
while count < 3:
    num = input("请输入你要猜测的数字：")
    guess = int(num)
    if guess == age:
        print("congratulations you have got thirty DoJo point!")
        break
    elif guess > age:
        print("I am so sorry that it is bigger than that")
        print("剩下的次数是"+str(2-count))
    else:
        print("I am so sorry that it is smaller than that")
        print("剩下的次数是"+str(2-count))
    count += 1

if count == 3:
    print("I am so sorry, you losse your DoJo point")