# TokenBasedAuthentication
Web API Token Authentication

GET http://localhost:55288/api/orders 401 Unauthorized

POST http://localhost:55288/api/account/register
Content-Type: application/json 
{ "userName": "Somprasong", "password": "123456", "confirmPassword": "123456" }
200 OK

POST http://localhost:55288/token
Content-Type: application/x-www-form-urlencoded or Content-Type: application/json
grant_type=password&username=Somprasong&password=123456 
200 OK
Example Result : 
{ access_token: "yUYh2B-2ZSzcnXf7cuft8vVCkPa5_mok9dWhPSwuARc98zAxFqW-oPv-htVvSXjoDa-U0aV6w6GiKbNg3fiArQT5xyujcQ4BlqwYavnPWDpR2RWd2ymjZmmoXXfs7MzK4rkJeV6QP-Bhx3VA1lfBzhJmxiov43lZEpB_xGPZ6_KZVcPHegLhLEV_Nqni_am6FogNt5tJH6eu-Fub5Vwzv8wxFwolOB5Ta8QOU7lh2ghFk5tD5IJtKF62lstXZEMB" token_type: "bearer" expires_in: 86399 }

GET http://localhost:55288/api/orders 
Header Authorization : bearer eW6JjpLg-5M7sqdvwSdNcI8stL8n5xYQMw2c54jfRzBQMF2wW2Z_topsVEV8iIaWVqLyJqTKHI6qLFcHIUjaLOYoBloasX95gntFArKjDkJxCpSFbUM9D12GKh_5mOSVhCQskvSnPIsqWPULONhY6SjhcxVDWZXtyHuv7fQdqroXeFfo1zxIvppsx0_8d8Aq1DUn9TJ1ppv-__m1qtOxq4T8wuZ23J1GZ2XBSh2gH4flH1_4lzUp3NCFWgbFSLqM 200 OK Result : { orderID: 10248 customerName: "Taiseer Joudeh" shipperCity: "Amman" isShipped: true }- 1: { orderID: 10249 customerName: "Ahmad Hasan" shipperCity: "Dubai" isShipped: false }- 2: { orderID: 10250 customerName: "Tamer Yaser" shipperCity: "Jeddah" isShipped: false }
