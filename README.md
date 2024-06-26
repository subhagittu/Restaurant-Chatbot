<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
</head>
<body>

<h1>Restaurant Chatbot</h1>
<img width="960" alt="yt_clone" src="https://github.com/subhagittu/Restaurant-Chatbot/blob/4e3194e0fad994fd0fd036744aaeee564978fe61/Screenshot%202024-05-26%20150551.png">
<p>This project is a restaurant chatbot built using FastAPI and Dialogflow. It handles various functionalities such as adding items to an order, removing items from an order, completing an order, and tracking an order status. The chatbot interacts with a MySQL database to store and retrieve order information.</p>

<h2>Project Structure</h2>
<ul>
    <li><strong>main.py:</strong> The main FastAPI application that handles incoming requests and routes them to the appropriate intent handlers.</li>
    <li><strong>generic_helper.py:</strong> A helper module containing utility functions for string manipulations and session ID extraction.</li>
    <li><strong>db_helper.py:</strong> A database helper module for interacting with the MySQL database, including functions for inserting order items, tracking orders, and fetching order details.</li>
</ul>

<h2>Dependencies</h2>
<p>To run this project, you need the following dependencies:</p>
<ul>
    <li>FastAPI</li>
    <li>Uvicorn</li>
    <li>mysql-connector-python</li>
</ul>
<img width="960" alt="yt_clone" src="https://github.com/subhagittu/Restaurant-Chatbot/blob/6064a2164903fbdc21ac049cd34c4a3981f2b214/Screenshot%202024-05-26%20152401.png">
<h2>Installation</h2>
<ol>
    <li>Clone the repository:</li>
    <pre><code>git clone &lt;repository-url&gt;</code></pre>
    <li>Navigate to the project directory:</li>
    <pre><code>cd &lt;project-directory&gt;</code></pre>
    <li>Install the required dependencies:</li>
    <pre><code>pip install -r requirements.txt</code></pre>
    <li>Ensure MySQL is installed and running, and update the database connection details in <code>db_helper.py</code>:</li>
    <pre><code>cnx = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="your_database"
)</code></pre>
</ol>

<h2>Usage</h2>
<ol>
    <li>Start the FastAPI server:</li>
    <pre><code>uvicorn main:app --reload</code></pre>
    <li>Integrate the webhook URL with your Dialogflow agent.</li>
    <li>Interact with the chatbot through the Dialogflow interface or any integrated platform (e.g., Google Assistant).</li>
</ol>

<h2>Intent Handlers</h2>
<ul>
    <li><strong>add_to_order:</strong> Adds specified food items and quantities to the current order.</li>
    <li><strong>remove_from_order:</strong> Removes specified food items from the current order.</li>
    <li><strong>complete_order:</strong> Completes the current order, saves it to the database, and provides the order total and ID.</li>
    <li><strong>track_order:</strong> Tracks the status of a given order ID.</li>
</ul>

<h2>Database Procedures</h2>
<p>The MySQL database includes the following stored procedures:</p>
<ul>
    <li><code>insert_order_item(food_item, quantity, order_id):</code> Inserts an item into the order.</li>
    <li><code>insert_order_tracking(order_id, status):</code> Inserts an order status into the tracking table.</li>
    <li><code>get_total_order_price(order_id):</code> Returns the total price for the specified order.</li>
    <li><code>get_order_status(order_id):</code> Returns the status of the specified order.</li>
</ul>

<h2>Deployment</h2>
<p>This project is successfully working and has been integrated on an html web page</p>

</body>
</html>
