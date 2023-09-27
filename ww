  def register_student():
    imya = input(" имя: ")
    familya = input(" фамилию: ")
    login = input(" логин: ")
    password = input(" пароль: ")

   
    if not is_login_unique(login):
        print("Пользователь с таким логином уже существует.")
    else:
       
        with open("students.txt", "a") as file:
            file.write(f"{imya} {familya} {login} {password}\n")
            print("Регистрация прошла успешно.")

def is_login_unique(login):
    with open("students.txt", "r") as file:
        for line in file:
            data = line.split()
            if data and data[2] == login:
                return False
    return True

def login_student():
    login = input("Введите логин: ")
    password = input("Введите пароль: ")

    with open("students.txt", "r") as file:
        for line in file:
            data = line.split()
            if data and data[2] == login and data[3] == password:
                print("Авторизация успешна.")
                return

    print("Логин или пароль неверны.")


while True:
    print("1. Регистрация")
    print("2. Авторизация")
    print("3. Выход")
    choice = input("Выберите действие (1/2/3): ")
    if choice == "1":
        register_student()
    elif choice == "2":
        login_student()
    elif choice == "3":
        break
    else:
        print("Некорректный выбор.")
