# EX-05: Server side processing
# Date:11/11/24
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
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Triangle Area Calculator</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

        body {
            font-family: 'Poppins', sans-serif; /* Clean, modern font style */
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #74b9ff, #55efc4, #ffeaa7);
            background-size: 300% 300%;
            animation: gradientBG 6s ease infinite;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            color: #2d3436;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            text-align: center;
            padding: 20px;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 30px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.4);
        }

        label {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 10px;
            display: block;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
        }

        input {
            background: rgba(255, 255, 255, 0.9);
            border: none;
            border-radius: 10px;
            width: calc(100% - 30px);
            padding: 12px 15px;
            margin: 10px 0;
            font-size: 1rem;
            color: #2d3436;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        button {
            background-color: #0984e3;
            color: white;
            border: none;
            padding: 12px 25px;
            margin-top: 20px;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: transform 0.2s, background-color 0.3s;
        }

        button:hover {
            background-color: #74b9ff;
            transform: scale(1.05);
        }

        .box {
            margin: 15px 0;
            padding: 20px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(5px);
        }

        h2 {
            color: #0984e3;
            margin-top: 20px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.4);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Triangle Area Calculator</h1>
        <form method="post">
            {% csrf_token %}
            <div class="box">
                <label for="base">Base:</label>
                <input type="number" id="base" name="base" step="any" required>
            </div>
            <div class="box">
                <label for="height">Height:</label>
                <input type="number" id="height" name="height" step="any" required>
            </div>
            <div class="box">
                <button type="submit">Calculate Area</button>
            </div>
        </form>
        {% if area is not None %}
            <h2>Area of the Triangle: {{ area }}</h2>
        {% endif %}
    </div>
</body>
</html>
~~~
# SERVER SIDE PROCESSING:
![Screenshot 2024-12-09 082207](https://github.com/user-attachments/assets/76fc9ff4-01bb-41c6-95dd-01640dd3a7ca)

# HOMEPAGE:

![Screenshot 2024-12-09 081933](https://github.com/user-attachments/assets/bb81fbac-7d6b-4f09-ac13-abc872270ec4)

# RESULT:
The program for performing server side processing is completed successfully.
