<pre>
  
print("Укажите верхнюю границу диапазона от 1 до 100")
max_limit = str(input())
while not is_valid(max_limit):
    print("А может быть все-таки введем целое число от 1 до 100?")
    max_limit = str(input())

print(f"Укажите нижнюю границу диапазона от 1 до {max_limit}")
min_limit = str(input())
while not is_valid(min_limit) or not int(min_limit) <= int(max_limit):
    print(f"А может быть все-таки введем целое число от 1 до {max_limit}?")
    min_limit = str(input())

n = random.randint(int(min_limit), int(max_limit))

victory = False
attempts = 0
while not victory:

    print("Введите число:")
    a = str(input())
    attempts += 1

    if not is_valid(a):
        print(f"А может быть все-таки введем целое число от {min_limit} до {max_limit}?")

    elif int(a) < n:
        print("Ваше число меньше загаданного, попробуйте еще разок")

    elif int(a) > n:
        print("Ваше число больше загаданного, попробуйте еще разок")

    else:
        print(f"Вы угадали, поздравляем!\nПопыток сделано: {attempts}")
        print("Чтобы сыграть еще, напишите 1")
        if not str(input()) == '1':
            print("Спасибо, что играли в числовую угадайку. Еще увидимся...")
            new_game = False
        victory = True
      
</pre>
