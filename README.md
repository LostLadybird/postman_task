# postman_task

1. Регистрируемся (Registration)
POST https://blog.kata.academy/api/users
{
  "user": {
    "username": "Julia",
    "email": "user@mail.ru",
    "password": "user123"
  }
}

Rsponse:
{
    "user": {
        "username": "julia",
        "email": "user@mail.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0MDhmMzY4NmY4YmVlMWIwMDU1NWQxOCIsInVzZXJuYW1lIjoianVsaWEiLCJleHAiOjE2ODM0OTIyMDAsImlhdCI6MTY3ODMwODIwMH0.46ayq_45-zHPs3XMYwVjXlNlni0J3rHptl6xuFZfDtc"
    }
}

2. Логинимся (Authentication):
POST https://blog.kata.academy/api/users/login
{
  "user": {
    "email": "user@mail.ru",
    "password": "user123"
  }
}

Response:
{
    "user": {
        "username": "julia",
        "email": "user@mail.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0MDhmMzY4NmY4YmVlMWIwMDU1NWQxOCIsInVzZXJuYW1lIjoianVsaWEiLCJleHAiOjE2ODM0OTIzMjgsImlhdCI6MTY3ODMwODMyOH0.tHd3vBEw-VranXpG-OqKJKmZXvalZgnV-pWbvZPeAww"
    }
}

3. Используя заголовок авторизации получить данные текущего пользователя (Endpoints -> Get Current User):
GET https://blog.kata.academy/api/user
Вкладка Authorization - bearer token:
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0MDhmMzY4NmY4YmVlMWIwMDU1NWQxOCIsInVzZXJuYW1lIjoianVsaWEiLCJleHAiOjE2ODM0OTIzMjgsImlhdCI6MTY3ODMwODMyOH0.tHd3vBEw-VranXpG-OqKJKmZXvalZgnV-pWbvZPeAww

Response:
{
    "user": {
        "username": "julia",
        "email": "user@mail.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY0MDhmMzY4NmY4YmVlMWIwMDU1NWQxOCIsInVzZXJuYW1lIjoianVsaWEiLCJleHAiOjE2ODM0OTI1MDksImlhdCI6MTY3ODMwODUwOX0.eaY9vYv1L1ZEnrYIKfDJIiqfQotlLr1dniCm4wGqcLI"
    }
}
