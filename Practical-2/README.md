# Practical No. 2

## Aim
To create a student registration form using HTML form tags.

## Problem Definition
To design a simple student registration form using HTML input elements such as text fields, radio buttons, dropdown lists, textarea, checkbox, submit, and reset buttons.

## Theory
HTML forms are used to collect information from users on a web page. The `<form>` tag acts as a container for different input elements. Text fields are used to enter details such as name, roll number, email, and phone number. Radio buttons allow users to select one option, while checkboxes are used for confirmation. The `<select>` and `<option>` tags create dropdown menus, and the `<textarea>` tag is used for longer text such as an address. Submit and reset buttons help users send or clear the entered data. Forms are widely used for registration and data collection.

## Procedure and Execution

### Step for Implementation
1. Open a text editor such as VS Code, Notepad, or Sublime Text.
2. Create a new file and save it as `index.html`.
3. Write the basic HTML structure using `<html>`, `<head>`, and `<body>` tags.
4. Add a heading using the `<h2>` tag.
5. Create the registration form using the `<form>` tag.
6. Add fields for name, roll number, email, password, phone number, and date of birth.
7. Add gender options using radio buttons.
8. Add department and semester using `<select>` and `<option>` tags.
9. Add an address field using the `<textarea>` tag and confirmation using a checkbox.
10. Add Register and Reset buttons, save the file, and open it in a web browser.

### Code

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Student Registration Form</title>
</head>

<body>

    <h2>Student Registration Form</h2>

    <form>

        Name: <br>
        <input type="text" id="name">
        <br><br>

        Roll Number: <br>
        <input type="text" id="roll">
        <br><br>

        Email: <br>
        <input type="email" id="email">
        <br><br>

        Password: <br>
        <input type="password" id="password">
        <br><br>

        Phone Number: <br>
        <input type="text" id="phone">
        <br><br>

        Date of Birth: <br>
        <input type="date" id="dob">
        <br><br>

        Gender: <br>
        <input type="radio" name="gender"> Male
        <input type="radio" name="gender"> Female
        <br><br>

        Department: <br>
        <select id="department">
            <option>Select Department</option>
            <option>CSE</option>
            <option>IT</option>
            <option>ECE</option>
            <option>Mechanical</option>
        </select>
        <br><br>

        Semester: <br>
        <select id="semester">
            <option>Select Semester</option>
            <option>Semester 1</option>
            <option>Semester 2</option>
            <option>Semester 3</option>
            <option>Semester 4</option>
        </select>
        <br><br>

        Address: <br>
        <textarea></textarea>
        <br><br>

        <input type="checkbox">
        I confirm that the above information is correct.
        <br><br>

        <input type="submit" value="Register">
        <input type="reset" value="Reset">

    </form>

</body>

</html>
```

## Output Analysis
The student registration form was successfully created and displayed in the web browser. It contains fields for name, roll number, email, password, phone number, date of birth, gender, department, semester, and address. Radio buttons are used for gender selection, dropdown lists are used for department and semester, and a checkbox is provided for confirmation. The Register and Reset buttons are also displayed correctly.

## Conclusion
In this practical, I learned how to create a student registration form using HTML form tags. I used text fields, radio buttons, dropdown lists, textarea, checkbox, submit, and reset buttons. This practical helped me understand how different HTML form elements are used to collect information from users on a web page.
