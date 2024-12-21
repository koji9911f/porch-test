<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Porsche UI</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        .car-section {
            padding: 20px;
            text-align: center;
        }
        .car-image {
            width: 100%;
            max-width: 400px;
            margin: auto;
            display: block;
            border-radius: 8px;
        }
        .car-details {
            margin-top: 20px;
        }
        .car-details h2 {
            margin: 10px 0;
        }
        .car-details p {
            margin: 5px 0;
            color: #555;
        }
        .color-options {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        .color-options button {
            width: 40px;
            height: 40px;
            margin: 0 5px;
            border: none;
            border-radius: 50%;
            cursor: pointer;
        }
        .color-options button.shark-blue { background-color: #0073e6; }
        .color-options button.agate-grey { background-color: #6e6e6e; }
        .color-options button.carmine-red { background-color: #a50000; }
        .color-options button.racing-yellow { background-color: #ffd700; }
        .color-options button.crayon { background-color: #d9d9d9; }
        .color-options button.guards-red { background-color: #ff0000; }
    </style>
</head>
<body>
    <div class="container">
        <div class="car-section">
            <img src="shark-blue.jpg" alt="Porsche 911 Carrera" class="car-image" id="carImage">
            <div class="car-details" id="carDetails">
                <h2>911 Carrera</h2>
                <p><strong>Top Speed:</strong> 182 mph</p>
                <p><strong>Power (PS):</strong> 385 PS</p>
                <p><strong>Max Torque:</strong> 450 Nm</p>
                <p><strong>Displacement:</strong> 2,981 cm³</p>
            </div>
            <div class="color-options">
                <button class="shark-blue" onclick="changeCar('shark-blue.jpg', 'Shark Blue')"></button>
                <button class="agate-grey" onclick="changeCar('agate-grey.jpg', 'Agate Grey')"></button>
                <button class="carmine-red" onclick="changeCar('carmine-red.jpg', 'Carmine Red')"></button>
                <button class="racing-yellow" onclick="changeCar('racing-yellow.jpg', 'Racing Yellow')"></button>
                <button class="crayon" onclick="changeCar('crayon.jpg', 'Crayon')"></button>
                <button class="guards-red" onclick="changeCar('guards-red.jpg', 'Guards Red')"></button>
            </div>
        </div>
    </div>
    <script>
        function changeCar(image, colorName) {
            const carImage = document.getElementById('carImage');
            const carDetails = document.getElementById('carDetails');

            carImage.style.opacity = 0;

            setTimeout(() => {
                carImage.src = image;
                carImage.alt = `Porsche 911 Carrera in ${colorName}`;
                carDetails.querySelector('h2').textContent = `911 Carrera (${colorName})`;
                carImage.style.opacity = 1;
            }, 500);
        }
    </script>
</body>
</html>

