# Practical No. 4A

---

## Aim

Introduction to JavaScript using Loop, Conditional Statements, and Form Validation.

---

## Problem Definition

Build a registration form containing student details such as name, email, password, phone number, roll number, department, and semester. Use JavaScript to validate the entered information when the user submits the form and display suitable alert messages for incorrect input.

---

## Theory

JavaScript is a scripting language used to make web pages interactive and dynamic. Conditional statements such as `if`, `else if`, and `else` are used to make decisions based on different conditions. Loops such as `for`, `while`, and `do-while` are used to repeat a block of code multiple times. Form validation is used to check whether the information entered by the user is correct before submitting the form. JavaScript can validate fields such as name, email, password, and phone number. If any field contains invalid or empty data, an error message is displayed to the user.

---

## Procedure and Execution

### Step for Implementation

1. Create an HTML registration form.
2. Add Name, Roll Number, Email, and Mobile Number fields.
3. Add Date of Birth and Gender fields.
4. Add Department and Semester dropdown lists.
5. Add Programming Language checkboxes.
6. Add Address, Password, and Confirm Password fields.
7. Add a Register button.
8. Write a JavaScript `validateForm()` function.
9. Use conditional statements to validate entered values.
10. Display alert messages for invalid input.
11. Apply basic CSS for simple form styling.
12. Open the HTML file in a web browser and test the form.

---

# Code

## HTML File - `index.html`

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Computer Student Registration Form</title>

    <link rel="stylesheet" href="Practicle_4.css">
</head>

<body>

<div class="container">

    <form onsubmit="return validateForm()" id="studentForm">

        <h2>Computer Science Student Registration</h2>

        <div class="input-box">
            <label>Full Name</label>
            <input type="text" id="name" placeholder="Enter your name">
        </div>

        <div class="input-box">
            <label>Roll Number</label>
            <input type="text" id="roll" placeholder="Enter Roll Number">
        </div>

        <div class="input-box">
            <label>Email</label>
            <input type="email" id="email" placeholder="Enter Email">
        </div>

        <div class="input-box">
            <label>Mobile Number</label>
            <input type="tel" id="mobile" placeholder="Enter Mobile Number">
        </div>

        <div class="input-box">
            <label>Date of Birth</label>
            <input type="date" id="dob">
        </div>

        <div class="input-box">

            <label>Gender</label><br>

            <label>
                <input type="radio" name="gender" value="Male">
                Male
            </label>

            <label>
                <input type="radio" name="gender" value="Female">
                Female
            </label>

            <label>
                <input type="radio" name="gender" value="Other">
                Other
            </label>

        </div>

        <div class="input-box">

            <label>Department</label>

            <select id="department">

                <option value="">Select Department</option>
                <option>Computer Technology</option>
                <option>Computer Engineering(IOT)</option>
                <option>Computer Engineering</option>
                <option>Information Technology</option>
                <option>Artificial Intelligence</option>
                <option>Data Science</option>
                <option>Cyber Security</option>

            </select>

        </div>

        <div class="input-box">

            <label>Semester</label>

            <select id="semester">

                <option value="">Select Semester</option>
                <option>Semester I</option>
                <option>Semester II</option>
                <option>Semester III</option>
                <option>Semester IV</option>
                <option>Semester V</option>
                <option>Semester VI</option>

            </select>

        </div>

        <div class="input-box">

            <label>Programming Languages</label><br>

            <label>
                <input type="checkbox"> C
            </label>

            <label>
                <input type="checkbox"> C++
            </label>

            <label>
                <input type="checkbox"> Java
            </label>

            <label>
                <input type="checkbox"> Python
            </label>

            <label>
                <input type="checkbox"> JavaScript
            </label>

        </div>

        <div class="input-box">

            <label>Address</label>

            <textarea id="address" rows="4"></textarea>

        </div>

        <div class="input-box">

            <label>Password</label>

            <input type="password" id="password">

        </div>

        <div class="input-box">

            <label>Confirm Password</label>

            <input type="password" id="confirmPassword">

        </div>

        <button type="submit">Register</button>

    </form>

</div>

<script src="Practicle_4.js"></script>

</body>

</html>
```

---

## JavaScript File - `Practicle_4.js`

```javascript
function validateForm(){

    let name = document.getElementById("name").value.trim();

    let roll = document.getElementById("roll").value.trim();

    let email = document.getElementById("email").value.trim();

    let mobile = document.getElementById("mobile").value.trim();

    let department = document.getElementById("department").value;

    let semester = document.getElementById("semester").value;

    let password = document.getElementById("password").value;

    let confirmPassword =
        document.getElementById("confirmPassword").value;


    if(name == ""){

        alert("Please enter your name.");

        return false;
    }


    if(roll == ""){

        alert("Please enter Roll Number.");

        return false;
    }


    if(email == ""){

        alert("Please enter Email.");

        return false;
    }


    if(mobile.length != 10){

        alert("Mobile number should contain 10 digits.");

        return false;
    }


    if(department == ""){

        alert("Select Department.");

        return false;
    }


    if(semester == ""){

        alert("Select Semester.");

        return false;
    }


    if(password.length < 6){

        alert("Password must contain at least 6 characters.");

        return false;
    }


    if(password !== confirmPassword){

        alert("Passwords do not match.");

        return false;
    }


    alert("Registration Successful!");

    return false;
}
```

---

## CSS File - `Practicle_4.css`

```css
body {

    font-family: Arial, sans-serif;

    background-color: #f2f2f2;
}


form {

    width: 400px;

    margin: 30px auto;

    background-color: white;

    padding: 20px;

    border: 1px solid black;
}


h2 {

    text-align: center;
}


label {

    font-weight: bold;
}


input,
select,
textarea {

    width: 100%;

    padding: 8px;

    margin-top: 5px;

    box-sizing: border-box;
}


input[type="radio"],
input[type="checkbox"] {

    width: auto;
}


button {

    padding: 10px 20px;

    background-color: blue;

    color: white;

    border: none;

    cursor: pointer;
}


button:hover {

    background-color: darkblue;
}
```

---

## Output Analysis

The registration form accepts student details such as name, roll number, email, mobile number, department, semester, password, and other information. When the user clicks the Register button, JavaScript checks the entered values. If any required field is empty or contains incorrect data, an alert message is displayed. The mobile number must contain 10 digits and the password must contain at least 6 characters. The password and confirm password must also match. If all details are entered correctly, the message **"Registration Successful!"** is displayed. Thus, JavaScript helps validate user input before form submission.

---

## Conclusion

In this practical, I learned how JavaScript can be used for form validation. I learned how to access HTML elements using `getElementById()` and use conditional statements to check the entered values. JavaScript checks fields such as name, roll number, email, mobile number, department, semester, and password before registration. It also displays suitable alert messages when incorrect data is entered. This practical helped me understand how JavaScript makes web forms interactive, validates user input, and improves the reliability of web applications.
