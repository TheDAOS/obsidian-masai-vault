```html
<!-- L2 - Advanced Task Manager with Event Delegation and Filtering -->

<!DOCTYPE html>

<html lang="en">

  

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Q15</title>

<style>

  

body {

font-family: 'Courier New', Courier, monospace;

background-color: black;

color: white;

}

  

#container {

padding: 10px;

display: flex;

flex-direction: column;

background-color: lightcoral;

padding: 10px;

border-radius: 10px;

width: 400px;

margin: auto;

}

  

#container * {

margin: 0;

margin-bottom: 5px;

}

  

#container > div {

display: flex;

justify-content: center;

}

  

#container:last-child {

margin-bottom: 20px;

}

  

button, input {

border: 0;

padding: 8px;

margin: 0px 10px;

border-radius: 10px;

background-color: whitesmoke;

}

  

li {

margin-top: 10px;

}

</style>

</head>

  

<body>

<div id="container">

<input type="text" name="inputTask" id="inputTask" placeholder="Enter Task Here">

<button type="button" id="addTask">Add Task</button>

<button type="button" id="allTasks">All Tasks</button>

<button type="button" id="completedTasks">Completed Tasks</button>

<button type="button" id="incompleteTasks">Incomplete Tasks</button>

<div id="countAll"></div>

<div id="countCompleted"></div>

<div id="countIncomplete"></div>

  

<ul id="tasks">

</ul>

</div>

  

<script>

// let tasksList = [];

const addTask = document.getElementById('addTask');

const tasksList = document.getElementById('tasks');

  

const countAll = document.getElementById('countAll');

const countCompleted = document.getElementById('countCompleted');

const countIncomplete = document.getElementById('countIncomplete');

  
  

function updateCounts() {

const tasks = tasksList.querySelectorAll('li');

const totalTasks = tasks.length;

let completedTasks = 0;

let incompleteTasks = 0;

  

tasks.forEach((task) => {

if (task.style.textDecoration === "line-through") {

completedTasks++;

} else {

incompleteTasks++;

}

});

  

countAll.innerText = `All Tasks: ${totalTasks}`;

countCompleted.innerText = `Completed Tasks: ${completedTasks}`;

countIncomplete.innerText = `Incomplete Tasks: ${incompleteTasks}`;

}

  
  

document.getElementById('allTasks').addEventListener('click', () => {

const tasks = tasksList.querySelectorAll('li');

tasks.forEach((task) => {

task.style.display = 'list-item';

});

})

  

document.getElementById('incompleteTasks').addEventListener('click', () => {

const tasks = tasksList.querySelectorAll('li');

tasks.forEach((task) => {

if (task.style.textDecoration !== "line-through") {

task.style.display = 'list-item';

} else {

task.style.display = 'none';

}

});

})

  

document.getElementById('completedTasks').addEventListener('click', () => {

const tasks = tasksList.querySelectorAll('li');

tasks.forEach((task) => {

if (task.style.textDecoration === "line-through") {

task.style.display = 'list-item';

} else {

task.style.display = 'none';

}

});

})

  
  

addTask.addEventListener('click', () => {

const taskInput = document.getElementById('inputTask').value;

  

const task = document.createElement('li');

  

const completeButton = document.createElement('button');

completeButton.innerText = "Completed";

completeButton.addEventListener('click', () => {

if (task.style.textDecoration === "line-through") {

task.style.textDecoration = "none";

} else {

task.style.textDecoration = "line-through";

}

});

  

const deleteButton = document.createElement('button');

deleteButton.innerText = "Delete";

deleteButton.addEventListener('click', () => {

tasksList.removeChild(task);

});

  

task.innerText = taskInput;

task.append(completeButton);

task.append(deleteButton);

tasksList.appendChild(task);

  

updateCounts();

});

</script>

</body>

  

</html>
```