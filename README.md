# Bmi-calculator-

this is my first project 
<br>
-by uday


Js 



function calculateBMI() {
    var height = parseFloat(document.getElementById('height').value);
    var weight = parseFloat(document.getElementById('weight').value);

    var bmi = weight / ((height / 100) ** 2);
    var category;

    if (bmi < 18.5) {
        category = 'Underweight';
    } else if (bmi < 25) {
        category = 'Normal weight';
    } else if (bmi < 30) {
        category = 'Overweight';
    } else {
        category = 'Obese';
    }

    document.getElementById('result').innerHTML = '<h2>Your BMI: ' + bmi.toFixed(2) + '</h2><p>You are ' + category + '</p>';

    displayDietPlan(category);
}

function displayDietPlan(category) {
    var dietTable = document.getElementById('diet-table');
    dietTable.innerHTML = ''; // Clear existing table content

    var dietPlan = [];

    switch (category) {
        case 'Underweight':
            dietPlan.push({ meal: 'Breakfast', timing: '7:00 AM', details: 'Oatmeal with fruits and nuts', calories: '400' });
            dietPlan.push({ meal: 'Morning Snack', timing: '10:00 AM', details: 'Greek yogurt with honey', calories: '200' });
            dietPlan.push({ meal: 'Lunch', timing: '1:00 PM', details: 'Grilled chicken salad', calories: '600' });
            dietPlan.push({ meal: 'Afternoon Snack', timing: '4:00 PM', details: 'Mixed nuts and fruits', calories: '200' });
            dietPlan.push({ meal: 'Dinner', timing: '7:00 PM', details: 'Salmon with quinoa and steamed vegetables', calories: '500' });
            break;
        case 'Normal weight':
            dietPlan.push({ meal: 'Breakfast', timing: '7:00 AM', details: 'Whole grain toast with avocado and eggs', calories: '400' });
            dietPlan.push({ meal: 'Morning Snack', timing: '10:00 AM', details: 'Apple slices with peanut butter', calories: '200' });
            dietPlan.push({ meal: 'Lunch', timing: '1:00 PM', details: 'Turkey and cheese sandwich with salad', calories: '600' });
            dietPlan.push({ meal: 'Afternoon Snack', timing: '4:00 PM', details: 'Cottage cheese with pineapple', calories: '200' });
            dietPlan.push({ meal: 'Dinner', timing: '7:00 PM', details: 'Grilled fish with quinoa and steamed vegetables', calories: '500' });
            break;
        case 'Overweight':
            dietPlan.push({ meal: 'Breakfast', timing: '7:00 AM', details: 'Smoothie with spinach, banana, and protein powder', calories: '400' });
            dietPlan.push({ meal: 'Morning Snack', timing: '10:00 AM', details: 'Carrot sticks with hummus', calories: '200' });
            dietPlan.push({ meal: 'Lunch', timing: '1:00 PM', details: 'Grilled vegetable wrap with side salad', calories: '600' });
            dietPlan.push({ meal: 'Afternoon Snack', timing: '4:00 PM', details: 'Greek yogurt with granola', calories: '200' });
            dietPlan.push({ meal: 'Dinner', timing: '7:00 PM', details: 'Baked chicken with sweet potato and green beans', calories: '500' });
            break;
        case 'Obese':
            dietPlan.push({ meal: 'Breakfast', timing: '7:00 AM', details: 'Whole grain pancakes with berries and maple syrup', calories: '400' });
            dietPlan.push({ meal: 'Morning Snack', timing: '10:00 AM', details: 'Low-fat cheese with whole grain crackers', calories: '200' });
            dietPlan.push({ meal: 'Lunch', timing: '1:00 PM', details: 'Turkey chili with brown rice', calories: '600' });
            dietPlan.push({ meal: 'Afternoon Snack', timing: '4:00 PM', details: 'Vegetable sticks with ranch dip', calories: '200' });
            dietPlan.push({ meal: 'Dinner', timing: '7:00 PM', details: 'Grilled steak with roasted potatoes and broccoli', calories: '500' });
            break;
        default:
            dietPlan.push({ meal: 'Unable to generate diet plan.', timing: '', details: '', calories: '' });
    }

    // Populate table with diet plan
    dietPlan.forEach(function (item) {
        var row = dietTable.insertRow();
        row.insertCell(0).innerHTML = item.meal;
        row.insertCell(1).innerHTML = item.timing;
        row.insertCell(2).innerHTML = item.details;
        row.insertCell(3).innerHTML = item.calories;
    });
}





Css


body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

.container {
    max-width: 800px;
    margin: 50px auto;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    padding: 20px;
}

.header {
    background-color: #007bff;
    color: #fff;
    padding: 20px;
    text-align: center;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    margin-bottom: 20px;
}

.section {
    background-color: #f8f9fa;
    padding: 20px;
    border-radius: 5px;
    margin-bottom: 20px;
}

.section-title {
    color: #333;
    margin-bottom: 10px;
}

.bmi-section, .diet-plan-section {
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    margin-bottom: 20px;
}

.form-group {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 5px;
}

input[type="number"] {
    width: calc(100% - 22px);
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    background-color: #007bff;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

#result {
    margin-top: 20px;
}

#diet-plan {
    color: #333;
}

table {
    width: 100%;
    border-collapse: collapse;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
}

th {
    background-color: #007bff;
    color: #fff;
    font-weight: bold;
    text-align: left;
}

.quote, .thankyou {
    text-align: center;
    margin-bottom: 20px;
    font-style: italic;
    color: #666;
}






Html





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BMI Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="container">
    <div class="header">
        <h1>BMI Calculator</h1>
    </div>
    <div class="section">
        <h2 class="section-title">Our 20-day nutrition program will change the way you look at food forever.</h2>
        <p>Our comprehensive nutrition program is designed to transform your relationship with food and help you achieve your health goals.</p>
    </div>
    <div class="section">
        <h2 class="section-title">From meal planning and nutrition to sleep and supplements, we'll help you create a personalized plan to meet your goals.</h2>
        <p>Our expert team will guide you through every step of the process, ensuring you have the support and resources you need to succeed.</p>
    </div>
    <div class="section">
        <h2 class="section-title">Meal planning</h2>
        <p>Create custom meal plans and grocery lists with our 200+ delicious recipes.</p>
    </div>
    <div class="section">
        <h2 class="section-title">Results</h2>
        <p>Track your progress and see your results with our personalized diet and exercise plans.</p>
    </div>
    <div class="quote">
        <p><em>Goodbye trendy diets. Hello mindful eating.</em></p>
    </div>
    <div class="bmi-section">
        <h2 class="section-title">BMI Calculator</h2>
        <form id="bmi-form">
            <div class="form-group">
                <label for="height">Height (cm):</label>
                <input type="number" id="height" placeholder="Enter your height in cm">
            </div>
            <div class="form-group">
                <label for="weight">Weight (kg):</label>
                <input type="number" id="weight" placeholder="Enter your weight in kg">
            </div>
            <button type="button" onclick="calculateBMI()">Calculate BMI</button>
        </form>
        <div id="result"></div>
    </div>
    <div class="diet-plan-section">
        <h2 class="section-title">Diet Plan</h2>
        <div id="diet-plan">
            <table id="diet-table">
                <tr>
                    <th>Meal</th>
                    <th>Timing</th>
                    <th>Meal Details</th>
                    <th>Calories</th>
                </tr>
            </table>
        </div>
    </div>
</div>
  <div class="thankyou">
        <p>Thank you for using our page! </p>
~By Uday 
    </div>
<script src="script.js"></script>
</body>
</html>
