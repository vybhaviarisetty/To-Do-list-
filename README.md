# To-Do-list-
<!DOCTYPE html>
<html>
<head>
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>To-Do List</h1>
  <input type="text" id="taskInput" placeholder="Add a task..." />
  <button onclick="addTask()">Add</button>
  <ul id="taskList"></ul>
  <script src="script.js"></script>
</body>
</html>
body {
  font-family: sans-serif;
  text-align: center;
  background-color: #f0f0f0;
}

input, button {
  padding: 10px;
  margin: 10px;
}
function addTask() {
  const input = document.getElementById('taskInput');
  const task = input.value;
  if (task === "") return;
  const li = document.createElement('li');
  li.textContent = task;
  document.getElementById('taskList').appendChild(li);
  input.value = "";
}
