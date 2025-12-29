# E-Insurance Management System

The E-Insurance Management Web Application is a digital solution designed to streamline insurance operations. It provides a user-friendly platform for insurance providers to manage policies and for policyholders to handle their insurance needs effectively.

### Key Features

* **Policy Management**: Create, modify, and renew insurance policies online while storing details like coverage and premiums.
* **Customer Portal**: A self-service area where policyholders can view their information, file claims, and get personalized recommendations.
* **Customer Interaction**: Includes features for customers to ask questions and receive feedback from administrators.
* **Secure Data Management**: Built with security in mind, utilizing encryption and access controls to protect sensitive financial and personal information.

### Technical Stack

* **Framework**: Django 3.0.5
* **Language**: Python 3.11
* **Frontend**: HTML, CSS (Bootstrap), JavaScript
* **Static Files**: WhiteNoise
* **Production Server**: Gunicorn

### Local Setup

To run this project on your local machine, follow these steps:

1. **Clone the Repository**:
```bash
git clone https://github.com/KelvinMutuku/E-Insuarance.git
cd E-Insuarance

```


2. **Create a Virtual Environment**:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

```


3. **Install Dependencies**:
Make sure you have `Pillow` installed for image handling.
```bash
pip install -r requirements.txt

```


4. **Database Setup**:
Run the migrations to initialize the SQLite database.
```bash
python manage.py migrate

```


5. **Create a Superuser**:
This allows you to access the admin dashboard at `/admin`.
```bash
python manage.py createsuperuser

```


6. **Run the Application**:
```bash
python manage.py runserver

```


Visit `http://127.0.0.1:8000` in your browser.

### Deployment (Render)

This project is configured to run on Render. If you are setting this up for the first time, follow these steps:

1. **Environment Variables**: You must set the following keys in your dashboard:
* `PYTHON_VERSION`: `3.11.10`
* `SECRET_KEY`: Your Django secret key.
* `EMAIL_HOST_USER` & `EMAIL_HOST_PASSWORD`: For the contact form functionality.
* `ALLOWED_HOSTS`: Include `e-insuarance.onrender.com`.


2. **Build Command**:
```bash
./build.sh

```


3. **Start Command**:
```bash
gunicorn insurancemanagement.wsgi:application

```



### License

This project is licensed under the terms of the MIT license.

---

**Live Demo:** [https://e-insuarance.onrender.com](https://e-insuarance.onrender.com)
