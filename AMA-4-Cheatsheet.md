## Django, Web, and HTTP Concepts 
### 1. What are validators in Django?
Validators are functions or classes used to **validate data** before saving it to the database.  
They ensure the data meets specific rules (like range, format, length).

Example:
- EmailValidator
- MinValueValidator
- MaxLengthValidator

### 2. What is the use of fields in Django?
Fields define the **type of data** stored in a model and how it is represented in the database.

Examples:
- CharField – text
- IntegerField – numbers
- DateField – dates
- BooleanField – true/false

Fields also handle validation and database column creation.

### 3. Client and Server Architecture
Client–Server architecture divides an application into two parts:
- **Client**: Sends requests (browser, mobile app)
- **Server**: Processes requests and sends responses (Django backend)

This improves scalability, security, and separation of concerns.


### 4. What does document represent?
A document represents a **single record** stored in a document-based database (like MongoDB).  
It is usually stored in **JSON-like format** and contains key–value pairs.


### 5. What is Click Jacking?
Clickjacking is a security attack where a user is tricked into clicking something different from what they see.  
Django prevents this using the **X-Frame-Options middleware**.

### 6. What is MVT?
MVT stands for:
- **Model** – handles data and database logic
- **View** – handles business logic
- **Template** – handles UI

Django follows the **MVT architectural pattern**.

### 7. Difference between `startproject` and `startapp`

| Command | Purpose |
|-------|---------|
| `startproject` | Creates the main Django project |
| `startapp` | Creates a reusable app inside the project |


### 8. Is Django a frontend or backend framework?
Django is a **backend framework**.  
It handles:
- Database operations
- Business logic
- Authentication
- APIs

Frontend is usually handled using HTML, CSS, JavaScript, React, etc.


### 9. Use of `urls.py`
`urls.py` maps **URLs to views**.  
It decides which view should handle a specific request.

Example:
- `/login/` → login view
- `/products/` → products view


### 10. What is status code 200 and 404?

| Status Code | Meaning |
|------------|---------|
| 200 | Request successful |
| 404 | Resource not found |


### 11. Command to create an app in Django
```bash
python manage.py startapp app_name
```
