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
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Saveetha Admissions Clone</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <div class="left">
      <div class="branding">
        <img src="img1.jpeg" alt="Saveetha Logo" />
        <h2>SAVEETHA ENGINEERING COLLEGE</h2>
        <h4>Affiliated to Anna University</h4>
        <h1>INDUSTRY 5.0</h1>
        <p>Ready Curriculum Imparting <br/> 21st Century Skills</p>
        <button class="promo-btn">Apply Now <i class="fa fa-angle-down"></i></button>
      </div>
    </div>

    <div class="right">
      <form class="form-box">
        <h2>Admissions Open 2025</h2>

        <div class="input-group">
          <i class="fa fa-user"></i>
          <input type="text" placeholder="Enter Name *" required />
        </div>

        <div class="input-group">
          <i class="fa fa-envelope"></i>
          <input type="email" placeholder="Enter Email Address *" required />
        </div>

        <div class="input-group">
          <i class="fa fa-phone"></i>
          <input type="tel" placeholder="Enter Mobile Number *" required />
        </div>

        <div class="input-group">
          <i class="fa fa-lock"></i>
          <input type="password" placeholder="Any Password of Your Choice *" required />
        </div>

        <div class="input-pair">
          <input type="text" placeholder="State *" required />
          <input type="text" placeholder="City *" required />
        </div>

        <div class="input-pair">
          <select required>
            <option value="">Course *</option>
            <option value="CSE">CSE</option>
            <option value="ECE">ECE</option>
            <option value="MECH">MECH</option>
            <option value="IT">IT</option>
          </select>
          <select required>
            <option value="">Specialization *</option>
            <option value="AI">AI</option>
            <option value="DS">Data Science</option>
            <option value="Robotics">Robotics</option>
          </select>
        </div>
        <label class="terms">
          <input type="checkbox" required />
          I agree for the above details and concern
        </label>
        <button class="apply-btn" type="submit">APPLY NOW <i class="fa fa-arrow-right"></i></button>
      </form>
    </div>
  </div>
</body>
</html>

```
## CSS Code:
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", sans-serif;
}

body {
  background: url("img2.webp") no-repeat center center fixed;
  background-size: cover;
  color: white;
}

.container {
  display: flex;
  height: 100vh;
  width: 100%;
  backdrop-filter: blur(3px);
}

.left {
  flex: 1;
  background-color: rgba(0, 0, 0, 0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 30px;
}
.branding {
  text-align: left;
  color: #fff;
}
.branding img {
  width: 80px;
  margin-bottom: 10px;
}
.branding h2 {
  font-size: 22px;
  font-weight: bold;
}
.branding h4 {
  background-color: yellow;
  display: inline-block;
  padding: 3px 10px;
  margin: 10px 0;
  color: #000;
}
.branding h1 {
  font-size: 38px;
  color: #ffc107;
  margin: 20px 0 10px;
}
.branding p {
  font-size: 18px;
  line-height: 1.5;
}
.promo-btn {
  margin-top: 20px;
  padding: 10px 25px;
  background-color: #ffc107;
  color: black;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.right {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.form-box {
  background-color: rgba(0, 0, 0, 0.85);
  padding: 30px 30px;
  border-radius: 12px;
  max-width: 450px;
  width: 100%;
}
.form-box h2 {
  text-align: center;
  margin-bottom: 20px;
}

.input-group {
  position: relative;
  margin-bottom: 15px;
}
.input-group i {
  position: absolute;
  top: 12px;
  left: 10px;
  color: gray;
}
.input-group input {
  width: 100%;
  padding: 10px 10px 10px 35px;
  border: none;
  border-radius: 5px;
  background-color: #1e1e1e;
  color: white;
}
.input-group input::placeholder {
  color: #aaa;
}

.input-pair {
  display: flex;
  gap: 10px;
  margin-bottom: 15px;
}
.input-pair input,
.input-pair select {
  flex: 1;
  padding: 10px;
  border-radius: 5px;
  background-color: #1e1e1e;
  border: none;
  color: white;
}
.input-pair select option {
  background-color: white;
  color: black;
}

.terms {
  font-size: 12px;
  margin: 10px 0;
  display: block;
  color: #ddd;
}

.apply-btn {
  width: 100%;
  padding: 12px;
  background-color: #ffc107;
  color: black;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
.apply-btn i {
  margin-left: 8px;
}

/* Responsive */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
  .left, .right {
    flex: none;
    width: 100%;
  }
  .left {
    padding: 20px;
  }
}
```
## Output:
![image](https://github.com/user-attachments/assets/ea0f9770-b2fd-4edb-b35d-c18b93f036ac)

## Result:
A landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS is designed successfully.
