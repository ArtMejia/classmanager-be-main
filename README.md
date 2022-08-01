
# Class Manager Api

This repo contains the Java Springboot Api for the React + Java 
instruction for careerdevs ch 15.

## Run Locally

to run locally 
1. download (or clone) the repo.
2. Install MySql
3. Open MySql and create the classroom database
4. create a user with full access to the database (see sql scripts for help)
5. update the application.properties file with the user and password you set 
6. load the project in intellij
7. go to: `src/main/java/ch15.classroom.demo/DemoApplication`
8. click on the green play button on line 9 (my need to let the app load a bit first).
9. confirm the application works by using postman to check the following GET routes:

* `http://localhost:8080/api/schools/`
* `http://localhost:8080/api/teachers`
* `http://localhost:8080/api/students/teacher/1`

### sql scripts
```
CREATE DATABASE classroom;
CREATE USER "classManager"@"%" identified by "schoolrules";
GRANT ALL ON classroom.* to "classManager"@"%";
```

## React requirements
1. install nodejs (nodejs.org) LTS
2. check that the follow commands do not give `command not found` errors
```shell
node --version
npm --version
npx --version
```

# Back End
1. back end can get a student by id
2. get a list of students by their teacher id
3. get a list of students by their school id
4. create a studen and assign them to a school and teacher
5. submit a payment using student id and payFees route

6. get a teacher by their id
7. get a list of teacher by their school id
8. create a teacher and assign them a school id
9. delete a teacher using their id

10. test route using /test route
11. get a list of schools
12. get school by id
13. create a school

# Front End
1. student can go to homepage using navigation bar
2. student can login using login route/page
3. sign in using student id, password can be anything
4. once signed in, student can see list of students and grade using directory
5. see their own profile (profile currently blank for all)
6. submit payment using payfees route
