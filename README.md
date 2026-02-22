# CODESOFT
#"codesoft python programming intership task"
##to_do list application
tasks = []

def show_menu():
    print("\n--- TO-DO LIST MENU ---")
    print("1. View Tasks")
    print("2. delete Task")
    print("3. update Task")
    print("4. Exit")

while True:
    show_menu()
    choice = input("Choose an option (1-4): ")

    if choice == '1':
        if not tasks:
            print("\nYour list is empty.")
        else:
            print("\nYOUR TASKS:")
            for index, task in enumerate(tasks, start=1):
                print(f"{index}. {task}")

    elif choice == '2':
        new_task = input("Enter the task: ")
        tasks.append(new_task)
        print("Task added!")

    elif choice == '3':
        if tasks:
            try:
                task_num = int(input("Enter task number to update: "))
                if 1 <= task_num <= len(tasks):
                    update = tasks.pop(task_num - 1)
                    print(f"update: {update}")
                else:
                    print("Invalid number.")
            except ValueError:
                print("Please enter a valid number.")
        else:
            print("Nothing to update.")

    elif choice == '4':
        print("Goodbye!")
        break

    else:
        print("Invalid choice, try again.")
