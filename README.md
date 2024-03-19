# studentCRUD

Can find demo @ the following link: https://mediaspace.carleton.ca/media/Eric+Gershtein%27s+Zoom+Meeting/1_ed4gkonn

First install required node modules by running: npm i

To run app, open command line and enter command: node app.js

Make sure that the postgres server is running. I used the following commands to set it up:

psql mydatabase

then either run the following or use the sqlinitialization file

CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    first_name TEXT NOT NULL,
    last_name TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE,
    enrollment_date DATE
);

INSERT INTO students (first_name, last_name, email, enrollment_date) VALUES ('John', 'Doe', 'john.doe@example.com', '2023-09-01'), ('Jane', 'Smith', 'jane.smith@example.com', '2023-09-01'), ('Jim', 'Beam', 'jim.beam@example.com', '2023-09-02');