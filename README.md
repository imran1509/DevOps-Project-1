# DevOps Project 1 (using Docker, Jenkins and AWS)
In this project we will deploy a Django todo app on an AWS EC2 instance using Docker and Jenkins.

## Prerequisites
Before starting the project you should have these things in your system.

- **Jenkins** installed
- **Docker** installed
- Account on **AWS**
- **Python** with Virtual environment & **Django** installed
- Todo App code (we will use code from this repository : [Django todo app](https://github.com/shreys7/django-todo))

## Step 1 : Run Locally

Before deploying the app on AWS, we will test run the app locally.

- Create a folder for the project, open the folder in VS code and open terminal in VS Code.
- Clone the repository.

```bash
  git clone https://github.com/shreys7/django-todo.git
```
![](https://github.com/imran1509/DevOps-Project-1/blob/main/Screenshots/1.PNG)

- Now we will create a virtual environment named env for the app so that it doesn't affect our system.

```bash
   virtualenv -p python3.11 env
```
- Activate the vritual environment

For windows/VS Code
```bash
   env\Scripts\activate
```

For Linux/MacOS/Git Bash
```bash
   source env/bin/activate
```

- Change directory to the app directory

```bash
   cd django-todo
```
- create all the migrations file (database migrations) required to run this App.

```bash
   python manage.py makemigrations
```
- Now, to apply this migrations run the following command

```bash
   python manage.py migrate
```
- We need to create an admin user to run this App. Type the following command and provide username, password and email for the admin user

```bash
   python manage.py createsuperuser
```
- We just need to start the server now. Start the server by following command

```bash
   python manage.py runserver
```
- Once the server is hosted, head over to http://127.0.0.1:8000/todos to check the app is running,
