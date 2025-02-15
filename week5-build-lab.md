# Week 5 Build Lab

**Due Date:** End of Week 5 Sunday 11:59 PM  
**Points:** 50  
**Submission Format:** Your HTML, CSS, and Javascript code and any supporting files. A screen shot or screen recording of it working is perfectly acceptable and makes it easy for me to check that you are doing well.


### Learning Objectives
- Extend your Week 4 webpage with **basic, practical JavaScript** to introduce dynamic behavior and user interaction.  
- Learn how to **manipulate the DOM** (Document Object Model) by showing/hiding elements or updating content on the page.  

---

## Overview

In this lab, you’ll:

1. **Copy your Week 4 project** (HTML & CSS) into a new folder named `week5_js_lab`.  
2. **Add a JavaScript file**, then link it to your HTML.  
3. Use **simple JavaScript** to toggle the visibility of an element, demonstrating how to respond to user actions (e.g., a button click) and update the page in real time.

---

## Step-by-Step Instructions

1. **Create a New Folder**  
   - Make a folder named `week5_js_lab`.  
   - Copy your `index.html` and `styles.css` from Week 4 into this new folder.

2. **Add a JavaScript File**  
   - In `week5_js_lab`, create a new file named `script.js`.

3. **Link the JavaScript in `index.html`**  
   - Just before the closing `</body>` tag in your HTML, add:

     ```html
     <!-- Link to our custom JavaScript file -->
     <script src="script.js"></script>
     ```

4. **Add an Interactive Button**  
   - In your `index.html`, choose a place where you want a user to click a button (e.g., near the “Fun Fact” aside or in a separate section).  
   - Example: Right under the `<h3>Fun Fact</h3>` in the aside, add a new button with an `id` so we can reference it in JavaScript:

     ```html
     <aside id="fun-fact-aside">
       <h3>Fun Fact</h3>
       <p>I once traveled to three countries in a single month!</p>
       <!-- NEW BUTTON to toggle the aside visibility -->
       <button id="toggle-fact-btn">Toggle Fun Fact</button>
     </aside>
     ```

5. **Write Basic JavaScript (in `script.js`)**  
   - We’ll toggle the aside’s visibility whenever the button is clicked. Add this code to `script.js`:

     ```js
     // DOMContentLoaded ensures the script runs after the HTML is fully parsed
     document.addEventListener("DOMContentLoaded", () => {
       // Select the button and the aside
       const toggleBtn = document.getElementById("toggle-fact-btn");
       const funFactAside = document.getElementById("fun-fact-aside");

       // Attach a click event listener to the button
       toggleBtn.addEventListener("click", () => {
         // Check current display style and toggle
         if (funFactAside.style.display === "none") {
           funFactAside.style.display = "block";
         } else {
           funFactAside.style.display = "none";
         }
       });
     });
     ```

   - **Explanation** (feel free to add these as code comments in `script.js`):  
     - We wait for `DOMContentLoaded` to ensure the HTML elements are loaded before we access them.  
     - `document.getElementById("toggle-fact-btn")` selects the button.  
     - `document.getElementById("fun-fact-aside")` selects the aside.  
     - On `toggleBtn.addEventListener("click", ...)`, we run a function that checks if `funFactAside` is currently hidden. If so, we show it; otherwise, we hide it.

6. **Try It Out**  
   - **Open `index.html` in your browser**.  
   - Click the “Toggle Fun Fact” button. The aside should hide or show depending on its current state.  
   - Resize the page to confirm your previous CSS media queries (Week 4) still work.

7. **Further Enhancements (Optional)**  
   - Style your button in `styles.css` for better aesthetics:

     ```css
     #toggle-fact-btn {
       background-color: #0066cc;
       color: #fff;
       border: none;
       padding: 0.5rem 1rem;
       cursor: pointer;
       margin-top: 1rem;
     }
     #toggle-fact-btn:hover {
       background-color: #005bb5;
     }
     ```

   - Add a **console.log** statement inside your click function to practice debugging or learn about the JavaScript console:

     ```js
     console.log("Toggle button was clicked!");
     ```

   - Use JavaScript to **change text** on the button from “Hide Fun Fact” to “Show Fun Fact” when toggling.

---

## Example Files

Below is a **complete sample** based on the Week 4 structure. Simply copy/paste into your `week5_js_lab` folder. Adjust text, images, or layout as desired.

