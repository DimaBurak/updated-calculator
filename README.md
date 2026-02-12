# updated-calculator
while True:
    try:
        a = float(input("Введите первое число: "))
        b = float(input("Введите второе число: "))
    except ValueError:
        print("Ошибка! Нужно вводить только числа.")
        continue

    op = input("Введите операцию (+, -, *, /): ")

    if op == "+":
        print("Результат:", a + b)
    elif op == "-":
        print("Результат:", a - b)
    elif op == "*":
        print("Результат:", a * b)
    elif op == "/":
        if b != 0:
            print("Результат:", a / b)
        else:
            print("На ноль делить нельзя")
    else:
        print("Неизвестная операция")

    again = input("Посчитать ещё? (да/нет): ")
    if again.lower() != "да":
        print("Калькулятор завершён.")
        break
