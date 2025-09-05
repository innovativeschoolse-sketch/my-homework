<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>مذكّري - واجباتي</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      direction: rtl;
      text-align: right;
      background: #f9f9f9;
      margin: 20px;
    }
    h1 {
      color: #4CAF50;
    }
    #taskInput {
      padding: 8px;
      width: 60%;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    #addBtn {
      padding: 8px 12px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      background: white;
      margin: 5px 0;
      padding: 10px;
      border-radius: 5px;
      box-shadow: 0 0 5px #ccc;
    }
  </style>
</head>
<body>
  <h1>📚 مذكّري - واجباتي</h1>
  <input type="text" id="taskInput" placeholder="أدخل واجبك هنا">
  <button id="addBtn">➕ إضافة</button>
  <ul id="taskList"></ul>

  <script>
    const input = document.getElementById("taskInput");
    const addBtn = document.getElementById("addBtn");
    const taskList = document.getElementById("taskList");

    addBtn.addEventListener("click", () => {
      const task = input.value.trim();
      if (task) {
        const li = document.createElement("li");
        li.textContent = task;
        taskList.appendChild(li);
        input.value = "";
      }
    });
  </script>
</body>
</html>
