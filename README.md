# Smart-Temperature-Monitoring-System
Overview
The Smart-Temperature-Monitoring-System is a Flask-based web app designed to monitor and manage environmental data using sensors. It integrates with AWS S3 for data storage, AWS SES for email alerts, and MySQL for database management. The app supports user authentication, data visualization, and real-time monitoring with GPIO support for hardware interactions.

Features
User Authentication: Secure login and signup functionalities.
Sensor Data Management: Collects temperature and humidity data from DHT22 sensors.
Real-Time Monitoring: Displays sensor data in real-time and handles data threshold alerts.
Data Storage: Stores sensor data in MySQL and uploads data to AWS S3.
Email Alerts: Sends alerts via AWS SES when sensor thresholds are exceeded.
GPIO Integration: Controls hardware components like LEDs based on sensor readings.
Getting Started
Prerequisites
Python 3.x (preferred version 3.8+)
Flask
Flask-Login
Flask-WTF
Adafruit-DHT
RPi.GPIO
mysql-connector-python
boto3
Werkzeug
Installation
Clone the repository:


git clone https://github.com/Kaushalmaurya07/Smart-Temperature-Monitoring-System.git
Navigate into the project directory:


cd sensor-monitoring-web-app
Create a virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install dependencies:

pip install -r requirements.txt
Set up your environment variables:

Create a .env file in the root directory with the following content (adjust with your own configurations):

plaintext

SECRET_KEY=your_secret_key
AWS_REGION=aws_region_name
AWS_ACCESS_KEY=your_access_key
AWS_SECRET_KEY=your_secret_access_key
S3_BUCKET_NAME=s3_bucket_name
MYSQL_HOST=localhost
MYSQL_USER=newuser
MYSQL_PASSWORD=mysql
MYSQL_DATABASE=sensor_db

Run the application:
python app.py
The application will be available at http://localhost:5000.

Usage
Access the Application: Navigate to http://localhost:5000 in your web browser.
Login/Signup: Use the provided login and signup forms to access the application.
Sensor Data: The home page displays real-time sensor data and updates based on sensor readings.
View Historical Data: Access historical data through endpoints that fetch data for different time ranges.
Contributing
Contributions are welcome! To contribute:

Fork the repository.

Create a new branch:

git checkout -b feature-branch
Make your changes and commit them:


git commit -am 'Add new feature'
Push to the branch:

git push origin feature-branch
Open a pull request to merge your changes.

For detailed contributing guidelines, refer to CONTRIBUTING.md.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgements
Adafruit-DHT for sensor support.
boto3 for AWS integrations.
RPi.GPIO for GPIO control on Raspberry Pi.
Contact
For support or inquiries, contact:

Email: kaushalmaurya07@gmail.com
GitHub: kaushalmaurya07
