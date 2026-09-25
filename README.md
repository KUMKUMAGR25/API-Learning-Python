# FASTAPI-Learning-Python
As a Beginner-friendly FastAPI learning repository.

<br>
Que: What is FastAPI?
<br>
FastAPI is a Python framework used to build APIs.
<br>
FastAPI allows you to create a backend/API using Python that can communicate with websites, mobile apps, databases, and AI/ML models.
<br>
=> Key Features
<br>
● Fast and high-performance.
<br>
● Easy to learn and use.
<br>
● Automatic interactive API documentation.
<br>
● Built-in request and data validation.
<br>
● Supports asynchronous programming.
<br>
● Uses Python type hints.
<br>
● Easy integration with databases and ML models.
<br>
<br>
#FastAPI in AI/ML
<br>
○FastAPI can be used to create an API around a Python machine learning model.
<br>
Frontend → FastAPI → ML Model → Prediction → Frontend
<br>
○This makes it possible to connect ML models with websites, mobile applications, and other software.
<br>
<br>
#What I Learned
<br>
●FastAPI basics.
<br>
●API endpoints and routes.
<br>
●GET and POST requests.
<br>
●Request and response handling.
<br>
●API documentation.
<br>
●Pydantic and data validation.
<br>
●Connecting FastAPI with Python/ML projects.
<br>
<br>
■ Installation
<br>
pip install fastapi uvicorn
<br>
Basic FastAPI Application
<br>
from fastapi import FastAPI
<br>
app = FastAPI()

<br>
<br>
■ Run the Application
<br>
uvicorn main:app --reload

<br>
@app.get("/")
def home():
<br>
   return {"message": "Hello, FastAPI!"}

<br>
<br>
#API Endpoints

<br>
Endpoints are URLs through which clients communicate with the application.
<br>
GET    /users
<br>
POST   /users
<br>
PUT    /users/{id}
<br>
DELETE /users/{id}
<br>
<br>
Path Parameters

<br>
Path parameters are values passed directly through the URL.
<br>
@app.get("/users/{user_id}")
<br>
def get_user(user_id: int):
<br>
    <br>return {"user_id": user_id}
