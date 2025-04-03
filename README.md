-- Question 1: Create the student table
CREATE TABLE student (
    id INT PRIMARY KEY,
    fullName VARCHAR(100),
    age INT
);

-- Question 2: Insert at least 3 records into the student table
INSERT INTO student (id, fullName, age) VALUES (1, 'Alice Johnson', 20);
INSERT INTO student (id, fullName, age) VALUES (2, 'Bob Smith', 22);
INSERT INTO student (id, fullName, age) VALUES (3, 'Charlie Brown', 19);

