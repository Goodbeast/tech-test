# Our hiring test.

## Instructions

Read each question carefully.  Each question specifies how to deliver the
requested solution; please follow these instructions carefully as they are
part of the question.  When something is requested by URL, it's fine to host
on a hidden page of your portfolio, or use CodePen, or any other hosting solution
as long as it's on a publicly accessible URL.

When you're finished, please return the test via email.  There's no need to
clone or fork this repository.

## Question 1: The Box
Recreate the image below using valid HTML and CSS or SASS. Please provide a URL
to your solution in your follow up email.

![boxtest](box.png)

## Question 2: Vue Temp
Using Vue.js, create a form that converts between Centigrade and Fahrenheit.
Please provide a URL to your solution in your follow up email.

- The page should have two fields, one labeled Fahrenheit and one labeled Centigrade.
- When one field is changed, it should update the other value.
- The default value when the page loads should be 20C.
- While you can't fail this question for having an unattractive form, tidiness and cleanliness of code and interface will be noted.


## Question 3: SQL
Create a SQL query that returns the username, full name (Last Name, First Name)
and last login date and time based on the following tables. Please include your
query in your follow up email.

- The fields returned should be labeled username, full_name, last_login
- Each user should appear once in the result set
- Remember to include the user who has never logged in.
- The SQL below is designed and tested using MySQL.

```
CREATE TABLE users(
username VARCHAR(32) NOT NULL,
password VARCHAR(32) NOT NULL,
first_name VARCHAR(255) NOT NULL,
last_name VARCHAR(255),
PRIMARY KEY (`username`));

CREATE TABLE logins (
username VARCHAR(32) NOT NULL,
last_login TIMESTAMP,
FOREIGN KEY (`username`) REFERENCES users(`username`));

INSERT INTO users
VALUES
('bob','9f9d51bc70ef21ca5c14f307980a29d8','Bob','Smith'),
('joe','8ff32489f92f33416694be8fdc2d4c22','Joe','Smith'),
('jane','5844a15e76563fedd11840fd6f40ea7b','Jane','Smith'),
('matt','ce86d7d02a229acfaca4b63f01a1171b','Matt','Smith');

INSERT INTO logins
VALUES
('bob','2011-01-02 06:42:15'),
('bob','2011-01-12 13:42:15'),
('jane','2011-01-02 08:42:15'),
('matt','2011-01-13 09:42:15'),
('jane','2011-01-14 12:42:15');

  ```
