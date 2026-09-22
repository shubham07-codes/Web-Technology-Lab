# Practical No. 4B

---

## Aim

To study and implement JavaScript DOM Manipulation.

---

## Problem Definition

Build a To-Do List web application where users can add tasks, delete tasks, and mark tasks as complete using vanilla JavaScript DOM methods only.

---

## Theory

JavaScript DOM Manipulation is used to access and modify HTML elements dynamically. DOM stands for Document Object Model. It represents the web page as a collection of objects that JavaScript can control. Using DOM methods such as `getElementById()`, `createElement()`, `appendChild()`, and `remove()`, we can add, change, or delete elements from a webpage. In a To-Do List application, DOM manipulation is used to create new tasks, mark tasks as completed, and remove tasks. Event handling is also used to perform actions when the user clicks buttons. Thus, DOM manipulation makes webpages interactive and responsive.

---

## Procedure and Execution

### Step for Implementation

1. Create an HTML page with a heading for the To-Do List.
2. Add an input box where the user can enter a task.
3. Add an Add Task button.
4. Create an empty list using the `<ul>` element.
5. Use `getElementById()` to access the input box and list.
6. Use `createElement()` to create a new task.
7. Add Complete and Delete buttons for every task.
8. Use `appendChild()` to add tasks to the list.
9. Use JavaScript events to mark tasks as completed.
10. Use the `remove()` method to delete tasks.
11. Use `classList.toggle()` to apply completed styling.
12. Run the webpage in a browser and test all operations.

---

# Code

## HTML File - `index.html`

```html
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">

    <title>To-Do List</title>


    <style>

        body {

            font-family: Arial;

            text-align: center;
        }


        input {

            padding: 8px;
        }


        button {

            padding: 8px;

            margin: 5px;
        }


        li {

            margin: 10px;
        }


        .completed {

            text-decoration: line-through;
        }

    </style>

</head>


<body>


    <h2>To-Do List</h2>


    <input
        type="text"
        id="taskInput"
        placeholder="Enter a task"
    >


    <button onclick="addTask()">

        Add Task

    </button>


    <ul id="taskList"></ul>


    <script>


        function addTask() {


            let input =
                document.getElementById("taskInput");


            let task =
                input.value.trim();


            if (task == "") {

                alert("Please enter a task.");

                return;
            }


            let li =
                document.createElement("li");


            let taskText =
                document.createElement("span");


            taskText.innerHTML = task;


            let completeButton =
                document.createElement("button");


            completeButton.innerHTML =
                "Complete";


            completeButton.onclick = function() {

                taskText.classList.toggle("completed");

            };


            let deleteButton =
                document.createElement("button");


            deleteButton.innerHTML =
                "Delete";


            deleteButton.onclick = function() {

                li.remove();

            };


            li.appendChild(taskText);

            li.appendChild(completeButton);

            li.appendChild(deleteButton);


            document
                .getElementById("taskList")
                .appendChild(li);


            input.value = "";

        }


    </script>


</body>

</html>
```

---

## Important DOM Methods Used

### `getElementById()`

It is used to access an HTML element using its ID.

```javascript
let input = document.getElementById("taskInput");
```

### `createElement()`

It is used to create a new HTML element dynamically.

```javascript
let li = document.createElement("li");
```

### `appendChild()`

It is used to add a newly created element inside another HTML element.

```javascript
li.appendChild(taskText);
```

### `classList.toggle()`

It is used to add or remove the completed class.

```javascript
taskText.classList.toggle("completed");
```

### `remove()`

It is used to remove a task from the webpage.

```javascript
li.remove();
```

---

## Output Analysis

The output displays a simple To-Do List application with an input field and an Add Task button. The user can enter a task and click the button to add it to the list. Every task contains Complete and Delete buttons. When the Complete button is clicked, a line appears through the task, indicating that the task has been completed. When the Delete button is clicked, the selected task is removed from the list. If the user tries to add an empty task, an alert message is displayed. Thus, JavaScript DOM methods dynamically control the webpage.

---

## Conclusion

In this practical, I learned about JavaScript DOM manipulation and event handling. I learned how to access HTML elements and dynamically create, modify, and remove elements using JavaScript. Methods such as `getElementById()`, `createElement()`, `appendChild()`, `remove()`, and `classList.toggle()` were used in the To-Do List application. The application allows users to add new tasks, mark completed tasks, and delete unnecessary tasks without refreshing the webpage. This practical helped me understand how DOM manipulation is used to create interactive and dynamic web applications.
