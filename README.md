# Basic-java-application-
New repo
import java.util.ArrayList;
import java.util.Scanner;
public class TaskListApp {
public static void main(String[] args) {
TaskList taskList = new TaskList();
Scanner scanner = new Scanner(Sys tem.in);
while (true) {
display Menu();
int choice = getUserChoice (scann
er);
switch (choice) {
case 1:
taskList.addTask(getTaskN
ame(scanner));
break;
case 2:
if (!taskList.isEmpty()) {
taskList.listTasks();
int taskNumber = getUser Input (scanner, "Enter the task number to remove: ");
if (taskList.is Valid TaskN
umber(taskNumber)) {
taskList.removeTask(taskNumber);
} else {
System.out.println("In
valid task number.");
}
} else {
System.out.println("No tasks to remove.");
}
break;
case 3:
if (!taskList.isEmpty()) {
taskList.listTasks();
} else {
System.out.println("No tasks to list.");
}
break;
case 4:
scanner.close();
return;
default:
System.out.println("Invalid option. Please try again.");
}
}
}
private static void display Menu() {
System.out.println("Task List Applic ation");
System.out.println("1. Add Task");
System.out.println("2. Remove Task
System.out.println("3. List Tasks");
System.out.println("4. Quit");
System.out.print("Select an option:
");
");
}
private static int getUserChoice (Scann er scanner) {
return scanner.nextInt()
