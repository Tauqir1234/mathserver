# Ex.05 Design a Website for Server Side Processing
# Date:9/11/2024
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
            padding: 20px;
        }
        h1 {
            color: #555;
        }
        .calculator {
            margin: 20px auto;
            padding: 20px;
            background: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            max-width: 400px;
        }
        input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            background-color: #5cb85c;
            color: white;
            font-size: 16px;
            cursor: pointer;
        }
        button:hover {
            background-color: #4cae4c;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
        }
    </style>
    </head>
    <body>
        <div class="image">
        <h1 style="text-align: center;">Calculate Power</h1>
        <form method="post">
              {% csrf_token %}
              <label for="intensity">Intensity (I):</label>
              <input type="number" step="0.01" id="intensity" name="intensity" required>
              <label for="resistance"><br>Resistance (R):</label>
              <input type="number" step="0.01" id="resistance" name="resistance" required>
            <button type="submit">Calculate Power</button>
        </form>
        {% if power is not None %}
        <div class="result">
           <h2>Result</h2>
           <p><strong>Power (P):</strong> {{ power }} Watts</p>
        </div>
        </div>
        {% endif %}
    </body>
</html>

```

# SERVER SIDE PROCESSING:
![alt text](<Screenshot 2024-12-07 144925.png>)
# HOMEPAGE:
![alt text](<Screenshot 2024-12-07 144858.png>)
# RESULT:
The program for performing server side processing is completed successfully.
