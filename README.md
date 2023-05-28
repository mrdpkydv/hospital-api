
  # Hospital Rest-API
## Description
 We’re going to design an API for the doctors of a Hospital which has been allocated by the
govt for testing and quarantine + well being of COVID-19 patients
- There can be 2 types of Users
- Doctors
- Patients
- Doctors can log in
- Each time a patient visits, the doctor will follow 2 steps
- Register the patient in the app (using phone    number, if the patient already exists, just
return the patient info in the API)
- After the checkup, create a Report
- Patient Report will have the following fields
- Created by doctor
- Status (patient status like:- fever , malaria etc):

The Routes here used in project
- /doctors/register → with username and password
- /doctors/login → returns the JWT to be used
- /patients/register
- /patients/:id/create-report
- /patients/:id/all_reports → List all the reports of a patient oldest to latest
- /reports/:status → List all the reports of all the patients filtered by a specific status
  
## Tech stack
 Node.js , Express , Mongo-DB , passport-JWT
  

  ## Operation check route end point on postman
  * http://localhost:8000/doctors/register
  * here doctors register themselves on this request end point
  ![Alt text](https://github.com/DivyaGaurav21/Hospital-API/blob/master/postman_screenshot/Screenshot%20(53).png?raw=true)
  * http://localhost:8000/doctors/login
  * now doctor login on this request.
  ![Test Image 4](https://github.com/DivyaGaurav21/Hospital-API/blob/master/postman_screenshot/Screenshot%20(54).png?raw=true)
  * by using doctor login jwt bearer jwt token , patient will be creatatd.
  * http://localhost:8000/patients/register
  ![test5](https://github.com/DivyaGaurav21/Hospital-API/blob/master/postman_screenshot/Screenshot%20(55).png?raw=true)
  * now creating of patient report edpoint by taking patient id (63f8b34ecf8cd598d92bfd44) reference.
  * http://localhost:8000/patients/:id/create-report 
  ![test6](https://github.com/DivyaGaurav21/Hospital-API/blob/master/postman_screenshot/Screenshot%20(56).png?raw=true)
  * now showing all report of patient by patient id(63f8b34ecf8cd598d92bfd44).
  * http://localhost:8000/patients/:id/all_reports

  ![test5](https://github.com/DivyaGaurav21/Hospital-API/blob/master/postman_screenshot/Screenshot%20(57).png?raw=true)
  * route endpoints :- /reports/:status
  ![test5](https://github.com/DivyaGaurav21/Hospital-API/blob/master/postman_screenshot/Screenshot%20(58).png?raw=true)
 
