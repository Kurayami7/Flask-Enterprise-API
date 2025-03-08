# Flask-Enterprise-API

## Purpose: 
### Serve automated requests via HTTP Post to retreive records of 1000+ individuals. Built to serve as custom endpoints to retrieve data from Moodle DB.
=======

![image](https://github.com/Kurayami7/Flask-Enterprise-API/assets/124408792/a4351f9b-d597-4ed5-bef8-185456354f05)

### Get started
The Moodle settings:
* Site Administration > External Services > Add (add a new service which contains the `gradereport_user_get_grade_items` function.
* You will need to create a token for the function you just added. <br>Go back to Site Administration > Manage tokens > Create Token using the service you just added.
![image](https://github.com/Kurayami7/Flask-Enterprise-API/assets/124408792/ece04b8a-e3c9-417a-98c9-ebae77fefdb6)
![image](https://github.com/Kurayami7/Flask-Enterprise-API/assets/124408792/0c18dfdf-a31f-401e-a4ad-db883deb9eee)


Ensure you have Python installed. We will also need to install a couple of libraries via Pip. <br>
 * python get-pip.py <br>
 * pip install flask <br>
 * pip install tables <br>
 * pip install flask_sqlalchemy <br>
 * pip install requests <br>

Then, you will need to set up a virtual environment which will let you perform ~illegal~ modifications without affecting your local system files. <br>
 * $env:FLASK_APP = "moodle_flask_api.py" <br>
 * SET FLASK_APP=moodle_flask_api.py <br>

You can then run your API on your localhost via flask:
* flask run


### Test in Postman
![image](https://github.com/Kurayami7/Flask-Enterprise-API/assets/124408792/458326f9-eeed-4fd1-88f3-266f791aef67)

### What routes do we have access to?
- #### Gets the information for all the students in the course.
  `http://127.0.0.1:5000/all`

- #### Gets all the attendance records for all students in the course.
  `http://127.0.0.1:5000/attendance`

- #### Gets the attendance record for a particular student in the course.
  `http://127.0.0.1:5000/student_id`
