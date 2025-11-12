STUDENT INFORMATION:<br>
Student name: Lưu Đức Mạnh <br>
Student ID: ITITIU23016 <br>

<hr>
LAB REPORT

<hr>

ADD:
<br>
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
<br>
(1) User choose edit -> change URL to student?action=edit&id=[]
(2) Controller read action -> call showEditForm()
(3) DAO get student object from DB (getStudentById(id))
(4) Controller setAttribute("student", data) → forward → student-form.jsp displays form with old data (Student Code usually readonly)
(5) User edits → submit(POST) → (student?action=update)
(6) updateStudent() get data -> set attribute to object -> call DAO
(7) DAO → updateStudent() → UPDATE UPDATE students SET ... WHERE id = ?
(8) Redirect to list + message (student?action=list&message=Student updated successfully)
(9) Display list

<hr>

DELETE
<br>
(1) User choose delete -> confirm -> send request (student?action=delete&id=[])
(2) Controller call deleteStudent()
(3) DAO → deleteStudent(id) DELETE FROM students WHERE id = ?
(4) Redirect to list (GET) through student?action=list&message=Student deleted successfully
(5) View displays the new list
