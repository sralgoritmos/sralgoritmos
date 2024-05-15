def is_repunit(n):
    digit = n % 10
    while n > 0:
        if n % 10!= digit:
            return False
        n = n // 10
    return True

def is_square(n):
    root = int(n ** 0.5)
    return root * root == n

num = int(input("Enter a number: "))
if is_repunit(num):
    print("The number is a Repunit")
    digit_sum = sum(int(digit) for digit in str(num))
    if is_square(digit_sum):
        print("The sum of its digits is a square")
    else:
        print("The sum of its digits is not a square")
else:
    print("The number is not a Repunit")