### **index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Week 5 JS Lab</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header id="page-header">
    <h1>My Personal Blog</h1>
  </header>

  <nav id="main-nav">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main>
    <section class="intro-section">
      <h2>Welcome to My World</h2>
      <p>
        I’m a first-year student at Albright College, exploring HTML, CSS, and now JavaScript.
        In my spare time, I love painting, hiking, and reading a good sci-fi novel.
      </p>
      <img src="me.jpg" alt="A photo of me" width="300">
    </section>

    <section class="hobbies-section">
      <h2>My Hobbies</h2>
      <p>Some of my favorite activities include:</p>
      <ul>
        <li>Painting</li>
        <li>Hiking</li>
        <li>Reading</li>
      </ul>
    </section>

    <aside id="fun-fact-aside">
      <h3>Fun Fact</h3>
      <p>I once traveled to three countries in a single month!</p>
      <button id="toggle-fact-btn">Toggle Fun Fact</button>
    </aside>
  </main>

  <footer id="page-footer">
    <p>&copy; 2025 by [Your Name]. All rights reserved.</p>
  </footer>

  <!-- Load JavaScript at the bottom -->
  <script src="script.js"></script>
</body>
</html>
```

### **styles.css**
```css
/* 
  BASIC RESET & GLOBAL STYLES
*/
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background-color: #e6eeff;
  color: #333;
}

/* HEADER */
#page-header {
  background-color: #0066cc;
  color: #fff;
  text-align: center;
  padding: 1.5rem 0;
}

/* NAVIGATION */
#main-nav {
  background-color: #333;
}

#main-nav ul {
  list-style: none;
  display: flex;
  justify-content: center; 
  gap: 1rem;
  margin: 0;
  padding: 0.5rem 0;
}

#main-nav a {
  color: #fff;
  text-decoration: none;
  padding: 0.5rem 1rem;
  display: block; 
  transition: background-color 0.3s;
}

#main-nav a:hover {
  background-color: #555;
}

/* MAIN CONTENT */
main {
  max-width: 1000px;
  margin: 2rem auto;
  padding: 1rem;
}

section {
  background-color: #fff;
  margin-bottom: 2rem;
  padding: 1rem;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

section h2 {
  color: #0066cc;
}

/* ASIDE */
#fun-fact-aside {
  background-color: #fafafa;
  margin: 1rem 0;
  padding: 1rem;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  float: right;
  width: 30%;
}

/* FOOTER */
#page-footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 1rem 0;
  clear: both;
}

/* BUTTON (Toggle) */
#toggle-fact-btn {
  background-color: #0066cc;
  color: #fff;
  border: none;
  padding: 0.5rem 1rem;
  cursor: pointer;
  margin-top: 1rem;
  transition: background-color 0.3s;
}

#toggle-fact-btn:hover {
  background-color: #005bb5;
}

/* RESPONSIVE MEDIA QUERIES */

/* Mobile (up to 600px) */
@media (max-width: 600px) {
  #main-nav ul {
    flex-direction: column;
    align-items: center;
  }

  #fun-fact-aside {
    float: none;
    width: 100%;
  }

  img {
    width: 100%;
    height: auto;
  }
}

/* Tablet (up to 900px) */
@media (max-width: 900px) {
  #fun-fact-aside {
    float: none;
    width: 100%;
  }
  
  main {
    max-width: 700px;
  }
}
```

### **script.js**
```js
/* 
  BASIC JAVASCRIPT FOR WEEK 5
  - Listens for 'DOMContentLoaded' 
  - Toggles #fun-fact-aside on button click
*/

document.addEventListener("DOMContentLoaded", () => {
  const toggleBtn = document.getElementById("toggle-fact-btn");
  const funFactAside = document.getElementById("fun-fact-aside");

  // When the button is clicked, hide/show the aside
  toggleBtn.addEventListener("click", () => {
    // Check current display style
    if (funFactAside.style.display === "none") {
      // Show aside
      funFactAside.style.display = "block";
    } else {
      // Hide aside
      funFactAside.style.display = "none";
    }

    // Optional: Log the click in the console
    console.log("Toggle button was clicked!");
  });
});
```

---

## Submission & Grading

1. **Submit your `index.html`, `styles.css`, and `script.js` files** to the designated place (LMS or Git repo).  
2. **Due Date:** End of Week 5.

**Grading Criteria**  
1. **Working JavaScript (40%)**: Demonstrates DOM interaction and event handling.  
2. **Code Organization & Comments (30%)**: Clear code structure, explanatory comments in both CSS and JS.  
3. **Responsive Design (20%)**: Your existing media queries (Week 4) still function.  
4. **Overall Presentation (10%)**: The page looks neat; the JavaScript feature is easy to use.

---

**That’s It!**  
You’ve now combined **HTML, CSS, and JavaScript** into a single project, bringing your page to life with a simple interactive feature. Experiment further to **add more functionality**—such as changing text or styles when the aside is hidden—or even customizing the JavaScript to handle other events. Have fun exploring the power of front-end web development!
