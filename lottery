import random

print(
    "Welcome to lottery program. Write 6 numbers between 0 and 50. If you hit least 2 of them you'll win!!"
)
print("(Hint: There are no repeating numbers on a lucky ticket...)")
userTicket = []
luckyTicket = []


def generateManually():
    i = 0
    while i < 6:
        i += 1
        taken_num = int(input("Enter your lucky number: "))
        if taken_num < 0 or taken_num > 50:
            i -= 1
            print("Between 0 and 50!!!")
        else:
            userTicket.append(taken_num)
    print("Your ticket is: \n", userTicket)


def contains(luckyTicket, target):
    for i in range(len(luckyTicket)):
        if luckyTicket[i] == target:
            return True


def generateRandomly():
    for i in range(6):
        random_number = random.randint(0, 51)
        result = contains(luckyTicket, random_number)
        if result:
            i -= 1
        else:
            luckyTicket.append(random_number)
    print("The lucky ticket is: \n", luckyTicket)


def hit_numbers(luckyTicket, userTicket):
    hit = 0
    for i in range(len(luckyTicket)):
        if contains(userTicket, luckyTicket[i]):
            hit += 1
    return hit


generateManually()
generateRandomly()
total_hit = hit_numbers(luckyTicket, userTicket)
if total_hit >= 2:
    print(f"Congratulations! You hit {total_hit} numbers and won!!!")
else:
    print(f"Sorry, you hit {total_hit} and lost...")
