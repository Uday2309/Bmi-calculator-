


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
