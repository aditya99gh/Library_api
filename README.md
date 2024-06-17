# Library_api
Pre-requisites:
Python 3.x

To set up this project locally, follow these steps:

1. Clone the repository:
    git clone [https://github.com/aditya99gh/Library_api.git]
    cd your-repository

2. Create a virtual environment:
     python -m venv venv
   
3. Activate the virtual environment:
     venv\Scripts\activate
   
4. Install dependencies:
     pip install -r requirements.txt
   
5. Set up database:
     python manage.py migrate

6. Create a superuser (optional):
     python manage.py createsuperuser

7. Start the development server:
     python manage.py runserver

8. Access the application:
     Open your web browser and navigate to http://localhost:8000/


   After this you can access the django database and play around with it, like creating books, magazines, subscription plans, etc.
   Then to check the APIs, we could hit below requests:
   1. ORDER ITEM : curl -X POST http://127.0.0.1:8000/api/order/ -H "Content-Type: application/json" -d "{ \"user_id\": 1, \"title\": \"Horror\", \"type\": \"book\"}"
   2. RETURN ITEM : curl -X POST http://localhost:8000/api/return/ -H "Content-Type: application/json" -d "{\"user_id\": 1, \"titles\": [\"Horror\"], \"type\": \"book\"}"
