# 🎂 Age Eligibility Checker — JavaScript Input & Conditional Logic

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Task-5-6D28D9?style=for-the-badge" alt="Task 5">
</p>

<p align="center">
  <b>✨ Take Input • Apply Logic • Display Results ✨</b>
</p>

<p align="center">
  A beginner-friendly web project that uses HTML, CSS and JavaScript to check
  voting eligibility based on age, with input validation and an interactive interface.
</p>

---

## 📌 About The Project

**Age Eligibility Checker** is a simple frontend project created to practice JavaScript input methods and conditional statements.

The webpage asks the user to enter their age and checks whether they are eligible to vote using an age threshold of **18 years**. HTML provides the structure, CSS styles the interface, and JavaScript handles input, validation and the result.

The project demonstrates `prompt()`, `alert()`, `document.write()`, `if-else`, the ternary operator and DOM manipulation.

> 💡 **"Learn the logic, write the code, and turn every concept into a project."**

---

## 🎯 Project Goals

The main purpose of this project is to practice and demonstrate:

- 🧱 Creating a webpage using HTML
- 🎨 Styling the page using CSS
- ⌨️ Taking user input using `prompt()`
- 🔔 Displaying popup messages using `alert()`
- 🧠 Applying `if-else` conditional logic
- 🔀 Using the ternary operator (`? :`)
- 🖥️ Displaying results with DOM manipulation
- ✅ Validating the entered age
- 📝 Understanding the use of `document.write()`

---

## 🖥️ Website Preview

The webpage contains a centered checker card with a heading, short instruction, button and result area.

```text
┌─────────────────────────────────────────┐
│                                         │
│          AGE ELIGIBILITY CHECKER         │
│                                         │
│   Check whether you are eligible to     │
│              vote based on age.         │
│                                         │
│          [ Check Eligibility ]           │
│                                         │
│          Your Age: 20                    │
│       You are eligible to vote.          │
│                                         │
└─────────────────────────────────────────┘
```

The design uses a dark gradient background, a white card, rounded corners and a button hover effect.

---

# ✨ Key Features

## 🎂 1. Age Input

The program asks the user to enter their age through the browser's `prompt()` dialog.

```javascript
let age = prompt("Enter your age:");
```

## ✅ 2. Voting Eligibility Check

The program uses `if-else` to check whether the entered age is 18 or above.

- Age **18 or above** — eligible to vote
- Age **below 18** — not eligible to vote yet

## ⚠️ 3. Input Validation

The program handles invalid input, including:

- Empty input
- Negative age
- Non-numeric input
- Decimal age
- Cancelled prompt

## 🔔 4. Alert Messages

The `alert()` method displays the eligibility result or an input error message.

## 🖥️ 5. Result on the Webpage

The result area is updated using `document.getElementById()` and `innerHTML`.

## 🎨 6. CSS Styling

The interface includes:

- Dark gradient background
- Centered white card
- Rounded corners
- Box shadow
- Styled button
- Hover transition
- Responsive card width

---

# 🧠 JavaScript Concepts Demonstrated

## 1️⃣ `prompt()`

`prompt()` opens a dialog box and takes input from the user.

```javascript
let age = prompt("Enter your age:");
```

## 2️⃣ `alert()`

`alert()` displays a message in a popup dialog box.

```javascript
alert("You are eligible to vote!");
```

## 3️⃣ `if-else`

The `if-else` statement checks the user's age.

```javascript
if (age >= 18) {
    alert("You are eligible to vote!");
} else {
    alert("You are not eligible to vote yet.");
}
```

## 4️⃣ Ternary Operator

The ternary operator chooses one of two messages based on a condition.

```javascript
let message = age >= 18
    ? "You are eligible to vote."
    : "You are not eligible to vote yet.";
```

## 5️⃣ DOM Manipulation

The webpage result is updated using the DOM.

```javascript
document.getElementById("result").innerHTML =
    "Your Age: " + age + "<br>" + message;
```

## 6️⃣ `document.write()`

The project includes a commented example of `document.write()`.

```javascript
// document.write("Your age is " + age);
```

> ⚠️ Calling `document.write()` after a webpage has loaded can replace the current document. For this reason, the example remains commented out and the actual result is displayed through DOM manipulation.

---

# 💻 Complete Source Code

Create a file named **`index.html`** and paste the complete code below. HTML, CSS and JavaScript are included in the same file.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Age Eligibility Checker</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #141e30, #243b55);
            color: white;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            background-color: white;
            color: #222;
            width: 90%;
            max-width: 450px;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
        }

        h1 {
            color: #243b55;
            margin-bottom: 15px;
        }

        p {
            margin-bottom: 20px;
            line-height: 1.6;
        }

        button {
            background-color: #243b55;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
        }

        button:hover {
            background-color: #141e30;
            transform: scale(1.05);
        }

        #result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            overflow-wrap: anywhere;
        }
    </style>
</head>

