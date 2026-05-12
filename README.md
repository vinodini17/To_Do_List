# Ex03 To-Do List using JavaScript
## Date: 12/05/2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

### index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>My To-Do List</h1>
        <div class="input-section">
            <input type="text" id="taskInput" placeholder="Add a new task...">
            <button id="addBtn">Add</button>
        </div>
        <ul id="taskList"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>

```

### style.css
```
body {
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #74ebd5, #acb6e5);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background-color: #ffffffcc; 
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    width: 400px;
    text-align: center;
}

h1 {
    margin-bottom: 20px;
    color: #4b0082; 
    text-shadow: 1px 1px 2px #bbb;
}

.input-section {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-bottom: 20px;
}

input[type="text"] {
    padding: 10px;
    width: 70%;
    border: 2px solid #4b0082;
    border-radius: 8px;
    font-size: 16px;
    outline: none;
    transition: 0.3s;
}

input[type="text"]:focus {
    border-color: #ff6347; 
    box-shadow: 0 0 5px #ff6347;
}

button {
    padding: 10px 15px;
    background-color: #ff6347; 
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
    transition: 0.3s;
}

button:hover {
    background-color: #ff4500; 
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: flex;
    justify-content: space-between;
    padding: 12px 15px;
    margin-bottom: 8px;
    border-radius: 8px;
    border-left: 5px solid #4b0082;
    background-color: #f9f9f9;
    transition: 0.3s;
    cursor: pointer;
}

li:hover {
    background-color: #e0f7fa;
}

li.completed {
    text-decoration: line-through;
    color: #999;
    border-left-color: #32cd32; 
    background-color: #e6ffe6;
}

.delete-btn {
    background-color: #dc3545; 
    border: none;
    padding: 5px 10px;
    color: white;
    border-radius: 5px;
    cursor: pointer;
    transition: 0.3s;
}

.delete-btn:hover {
    background-color: #a71d2a;
}

#status {
    margin-top: 15px;
    font-weight: bold;
    color: #4b0082;
}


```
### script.js
```
const taskInput = document.getElementById('taskInput');
const addBtn = document.getElementById('addBtn');
const taskList = document.getElementById('taskList');

function addTask() {
    const taskText = taskInput.value.trim();
    if (taskText === "") {
        alert("Please enter a task!");
        return;
    }

    const li = document.createElement('li');
    li.textContent = taskText;

    li.addEventListener('click', () => {
        li.classList.toggle('completed');
    });

    const deleteBtn = document.createElement('button');
    deleteBtn.textContent = 'Delete';
    deleteBtn.className = 'delete-btn';
    deleteBtn.addEventListener('click', (e) => {
        e.stopPropagation(); 
        li.remove();
    });

    li.appendChild(deleteBtn);
    taskList.appendChild(li);

    taskInput.value = '';
}
addBtn.addEventListener('click', addTask);

taskInput.addEventListener('keypress', (e) => {
    if (e.key === 'Enter') {
        addTask();
    }
});

```
## OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d3b19289-f5d0-4128-80c9-2d5c4c743e3e" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
