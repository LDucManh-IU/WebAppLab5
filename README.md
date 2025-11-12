STUDENT INFORMATION:<br>
Student name: Lưu Đức Mạnh <br>
Student ID: ITITIU23016 <br>

<hr>
LAB REPORT

<hr>

ADD:
(1) User access list page: student-list.jsp through student?action=list<br>
(2) User select "Add new student" button -> Url change to  student?action=new <br>
(3) StudentController.java read "action=new" -> call function showNewForm() -> direct to sdudent-form.jsp <br>
(4) User fill the form -> submit (method = POST) -> form sent to "student?action =insert"
(5) doPost() read action -> call funtuction insertStudent() -> Get data from form -> create new Student newStudent -> call DAO <br>
(6) DAO call addStudent() -> Insert to database (INSERT INTO students (student_code, full_name, email, major) VALUES)<br>
(7) Success -> redirect (response.sendRedirect("student?action=list&message=Student added successfully");)'
(8) View list after change + success message

<hr>

EDIT:


