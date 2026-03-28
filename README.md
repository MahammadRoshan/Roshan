# Roshan
<!DOCTYPE html>
<html lang="en">
<head>
    <title>To-Do App</title>

    <style>
        body {
            font-family: Arial;
            background: #f2f2f2;
            text-align: center;
        }

        .container {
            background: white;
            padding: 20px;
            margin: 100px auto;
            width: 300px;
            border-radius: 10px;
        }

        input {
            padding: 10px;
            width: 70%;
        }

        button {
            padding: 10px;
            background: green;
            color: white;
            border: none;
        }

        li {
            margin-top: 10px;
            list-style: none;
            background: #eee;
            padding: 10px;
            cursor: pointer;
        }
    </style>

</head>
<body>

<div class="container">
    <h1>My To-Do List</h1>

    <input type="text" id="taskInput" placeholder="Enter a task">
    <button onclick="addTask()">Add</button>

    <ul id="taskList"></ul>
</div>

<script>
    function addTask() {
        let input = document.getElementById("taskInput");
        let task = input.value;

        if (task === "") {
            alert("Enter a task!");
            return;
        }

        let li = document.createElement("li");
        li.textContent = task;

        // Click to remove task
        li.onclick = function () {
            li.remove();
        };

        document.getElementById("taskList").appendChild(li);
        input.value = "";
    }
</script>

</body>
</html>