<body>

    <div class="container">
        <h1>Age Eligibility Checker</h1>

        <p>
            Check whether you are eligible to vote
            based on your age.
        </p>

        <button onclick="checkAge()">Check Eligibility</button>

        <div id="result"></div>
    </div>

    <script>
        function checkAge() {

            // User se age input lena
            let age = prompt("Enter your age:");

            // Agar user Cancel dabaye
            if (age === null) {
                alert("You cancelled the process.");
                return;
            }

            age = age.trim();

            // Empty ya invalid input check karna
            if (age === "" || !Number.isFinite(Number(age))
                || Number(age) < 0
                || !Number.isInteger(Number(age))) {

                alert("Please enter a valid age.");
                document.getElementById("result").innerHTML =
                    "Invalid age entered.";
                return;
            }

            age = Number(age);

            // If-else se eligibility check karna
            if (age >= 18) {
                alert("You are eligible to vote!");
            } else {
                alert("You are not eligible to vote yet.");
            }

            // Ternary operator ka use
            let message = age >= 18
                ? "You are eligible to vote."
                : "You are not eligible to vote yet.";

            // Page par result show karna
            document.getElementById("result").innerHTML =
                "Your Age: " + age + "<br>" + message;

            // document.write() ka demonstration
            // Isko uncomment karne par current page replace ho jayega.
            // document.write("Your age is " + age);
        }
    </script>

</body>
</html>
```

---

# 🧪 Sample Test Cases

| Input | Expected Result |
|---|---|
| `20` | Eligible to vote |
| `18` | Eligible to vote |
| `17` | Not eligible to vote yet |
| `0` | Not eligible to vote yet |
| `-5` | Invalid age |
| `abc` | Invalid age |
| Empty input | Invalid age |
| `18.5` | Invalid age |
| Cancel in prompt | Process cancelled |

---

# 📂 Project Structure

Keep the files together in the same project folder.

```text
📁 TASK-5
│
├── 📄 index.html
└── 📘 README.md
```

The `index.html` file contains the HTML structure, CSS styling and JavaScript logic. The `README.md` file explains the project and contains the complete source code.

---

# 🛠️ Technologies Used

<p>
  <img src="https://img.shields.io/badge/HTML5-Structure-orange?style=flat-square&logo=html5" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-Styling-blue?style=flat-square&logo=css3" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-Logic-yellow?style=flat-square&logo=javascript" alt="JavaScript">
</p>

| Technology | Used For |
|---|---|
| 🧱 **HTML5** | Defines the webpage structure |
| 🎨 **CSS3** | Styles the card, background and button |
| ⚙️ **JavaScript** | Handles input, validation and eligibility logic |
| 🌐 **Web Browser** | Runs and tests the webpage |

---

# 🚀 How To Run The Project

### Step 1 — Create the project folder

Create a folder named `TASK-5`.

### Step 2 — Create the HTML file

Create a file named `index.html` inside the folder.

### Step 3 — Add the code

Paste the complete source code into `index.html` and save it.

### Step 4 — Open the webpage

Open `index.html` in a modern web browser.

You can use:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Brave
- Opera

### Step 5 — Test the checker

Click **Check Eligibility**, enter an age and view the result.

No additional libraries or installations are required.

---

# 🧪 What I Practiced From This Project

### JavaScript Concepts

- ✅ `prompt()`
- ✅ `alert()`
- ✅ `document.write()`
- ✅ `if-else`
- ✅ Ternary operator
- ✅ `Number()` conversion
- ✅ Input validation
- ✅ DOM manipulation
- ✅ `innerHTML`
- ✅ Functions and return statements

### HTML & CSS Concepts

- ✅ HTML document structure
- ✅ Buttons and `onclick`
- ✅ `div` containers
- ✅ CSS selectors
- ✅ Flexbox alignment
- ✅ Gradients
- ✅ Padding and margins
- ✅ Border radius
- ✅ Box shadow
- ✅ Hover effects
- ✅ Responsive width

---

# 🧠 How The Program Works

```text
Start
  ↓
Click "Check Eligibility"
  ↓
Enter Age using prompt()
  ↓
Validate the input
  ↓
Is the age valid?
  ├── No → Show error message
  │
  └── Yes
        ↓
     Is age >= 18?
        ├── Yes → Eligible to vote
        └── No  → Not eligible yet
        ↓
     Display result on webpage
```

---

# 🌟 Why This Project Matters

This project combines basic JavaScript concepts into one practical example. It helps demonstrate how a program can accept user input, validate data, make decisions and display a result.

```text
User Input
    ↓
Input Validation
    ↓
Conditional Logic
    ↓
Result Message
    ↓
Interactive Webpage
```

The project provides a foundation for learning more JavaScript topics and building interactive frontend applications.

---

# 🔮 Future Improvements

This project can be improved further by:

- [ ] Adding a visible age input field
- [ ] Adding separate success and error message styles
- [ ] Separating HTML, CSS and JavaScript into individual files
- [ ] Adding keyboard accessibility
- [ ] Improving form validation
- [ ] Adding more eligibility categories
- [ ] Deploying the webpage using GitHub Pages

---

# 🤝 Contributions

This project is created for learning and practice. You can experiment with the code, change the design and add new features to improve your understanding of HTML, CSS and JavaScript.

---

# 📜 License

This project is intended for **educational and learning purposes**.

---

# ❤️ Final Note

> **"Practice turns concepts into skills, and projects turn skills into experience."**

Keep learning.  
Keep experimenting.  
Keep building.

### ✨ Learn • Code • Create • Repeat.

---

## 👩‍💻 Author

**Garima**

🎓 Student  
💻 Learning HTML, CSS & JavaScript  
🚀 Building projects and improving one step at a time

---

<p align="center">
  <b>⭐ If you found this project useful, consider giving the repository a star!</b>
</p>

<p align="center">
  Made with ❤️ using HTML, CSS & JavaScript
</p>
