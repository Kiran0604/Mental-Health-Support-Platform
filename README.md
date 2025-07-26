# Mental Health Support Platform

A web-based platform designed to connect individuals with therapists, providing tools for booking appointments, real-time chat, and support from an integrated AI assistant. This project is built with Python and Flask and is deployed on Microsoft Azure.

---
## ✨ Key Features

* **User Authentication**: Secure registration and login for patients and therapists.
* **Appointment Booking**: Patients can view therapist availability and book sessions.
* **Real-time Chat**: Secure, real-time communication between patients and therapists using Socket.IO.
* **AI-Powered Assistant**: An integrated conversational AI (using Google's Generative AI) to provide initial support and information.
* **Separate User Dashboards**: Customized dashboards for both patients and therapists to manage their information and appointments.
* **Email Notifications**: Automated email confirmations for appointments and other important events.

---
## 🚀 Technology Stack

* **Backend**: Python, Flask
* **Database**: MySQL
* **Real-time Communication**: Flask-SocketIO
* **AI Integration**: Google Generative AI
* **Deployment**: Microsoft Azure App Service + Azure Database for MySQL
* **Frontend**: HTML, CSS, JavaScript

---
## ⚙️ Setup and Local Installation

To run this project on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Kiran0604/Mental-Health-Support-Platform.git](https://github.com/Kiran0604/Mental-Health-Support-Platform.git)
    cd Mental-Health-Support-Platform
    ```

2.  **Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up your local database:**
    * Make sure you have a local MySQL server running.
    * Create a database (e.g., `therapy`).
    * Import the database schema and data from your `.sql` file if you have one.

5.  **Configure environment variables:**
    * Create a `.env` file in the root directory.
    * Add your local database credentials and other secret keys to this file:
        ```env
        DB_HOST=localhost
        DB_USER=your_local_user
        DB_PASSWORD=your_local_password
        DB_NAME=therapy
        FLASK_SECRET_KEY=a_very_long_and_random_string
        # Add any other keys like for Google AI or email
        ```
    * Ensure your `app.py` is configured to load these variables.

6.  **Run the application:**
    ```bash
    flask run
    ```
    The application will be available at `http://127.0.0.1:5000`.

---
## ☁️ Azure Deployment

This application is deployed on Microsoft Azure using the following services:

* **Azure App Service**: Hosts the Flask web application. Deployment is automated via GitHub Actions, triggering on every push to the `main` branch.
* **Azure Database for MySQL (Flexible Server)**: A managed database service that hosts the application's data.

The live application can be accessed at:
[https://mentalhealth-platform-a6byenawd4dfgnah.southindia-01.azurewebsites.net/](https://mentalhealth-platform-a6byenawd4dfgnah.southindia-01.azurewebsites.net/)
