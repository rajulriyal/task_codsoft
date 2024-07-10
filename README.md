# task_codsoft
tasks=[]

def addTask():
    task = input ("Please Enter a task :")
    tasks.append(task)
    print(f"Task '{task}' added to the list .")  
    
def listTasks():
    if not tasks:
        print("There are no tasks currently .")
    else:
        print("Current Tasks:")
        for index,task in enumerate(tasks):
            print(f"Task #{index}.{task}")      
def deleteTask():
    listTasks()
    try:
        taskToDelete = int (input ("Enter  the #  to delete :"))
        if taskToDelete >=0 and taskToDelete < len(tasks):
            tasks.pop(taskToDelete)
            print(f"Task {taskToDelete} has been removed.")
        else:
            print(f"Task #{taskToDelete} was not found .")
    except:
        print("Invalid input .")    

if __name__==  "__main__":
    print("************** To DO List *****************")
    while True:
        print("\n")
        print("PLease select one of the following option.")
        print("****************************************")
        print("1.Add a new task")
        print("2.Delete a task")
        print("3.List tasks")
        print("4.Exit")
        choice= input("Enter your choice :")
        
        if(choice=="1"):
            addTask()
        elif(choice =="2"):
            deleteTask()
        elif(choice =="3"):
            listTasks()
        elif(choice=="4"):
            break
        else:
            print("Invalid input .Please try again .")
