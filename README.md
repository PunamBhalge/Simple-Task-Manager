import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class Task {
    private String title;
    private String description;
    private String deadline;
    private String status;

    public Task(String title, String description, String deadline, String status) {
        this.title = title;
        this.description = description;
        this.deadline = deadline;
        this.status = status;
    }

    // Getters and setters
}

public class TaskManager {
    private List<Task> tasks;
    private Scanner scanner;

    public TaskManager() {
        tasks = new ArrayList<>();
        scanner = new Scanner(System.in);
    }

    public void addTask(Task task) {
        tasks.add(task);
    }

    public void displayTasks() {
        for (Task task : tasks) {
            System.out.println(task.getTitle() + " - " + task.getDescription() + " - " +
                    task.getDeadline() + " - " + task.getStatus());
        }
    }

    // Implement other functionalities like updateTask, deleteTask, etc.

    public static void main(String[] args) {
        TaskManager taskManager = new TaskManager();
        // Example usage
        Task task1 = new Task("Complete Java assignment", "Finish coding exercises", "2024-03-15", "Pending");
        taskManager.addTask(task1);
        taskManager.displayTasks();
    }
}
