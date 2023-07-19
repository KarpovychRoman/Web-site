<!DOCTYPE html>
<html>
<head>
    <title>Сервіс ветеринарної клінікі</title>
</head>
<body>
    <h1>Сервіс ветеринарної клініки</h1>
    
    <form id="addPetForm">
        <h2>Додати нового улюбленця</h2>
        <label for="name">Ім'я:</label>
        <input type="text" id="name" required>
        <br>
        <label for="species">Вид:</label>
        <input type="text" id="species" required>
        <br>
        <label for="age">Вік:</label>
        <input type="number" id="age" required>
        <br>
        <button type="submit">Додати</button>
    </form>
    
    <h2>Список улюбленців</h2>
    <ul id="petList"></ul>
    
    <script>
        document.getElementById("addPetForm").addEventListener("submit", function(event) {
            event.preventDefault();
            
            // Отримуємо значення полів форми
            var name = document.getElementById("name").value;
            var species = document.getElementById("species").value;
            var age = document.getElementById("age").value;
            
            // Створюємо новий елемент списку
            var newPet = document.createElement("li");
            newPet.textContent = "Ім'я: " + name + ", Вид: " + species + ", Вік: " + age;
            
            // Додаємо нового улюбленця до списку
            document.getElementById("petList").appendChild(newPet);
            
            // Очищаємо поля форми
            document.getElementById("name").value = "";
            document.getElementById("species").value = "";
            document.getElementById("age").value = "";
        });
    </script>
</body>
</html>
