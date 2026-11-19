from time import sleep

General = {} 

def show_task_topics():
    if General == {}:
        print("There is no topic\nPlease Enter topic first")
    else:
        for key, value in General.items():
            print(f"{key}: {'\n'.join(map(str, value))}\n")
    sleep(3)


def add_task_topic():
    
    while True:
        topic_name = input("Please Enter the topic: ")
        if topic_name in General.keys():
            print("This topic already existn")
        else: 
            break

    topic_list = []
    General[topic_name] = topic_list
    topic_answer = input("Do you want to add tasks? (Yes/No)\n")
    topic_answer.lower()
    
    if topic_answer == "yes" or topic_answer == "y":
        print("\nwhen you have entered all the tasks please type done")
        print(f"{topic_name}'s tasks:")
        while True: 
            task = input()
            if task.lower() == "done":
                break
            topic_list.append(task)

    print("\nComplete ...")
    sleep(1)        


def delete_task_topic():
    
    while True: 
        d_task_name = input("Please Enter the task you want to delete:\n")
        if d_task_name not in General:
            print("this topic does not exist")
        else:
            break
    
    answer = input(f"Are you sure about deleting {d_task_name}'s tasks? (yes/no)\n")
    if answer.lower() == "yes" or answer.lower() == "y":
        del General[d_task_name]

    print("\nComplete ...")
    sleep(1)


def edit_an_existing_topic():

    while True: 
        answer1 = input("Please Enter the task you want to edit:\n")
        if answer1 not in General:
            print("this topic does not exist")
        else:
            break
    
    while True: 
        new_name = input("Please enter new topic:\n")
        if new_name in General:
            print("this topic Already exist")
        else:
            break
    
    value = General[answer1]
    del General[answer1]
    General[new_name] = value

    print("\nComplete ...")
    sleep(1)


def add_new_task():
    
    while True: 
        in_topic = input("Please Enter the topic you want to submit the task to:\n")
        if in_topic not in General:
            print("this topic does not exist")
        else:
            break
    
    print("\nwhen you have entered all the tasks please type done")
    print(f"{in_topic}'s tasks:")
    while True: 
        new_task = input()
        if new_task.lower() == "done":
            break
        General[in_topic].append(new_task)

    print("\nComplete ...")
    sleep(1)


def delete_completed_task():
    
    while True: 
        tpc = input("Please Enter the topic you want to delete task from:\n")
        if tpc not in General:
            print("this topic does not exist")
        else:
            break

    print(f"{tpc}'s tasks:")
    for index, item in enumerate(General[tpc], 1):
        print(f"{index}. {item}")

    print("Please enter the number of tasks you want to delete:")
    print("and type done when you enter all numbers")
    while True:
        num_del = input()
        if num_del.lower() == "done":
            break
        elif int(num_del) < 1 or int(num_del) > len(General[tpc]):
            print("invalid number !!")
        else:
            del General[tpc][int(num_del) - 1]

    print("\nComplete ...")
    sleep(1)


def main():
    
    while True:
        
        print("\n __ to-do list menu __")
        print("1. show task topics")
        print("2. add task topic")
        print("3. delete task topic")
        print("4. Edit an existing topic")
        print("5. add new task")
        print("6. delete completed task")
        print("7. Exit\n")
        
        answer = input()
        answer == answer.lower()
        
        if answer == "1" or answer == "show task topics":
            show_task_topics()

        elif answer == "2" or answer == "add task topic":
            add_task_topic()
            
        elif answer == "3" or answer == "delete task topic":
            delete_task_topic()

        elif answer == "4" or answer == "edit an existing topic":
            edit_an_existing_topic()
 
        elif answer == "5" or answer == "add new task":
            add_new_task()

        elif answer == "6" or answer == "delete completed task":
            delete_completed_task()
        
        elif answer == "7" or answer == "exit":
            break
        
        else:
            print("invalid choice !!\n")    


main()
