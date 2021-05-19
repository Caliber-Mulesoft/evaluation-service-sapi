# Evaluation Service System API

# ABOUT THE PROJECT
The Evaluation Service API app is a service level api that encapsulates assessment data from the Caliber API.

# BUILT WITH
- Mulesoft
- MUnit
- Log4J
- Maven
- Anypoint Platform
- Anypoint Studio
- REST
  
# GETTING STARTED
- Go to ${users.home}/m2 folder:
- Rename or delete repository
- Rename settings.xml
- git clone https://github.com/Caliber-Mulesoft/evaluation-service-sapi.git
- Import project AssessmentsProcessAPI into Anypoint Studio (the folder containing the project has the same name).
- Deploy to CloudHub (Anypoint Platform)
- Please refer to the SETUP document for more detailed installation steps.

# PREREQUISITES
- Anypoint platform
- Anypoint studio 7.8.0
- OpenJDK 8
- Embedded Maven
- HTTP connector 1.5.24
- APIkit 1.5.1

# USAGE EXAMPLES
- GET all assessments: /assessments
Example Response:
```
[
  {
    "assessmentId": 63,
    "rawScore": 100,
    "assessmentTitle": "Mock Assessment 1-0",
    "assessmentType": "Presentation",
    "weekNumber": 1,
    "batchId": "TR-1028",
    "assessmentCategory": 5,
    "assignmentDate": "01-01-2020"
  },
  {
    "assessmentId": 64,
    "rawScore": 100,
    "assessmentTitle": "Mock Assessment 1-1",
    "assessmentType": "Presentation",
    "weekNumber": 1,
    "batchId": "TR-1028",
    "assessmentCategory": 39,
    "assignmentDate": "02-02-2020"
  }
]
```
- GET assessments by ID: /assessments/{ID}
Example Response:
```
[
  {
    "assessmentId": 63,
    "rawScore": 100,
    "assessmentTitle": "Mock Assessment 1-0",
    "assessmentType": "Presentation",
    "weekNumber": 1,
    "batchId": "TR-1028",
    "assessmentCategory": 5,
    "assignmentDate": "01-01-2020"
  }
]
```
- GET all grades: /grades
Example Response:
```
[
  {
    "dateRecieved": "2021-04-16",
    "gradeId": 1,
    "score": 9.104028,
    "traineeId": "SF-2128",
    "assessmentId": 1
  },
  {
    "dateRecieved": "2021-01-06",
    "gradeId": 24660,
    "score": 83.40503,
    "traineeId": "SF-1819",
    "assessmentId": 1355
  }
]
```
- GET grades by ID: /grades/{ID}
Example Output:
```
[
  {
    "dateRecieved": "2021-04-16",
    "gradeId": 1,
    "score": 9.104028,
    "traineeId": "SF-2128",
    "assessmentId": 1
  }
]
```
- GET an average of grades dependent on the week, assessment or batch: /average
Example Output:
```
76.988
```

# AUTHORS
- Christopher Proutt
- Diego Franchi
- Daniel Beintema
- Kevin Novikov
