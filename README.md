# SQL-Automation-Use-of-Stored-Procedures-in-SQL
This is a project that looks into data ETL automation in SQL using stored procedures. A School DBMS is used as a case study in this project.

The InsertStudents stored procedure is designed to add new students' records into the 
students table in our students database. It provides an efficient way to insert all necessary 
information in a single operation. 
Parameters 
The parameters declared for this procedure include: 
@StudentID: This parameter is intended to store the unique identifier for each new student and 
requires string values, such as ‘S156’. 
@StudentName: This parameter stores the full name of every student and requires string 
values to be provided. 
@Gender: This stores the gender of the student 
@DOB: This stores the student’s date of birth and would require dates in standardized formats 
YYY-MM-DD. 
@ DepartmentID: This parameter specifies the identifier of the department each student 
belongs to. 
@Email: This parameter stores the student’s email address and requires string values. 
The InsertStudents procedure is run using EXEC InsertStudents by taking the values 
provided and inserting them as a new row into the Students table. 
The NewEnrollment procedure inserts a new course enrollment for a specific student on the 
Enrollments table. 
The parameters declared include: 
@EnrollmentID, @StudentID, @CourseID & @ENrollmentDate. These parameters specify 
the unique identifier for each course enrollment, the unique student and course identifier, and 
the date on which the enrollment record is created. 
The StudentsInCourse stored procedure returns a list of students enrolled in a specific course. 
The parameter declared in this procedure is the @CourseID, which serves as a reference for 
whatever CourseID is specified in the EXEC StudentsInCourse call statement. A sample call 
statement would appear like this - Exec StudentsInCourse @CourseCode = 'PSY351' and 
return an output as shown below 
The Studentstaught stored procedure returns a list of students grouped by the instructor who 
taught them. The declared parameter is @InstructorName, which serves as a reference in the 
EXEC statement to identify the instructor whose list of students should be retrieved. The 
statement Exec Studentstaught @InstructorName = 'Professor Bankole' will return the 
output below. 
The UpdateStudentMail stored procedure updates preexisting student records by inserting the 
email address for the specified student using the declared parameters @StudentID & @Email. 
The statement Exec UpdateStudentMail 'S3041', 'Wlyon@stu.edu.com' will insert the email 
provided to the student with id S3041. 
The StudentCourseEnrollment stored procedure returns a list of all courses enrolled in by a 
specific student using the parameter @StudentID.  
The call statement Exec StudentCourseEnrollment @StudentID = 'S3029' will return the 
output in the diagram below. 
The CourseEnrollment stored procedure shows a count of students enrolled in a specific 
course. The parameter declared is @StudentID, which specifies which course’s enrollment 
count should be retrieved. 
The call statement Exec CourseEnrollment @CourseID = 'Eco302' will return the output 
below. 
 
