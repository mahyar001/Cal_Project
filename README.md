# Cal_Project
# Made By Mahyar Norouzi

class Calculator:
    def add(self, x, y):
        return x + y

    def subtract(self, x, y):
        return x - y

    def multiply(self, x, y):
        return x * y

    def divide(self, x, y):
        if y == 0:
            return "Error! Division by zero."
        else:
            return x / y


if __name__ == "__main__":
    calculator = Calculator()

    while True:
        print("\nعملیات‌های ممکن:")
        print("1. جمع")
        print("2. تفریق")
        print("3. ضرب")
        print("4. تقسیم")
        print("5. خروج")

        choice = input("لطفاً شماره عملیات مورد نظر خود را وارد کنید: ")

        if choice == '5':
            print("ماشین حساب خاتمه یافت.")
            break

        if choice in ['1', '2', '3', '4']:
            x = float(input("لطفاً عدد اول را وارد کنید: "))
            y = float(input("لطفاً عدد دوم را وارد کنید: "))

            if choice == '1':
                result = calculator.add(x, y)
                print(f"جمع: {result}")
            elif choice == '2':
                result = calculator.subtract(x, y)
                print(f"تفریق: {result}")
            elif choice == '3':
                result = calculator.multiply(x, y)
                print(f"ضرب: {result}")
            elif choice == '4':
                result = calculator.divide(x, y)
                print(f"تقسیم: {result}")
        else:
            print("ورودی نامعتبر! لطفاً شماره صحیح عملیات را وارد کنید.")
