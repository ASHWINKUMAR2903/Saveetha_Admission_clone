# Saveetha_Admission_clone
## Date:09.07.25

## Objective:
To design a landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS. This activity reinforces skills in layout design, form creation, user input handling, responsive structure, and visual styling based on a real-world example.

## Tasks:
#### 1. Analyze the Landing Page Layout:
Observe the split-screen layout with a promotional section on the left and a form on the right.

Note the use of background images, text styling, and branding elements.

#### 2. Create the HTML Structure:
Use semantic tags like ```<section>, <header>, <form>, and <footer>``` to organize content.

Structure the form with input fields such as name, email, phone, password, city, state, course, specialization, captcha, and checkbox.

#### 3. Add Form Functionality:
Include appropriate input types (text, email, tel, password, select, etc.) with placeholders and labels.

Use the <button> element for the "APPLY NOW" action.

#### 4. Apply CSS Styling:
Implement a split layout using flexbox or grid.

Style the form elements with padding, shadows, background colors, and rounded borders.

Include hover effects and button transitions to match the original look.

#### 5. Incorporate Images and Branding:
Add the institution logo and use matching fonts and colors.

Place a background image or blurred overlay behind the form content if needed.

#### 6. Ensure Responsiveness:
Make sure the page adapts to different screen sizes using media queries.

Maintain readability and layout integrity on both desktop and mobile.

## HTML Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saveetha Admission Enquiry</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <main class="container">
        <section class="left-section">
            <div class="branding">
                <img src="img1.jpeg" alt="Saveetha Logo" class="logo">
                <h1>Saveetha Engineering College</h1>
                <p>Affiliated to Anna University</p>
            </div>
        </section>

        <section class="form-section">
            <div class="form-border">
                <h2>Admission Enquiry Form</h2>
                <form>
                    <input type="text" placeholder="Enter Name" required>
                    <input type="email" placeholder="Enter Email" required>
                    <input type="tel" placeholder="Enter Phone Number" required>

                    <div class="radio-group">
                        <label>Gender:</label>
                        <label><input type="radio" name="gender" required> Male</label>
                        <label><input type="radio" name="gender" required> Female</label>
                    </div>

                    <label>Date of Birth:</label>
                    <input type="date" required title="Enter your date of birth" placeholder="Select Date of Birth">

                    <label for="department">Department Interested:</label>
                    <select id="department" required>
                        <option value="">Select Department</option>
                        <option value="CSE">CSE</option>
                        <option value="ECE">ECE</option>
                        <option value="MECH">MECH</option>
                        <option value="IT">IT</option>
                    </select>

                    <input type="text" placeholder="Enter State" required>
                    <input type="text" placeholder="Enter City" required>

                    <div class="checkbox-group">
                        <label>Preferred Mode of Contact:</label>
                        <label><input type="checkbox" name="contact"> Phone</label>
                        <label><input type="checkbox" name="contact"> Email</label>
                    </div>

                    <button type="submit">APPLY NOW</button>
                    <button type="reset">Clear Form</button>
                </form>
            </div>
        </section>
    </main>
</body>
</html>
```
## CSS Code:
```
* {
    box-sizing: border-box;
    margin: 0;  
    padding: 0;
    font-family: Arial, sans-serif;
}
body {
    background-color: #ffffff;
    color: #fff;
    background: url("img2.webp") no-repeat center center fixed;
    background-size: cover;
}

.left-section {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px;
    color: white;
}
.left-section .logo {
    width: 100px;
    margin-bottom: 20px;
}
.left-section h1 {
    font-size: 2rem;
    margin-bottom: 10px;
}
.left-section p {
    font-size: 1.2rem;
}

.form-section {
    flex: 1;
    background-color: rgba(23, 37, 42, 0.8); /* adds slight transparency */
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px;
}

.form-border {
    width: 100%;
    max-width: 500px;
    background-color: #1f3a47;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.3);
}
.form-border h2 {
    text-align: center;
    margin-bottom: 20px;
}
form input,
form select,
form button {
    width: 100%;
    padding: 10px;
    margin-top: 10px;
    border-radius: 5px;
    border: none;
}
form input,
form select {
    background-color: #0d1b2a;
    color: #fff;
}

form input[type="radio"],
form input[type="checkbox"] {
    width: auto;
    margin-right: 8px;
}
.radio-group,
.checkbox-group {
    margin: 10px 0;
}
form label {
    display: block;
    margin-top: 15px;
    margin-bottom: 5px;
    color: #eee;
}
form button {
    background-color: #007bff;
    color: #fff;
    margin-top: 15px;
    transition: background-color 0.3s ease;
}
form button:hover {
    background-color: #0056b3;
}

@media (max-width: 768px) {
    .container {
        flex-direction: column;
    }
    .left-section, .form-section {
        flex: unset;
        width: 100%;
    }
    .left-section {
        padding: 20px;
    }
}
```
## Output:
![image](https://github.com/user-attachments/assets/1d7d62da-1811-4734-ab6d-9dfebc4d244c)

## Result:
A landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS is designed successfully.
