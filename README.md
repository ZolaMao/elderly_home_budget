# elderly_home_budget
# Инициализация словаря с бюджетом дома престарелых
elderly_home_budget = {
    "food": 1000,
    "staff_salaries": 5000,
    "medical_supplies": 2000,
    "maintenance": 1500
}

# Функция для вывода текущего состояния бюджета
def print_budget(budget):
    print("Current Budget:")
    for category, amount in budget.items():
        print(f"{category}: ${amount}")

# Функция для добавления расходов в определенную категорию бюджета
def add_expense(budget, category, amount):
    if category in budget:
        budget[category] -= amount
    else:
        print("Invalid category")

# Функция для добавления доходов в бюджет
def add_income(budget, amount):
    budget["income"] = budget.get("income", 0) + amount

# Вывод текущего состояния бюджета
print_budget(elderly_home_budget)

# Добавление расходов на медицинские расходы
add_expense(elderly_home_budget, "medical_supplies", 500)

# Добавление доходов
add_income(elderly_home_budget, 3000)

# Вывод обновленного состояния бюджета
print_budget(elderly_home_budget)
