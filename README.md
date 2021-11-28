# поработать с переменными
a = 10
b = 20
value = a + b

print(value)

# запросить у пользователя несколькл чисел и строк
age = int(input("Укажите свой возраст"))

if age >= 18:
    print('совершеннолетний')
else:
    print("несовершеннолетний")

name = input("Укажите имя")

print("Привет", name)

# преобразовать время в секундах в формат чч:мм:сс
seconds = int(input("Время в секундах "))
hours = seconds // 3600
seconds %= 3600
minutes = seconds // 60
seconds %= 60

print("%02d:%02d:%02d" % (hours, minutes, seconds))

# вывести сумму n + nn + nnn
n = int(input("Введите число - "))
sum_n = (n + int(str(n) + str(n)) + int(str(n) + str(n)+ str(n)))
print("Сумма чисел n + nn + nnn - %d" % sum_n)

# найти максимальную цифру в целом положительном числе
n = int(input("Введите целое положительное число"))
max_numb = n % 10
while n >= 1:
    n = n // 10
    if n % 10 > max_numb:
     max_numb  = n % 10
    if n > 9:
       continue
    else:

        print("Максимальное цифра в числе ", max_numb)

        break

# запросить у пользователя значение выручки и издержек
profit = int(input("Введите выручку фирмы "))
costs = int(input("Введите издержки фирмы "))
if profit > costs:
    print(f"Фирма показывает прибыль. Рентабельность составляет {profit / costs}")
    staff = int(input("Введите количество сотрудников"))
    print(f"прибыль в расчете на одного сторудника сотавила {profit / staff}")
elif profit == costs:

    print('Фирма работает без прибыли')
else:

    print("Фирма работает в убыток")

# посчитать через сколько дней бегун достигнет цели, если будет бегать каждый день и каждый следующий день
# удлиннять дистанцию на 10% (0,1) от предыдущего дня
a = int(input("Введите результат первой пробежки в км "))
b = int(input("Введите цель пробежки в км "))
days = 1
km = a
while km < b:
    a = a + a * 0.1
    days = days + 1
    km = km + a
print(f"Вы достигнете цели на %.d день" % km)




