age = 18
count = 0
while count < 3:
    num = input("��������Ҫ�²�����֣�")
    guess = int(num)
    if guess == age:
        print("congratulations you have got thirty DoJo point!")
        break
    elif guess > age:
        print("I am so sorry that it is bigger than that")
        print("ʣ�µĴ�����"+str(2-count))
    else:
        print("I am so sorry that it is smaller than that")
        print("ʣ�µĴ�����"+str(2-count))
    count += 1

if count == 3:
    print("I am so sorry, you losse your DoJo point")