# Projeto Todo List API

Projeto utilizando uma lista de tarefas feito com base nos ensinamentos do curso de Java da DIO em 2024. Tecnologias utilizadas no projeto:

- Spring Boot
- Java 17
- Maven
- Swagger
- Railway

# Classes
```mermaid
classDiagram
class TaskController {
+ getTask(id: Long): Task
+ createTask(task: Task): Task
+ updateTask(id: Long, task: Task): Task
+ deleteTask(id: Long): void
}

class TaskService {
+ getAllTasks(): List<Task>
+ getTaskById(id: Long): Task
+ createTask(task: Task): Task
+ updateTask(taskId: Long, task: Task): Task
+ deleteTask(taskId: Long): void
}

class Task {
- id: Long
- description: String
- completed: boolean
}

class TaskNotFoundException {
+ TaskNotFoundException(message: String)
}

TaskController --|> TaskService
TaskService --|> Task
TaskController --|> TaskNotFoundException

