# NF

Department(ID, head)
Teacher(PD, masterDepID, departmentID, sumValueUnits)
Student(PD, departmentID, class, function,siblingID,semMark,yearMark)
Parents(PD, studentID,nameChild)
Class(ID, Dep, curriculumID)
Subject(ID, semester,extent, teacher,curriculumID,compulsoryGrp)
Curriculum(ID, formEdu, class, subject)



## Assos

Teacher-1---n-Teacher_educate_Student-n---1-Student
key1:TeacherID
key2:SudentID

Teacher-1---n-Teacher_give_Class-n---1-Class
key1: TeacherID
key2: ClassID

Parent-1---n-Parent_gaveBirth_Student-n---1-Student
key1:ParentID
key2: StudentID

Teacher-1---n-Teacher_specialized_Subject-n---1-Subject
key1:TeacherID
key2:SubjectID

Teacher-1---n-Teacher_teachAt_Department-1---n-Department
