## JUIT WebKiosk API - NodeJS (Unofficial)

<img alt="Javascript" src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E"/> <img alt="Nodejs" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/> <img alt="Puppeteer" src="https://img.shields.io/badge/Puppeteer-40B5A4?style=for-the-badge&logo=Puppeteer&logoColor=white"/>

A __working api__ for accessing JUIT WebKiosk Data. Created using NodeJS            


BASE URL: https://juit-webkiosk-api.herokuapp.com/


### Required request body
```
{
    "username": "XXXXXXXX",
    "password": "XXXXXXXX"
}
```

### Endpoints

* ```/v1.0/login```    
  Login into the JUIT WebKiosk portal.
  

* ```/v1.0/attendance```    
  Get attendance details for a given semester.
  

* ```/v1.0/personalDetails```   
  Get the personal details as on the webkiosk.
  

* ```/v1.0/cgpa```   
  Get the CGPA report for all semesters.
  

* ```/v1.0/grades```    
  Get the Exam Grades for a given semesters.
  

* ```/v1.0/semesters```    
  Get the list of valid Semester Codes.
  

* ```/v1.0/faculty```   
  Get the list of registered subject faculty.
  
  
* ```/v1.0/subjects```   
  Get the list of registered subjects for a given semester


## Examples

- ### Personal Details.
**Endpoint:**      
```https://juit-webkiosk-api.herokuapp.com/v1.0/personalDetails/```      
**Body:**     
 ```
 {
    "username":"xxxxx",
    "password":"xxxxx"
 }
```           
**Response:**
  ```
  {
    "Name": "Aarhan Ali Khan",
    "Rollno": "201221",
    "FathersName": "xxxx",
    "Course": "B.T. ( CSE)",
    "Semester": "4",
    "Mobile": "xxxxx",
    "ParentMobile": "xxxxx",
    "Email": "xxxxx",
    "address": "xxxx",
    "percentage12": "not that great to be put on display",
    "percentage10": "not that great to be put on display"
  }
  ```
- ### Faculty

**(NOTE- Pass in different semester codes, can get the available semester codes by calling the /semesters endpoint)**    

**Endpoint:**      
```https://juit-webkiosk-api.herokuapp.com/v1.0/grades/2020ODDSEM```  
**Body:**     
 ```
 {
    "username":"xxxxx",
    "password":"xxxxx"
 }
```     
**Response:**       
  ```
  [
    {
        "SubjectName": "ENGINEERING MATHEMATICS-I(18B11MA111)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A+"
    },
    {
        "SubjectName": "ENGINEERING PHYSICS LAB-I(18B17PH171)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A"
    },
    {
        "SubjectName": "ENGINEERING PHYSICS-I(18B11PH111)",
        "ExamCode": "2020ODDSEM",
        "Grade": "B+"
    },
    {
        "SubjectName": "ENGLISH AND TECHNICAL COMMUNICATION LAB(18B17HS171)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A+"
    },
    {
        "SubjectName": "ENGLISH AND TECHNICAL COMMUNICATION(18B11HS111)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A+"
    },
    {
        "SubjectName": "PROGRAMMING FOR PROBLEM SOLVING LAB-II(19B17CI171)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A"
    },
    {
        "SubjectName": "PROGRAMMING FOR PROBLEM SOLVING-II(19B11CI111)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A"
    },
    {
        "SubjectName": "WORKSHOP PRACTICES(18B17GE171)",
        "ExamCode": "2020ODDSEM",
        "Grade": "A"
    }
]
  ```
 flexing online sem grades ⌐■_■
