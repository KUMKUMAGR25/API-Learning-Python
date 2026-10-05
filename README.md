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
<br>
def home():
<br>
   return {"message": "Hello, FastAPI!"}

<br>
<br>
#API Endpoints

<br>
Endpoints are URLs through which clients communicate with the application.
<br>
▪︎ GET    /users
<br>
▪︎ POST   /users
<br>
▪︎ PUT    /users/{id}
<br>
▪︎ DELETE /users/{id}
<br>
<br>
● Path Parameters

<br>
Path parameters are values passed directly through the URL.
<br>
@app.get("/users/{user_id}")
<br>
def get_user(user_id: int):
<br>
   return {"user_id": user_id}
<br>
<br>
● Query Parameters
<br>
Query parameters are used to send additional information through the URL.
<br>
@app.get("/search")
<br>
def search(name: str):
<br>
    return {"name": name}
<br>
<br>
● Request Body
<br>
Request bodies are used to send structured data to the API.
<br>
<br>
from pydantic import BaseModel
<br>
class Student(BaseModel):
<br>
    name: str
    <br>
    age: int
    <br>

@app.post("/students")
<br>
def create_student(student: Student):
<br>
    return student
<br>
<br>
● Pydantic
<br>
Pydantic is used for data validation and defining the structure of request and response data.
<br>
CRUD Operations
<br>
Create → POST
<br>
Read → GET
<br>
Update → PUT/PATCH
<br>
Delete → DELETE
<br>
<br>
Status Codes
<br>
200 → Successful request
<br>
201 → Resource created
<br>
400 → Bad request
<br>
404 → Resource not found
<br>
500 → Server error
<br>
<br>
● Error Handling
<br>
FastAPI provides HTTPException for handling API errors.
<br>
from fastapi import HTTPException
<br>
raise HTTPException(
<br>
    status_code=404,
    <br>
    detail="User not found"
    <br>
)
<br>
<br>
● Automatic Documentation
<br>
FastAPI automatically provides interactive API documentation.
<br>
/docs
<br>
/redoc
<br>
<br>
● FastAPI + Database
<br>

FastAPI can be connected with databases such as SQLite, MySQL, and PostgreSQL to store and manage application data.
<br>
<br>
● FastAPI + Machine Learning
<br>
FastAPI can be used to deploy Python machine learning models as APIs.
<br>
Frontend → FastAPI → ML Model → Prediction
<br>
<br>
FastAPI + Frontend
<br>
FastAPI can act as the backend and communicate with frontend technologies such as HTML, CSS, JavaScript, and React.
