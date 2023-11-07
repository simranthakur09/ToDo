# <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>simran thakur</title>
    <style>


body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    
   
}

.left-pane {
    width: 40%;
    border-right: 1px solid #ccc;
    color: black;
    padding: 20px;
    background-color: #ccc;
    max-height: 300px;
    overflow-y: auto; 
    font-size: 20px;
}

.right-pane {
    display: flex;
    width: 40%;
    padding: 20px;
    border: 1px solid white;
    
    width: 40%;
   
    
}

.task {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding: 10px;
    border-bottom: 1px solid #ccc;
}

.completed {
    text-decoration: line-through;
    opacity: 0.5;
}

button {
    padding: 5px 10px;
    margin: 0 5px;
    cursor: pointer;
}

button.complete-btn {
    background-color: black;
    color: #fff;
    border: none;
}

button.delete-btn {
    background-color: black;
    color: white;
    border: none;
}
#task-input{
    border: 1px solid white;
    height: 50px;
    width:300px;
    font-size: 30px;
}
h1{
    font-size: 30px;
}

    </style>
</head>
<body>
    <div class="left-pane">
        <h1>Simran Thakur TASK LIST</h1>
    </div>
    <div class="right-pane">
        
        <form id="task-form">
            <input type="text" id="task-input" placeholder="I Need to DO........"><br><br>
            <button type="submit">Add Task</button>
        </form>
        
    </div>

    <script > document.getElementById('task-form').addEventListener('submit', function(event) {
        event.preventDefault();
   document.getElementById('task-form').addEventListener('submit', function(event) {
       event.preventDefault();
   
       var taskInput = document.getElementById('task-input').value;
   
   
   });
   
       var taskInput = document.getElementById('task-input').value;
   
       //  ^  Create a new task element
       var taskElement = document.createElement('div');
       taskElement.classList.add('task');
       taskElement.innerHTML = `
           <span>${taskInput}</span>
           <input type="checkbox" class="complete-btn">
           <button class="delete-btn">X</button>
       `;
   
       document.querySelector('.left-pane').appendChild(taskElement);
   
    
       document.getElementById('task-input').value = '';
   
       taskElement.querySelector('.complete-btn').addEventListener('click', function() {
           taskElement.classList.toggle('completed');
       });
   
       taskElement.querySelector('.delete-btn').addEventListener('click', function() {
           taskElement.remove();
       });
   });
   </script>
    
</body>
</html>
