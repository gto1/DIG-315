# Week 4 Build Lab

**Due Date:** End of Week 4 Sunday 11:59 PM  
**Points:** 50  
**Submission Format:** Your HTML and CSS code and any supporting files

### Learning Objectives
- Improve your Week 3 web page design by adding **polished styles** and **basic media queries** for a responsive layout.  
- Continue practicing effective CSS with clear comments, so you and your peers can easily understand how the code works.  


### Overview
In Week 3, you combined HTML and CSS to style your page. Now, we’ll **refine** that design and make it **responsive** with **media queries**. You’ll learn how to adapt your site to different screen sizes (mobile, tablet, desktop) so it remains user-friendly on any device.


### Instructions

1. **Set Up Your Workspace**  
   - Inside your existing project folder (e.g., `DIG-315 Project`) or whatever yours is named, create a **new HTML file** for Week 4 named `responsive.html` or something similar. Be sure you have the proper `.html`.  
   - Add in your basic HTML code to this file. Alternately, you can copy your `portfolio.html` code from Week 3 into this new file for a quick setup.  
   - Open your CSS file named `styles.css` in the same folder. At this point you should have at least your four (4) `.html` files and also your one (1) `styles.css` all in your one (1) project folder.


2. **Link Files & Confirm**  
   - Ensure your new `responsive.html` properly links to `styles.css` (just like Week 3).  
   - Open `responsive.html` in the browser to verify your current styling is still intact.

3. **Refine & Organize CSS**  
   - In your `styles.css`, **add explanatory comments** to existing selectors. For example:
     ```css
     /* 
       BODY SELECTOR
       - Sets the default font, background color,
         and global margin/padding. 
     */
     body {
       margin: 0;
       padding: 0;
       font-family: Arial, sans-serif;
       background-color: #e6eeff;
     }
     ```
   - Tweak your element, class, or ID selectors for better spacing, color harmony, and clarity. For instance, you might choose a consistent color palette, or adjust your margin/padding for a cleaner layout.

4. **Add New Styles for a Polished Look**  
   - Create a cohesive look using the following suggestions:
     - **Improved Header/Nav**: Make a prominent header area with a background color, a logo or brand text, and aligned navigation links.  
     - **Section/Article/Aside Styling**: Add subtle borders, box-shadow, or background shading to separate content areas:
       ```css
       /* 
         Example: Add a light gray background 
         and soft box shadow to sections 
       */
       section {
         background-color: #fff;
         margin: 1rem auto;
         padding: 1rem;
         max-width: 800px;
         box-shadow: 0 2px 5px rgba(0,0,0,0.1);
       }
       ```
     - **Footer**: A footer with a darker background color than the header can help visually separate it from the main content.

5. **Introduce Basic Media Queries**  
   - To make your site responsive, add **media queries** to `styles.css`. Start with **two breakpoints**—one for mobile (max 600px) and one for tablet (max 900px).  
   - Wrap your responsive rules inside these queries:
     ```css
     /* 
       MOBILE STYLES: 
       For screens up to 600px wide
     */
     @media (max-width: 600px) {
       /* 
         Example: Make the nav links stack vertically,
         increase font sizes or spacing for better legibility 
       */
       nav ul {
         display: block; /* or flex with direction: column; */
         text-align: center; 
       }
       nav ul li {
         margin-bottom: 1rem;
       }
       /* 
         Other adjustments for images, sections, aside, etc.
       */
       img {
         width: 100%; /* Make images fluid on small screens */
         height: auto; 
       }
     }

     /* 
       TABLET STYLES:
       For screens up to 900px wide 
       (but above 600px, if you like).
       This may overlap with the mobile query,
       so consider it an intermediate size.
     */
     @media (max-width: 900px) {
       /* 
         For example, reduce margins or change 
         the layout of aside from float to a full-width block 
       */
       aside {
         float: none; 
         width: 100%;
         margin: 1rem 0;
       }
     }
     ```
   - **Explain your choices** in comments, so it’s clear why you picked certain widths or layout changes.

6. **Test Different Screen Sizes**  
   - Resize your browser window or use your developer tools to simulate various device sizes (mobile, tablet, desktop).  
   - Check that your design remains clean, readable, and easy to navigate.

7. **Optional Enhancements**  
   - **Hover States**: Improve your buttons and nav links with hover transitions, as you did in Week 3.  
   - **Responsive Typography**: Use `em` or `rem` units, or add media queries to adjust `font-size` for smaller screens.  
   - **Flexbox or Grid**: If you want to experiment further, try converting some float-based layouts to a Flexbox or CSS Grid approach.

8. **Final Review & Submission**  
   - Verify all your code is valid HTML & CSS, with no stray tags or missing curly braces.  
   - Upload `index.html` and `styles.css` to your class LMS or Git repo as required.  
   - **Due Date**: End of Week 4.



### Grading Criteria

1. **Responsive Layout (40%)**  
   - Uses at least two media queries (`@media`) with clear breakpoints.  
   - Design adapts correctly for smaller screens.

2. **CSS Organization & Comments (25%)**  
   - Meaningful, concise comments for major selectors and media queries.  
   - Logical grouping/order of CSS rules.

3. **Enhanced Visual Design (25%)**  
   - Demonstrates thoughtful color choices, spacing, and layout beyond Week 3 basics.  
   - Clear improvements in overall aesthetics and usability.

4. **Code Quality & Submission (10%)**  
   - HTML and CSS are properly linked, validated, and submitted on time.  
   - Shows effort in cleaning up and improving the previous assignment.


**That’s it!** By applying **media queries** and a more polished CSS design, you’ll experience the power of **responsive web development**. Keep experimenting, ask questions, and enjoy seeing your page come to life on screens of all sizes.


### A Comprehensive Look at the Full Code Solution

Below is an **example** of how you might complete the **Week 4 assignment** with fully written HTML and CSS. This example uses semantic elements, a responsive layout, and clear code comments explaining each part. You can copy/paste these files directly into your `week4_responsive_assignment` folder and open `index.html` in your browser to see the result. Feel free to modify text content, images, or color choices to match your own style.

---

## `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Week 4 Responsive Assignment</title>
  <!-- Link to the external CSS file -->
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- 
    HEADER 
    - Contains page title or logo 
    - Optional: Could place nav inside header, but here we keep them separate
  -->
  <header id="page-header">
    <h1>My Personal Blog</h1>
  </header>

  <!-- 
    NAVIGATION 
    - Main site menu 
    - Uses an unordered list for links 
  -->
  <nav id="main-nav">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- 
    MAIN CONTENT 
    - Encloses primary page content 
    - Contains multiple sections and an aside 
  -->
  <main>
    <section class="intro-section">
      <h2>Welcome to My World</h2>
      <p>
        I’m a first-year student at Albright College, exploring HTML, CSS, and beyond.
        In my spare time, I love painting, hiking, and reading a good sci-fi novel.
      </p>
      <!-- 
        Image for demonstration 
        (replace "me.jpg" with your own image file if you have one) 
      -->
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

    <!-- 
      ASIDE 
      - Supplemental content that might be tangential or complementary 
    -->
    <aside id="fun-fact-aside">
      <h3>Fun Fact</h3>
      <p>I once traveled to three countries in a single month!</p>
    </aside>
  </main>

  <!-- 
    FOOTER 
    - Closing section of the page 
    - Commonly includes copyright 
  -->
  <footer id="page-footer">
    <p>&copy; 2025 by [Your Name]. All rights reserved.</p>
  </footer>
</body>
</html>
```

---

## `styles.css`

```css
/* 
  ------------------------------
  GLOBAL STYLES & BASIC RESETS
  ------------------------------
*/
* {
  /* Ensures consistent box sizing across elements */
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* 
  BODY SELECTOR
  - Sets default font, background color, etc.
*/
body {
  font-family: Arial, sans-serif; 
  background-color: #e6eeff; /* Light blue background */
  color: #333; /* Dark gray text */
}

/* 
  ------------------------------
  HEADER & NAVIGATION STYLES
  ------------------------------
*/

/* HEADER 
   - Basic styling for the page header 
*/
#page-header {
  background-color: #0066cc;
  color: #fff;
  text-align: center;
  padding: 1.5rem 0;
}

/* NAVIGATION 
   - Horizontal menu using flexbox 
*/
#main-nav {
  background-color: #333;
}
#main-nav ul {
  list-style: none;
  display: flex;
  justify-content: center;  /* Center nav items horizontally */
  gap: 1rem;               /* Spacing between each list item */
  margin: 0;
  padding: 0.5rem 0;
}
#main-nav li {
  /* Each nav item is spaced by the gap above */
}
#main-nav a {
  color: #fff;
  text-decoration: none;
  padding: 0.5rem 1rem;
  display: block; /* Helps with clickable area */
  transition: background-color 0.3s;
}
#main-nav a:hover {
  background-color: #555; 
}

/* 
  ------------------------------
  MAIN CONTENT
  ------------------------------
*/

/* MAIN 
   - Center content with a max-width 
   - Add some top/bottom spacing 
*/
main {
  max-width: 1000px;
  margin: 2rem auto; 
  padding: 1rem;
}

/* SECTIONS 
   - White background, slight shadow 
*/
section {
  background-color: #fff;
  margin-bottom: 2rem;
  padding: 1rem;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

/* Example of a distinct style for one section if desired */
.intro-section {
  /* Could add special color or border */
}

/* Another style for a second section */
.hobbies-section {
  /* Could do something like a subtle border-top, etc. */
  border-top: 2px solid #eee;
  margin-top: 2rem;
}

/* HEADINGS inside sections */
section h2 {
  color: #0066cc; /* Matches header color scheme for consistency */
}

/* 
  ASIDE
   - Usually displayed in a smaller column or float
*/
#fun-fact-aside {
  background-color: #fafafa;
  margin: 1rem 0; 
  padding: 1rem;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  float: right;   /* Floats the aside to the right on larger screens */
  width: 30%;     /* Adjust as desired */
}

/* 
  ------------------------------
  FOOTER STYLES
  ------------------------------
*/
#page-footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 1rem 0;
  clear: both; /* Ensures footer doesn't wrap around the aside float */
}

/* 
  ------------------------------
  RESPONSIVE DESIGN (MEDIA QUERIES)
  ------------------------------
*/

/* 
  MEDIA QUERY 1: MOBILE STYLES
  For screens up to 600px wide 
*/
@media (max-width: 600px) {
  /* 
    - Nav turns into a vertical list
    - Aside stops floating 
    - Images become fluid 
  */

  #main-nav ul {
    flex-direction: column;
    align-items: center; 
  }

  #main-nav a {
    padding: 1rem; /* Bigger tappable area */
  }

  #fun-fact-aside {
    float: none;    /* Remove float */
    width: 100%;    /* Full width */
    margin: 1rem 0;
  }

  /* Make images scale to fit screen width */
  img {
    width: 100%;
    height: auto;
  }
}

/* 
  MEDIA QUERY 2: TABLET STYLES
  For screens up to 900px wide
  (But above 600px, if you want an in-between layout)
*/
@media (max-width: 900px) {
  /* 
    - Slight modifications to layout 
    - Perhaps reduce the width of aside 
  */

  #fun-fact-aside {
    float: none;
    width: 100%;
    margin: 1rem 0;
  }
  
  main {
    /* Maybe a narrower max-width to ensure text lines don't get too long */
    max-width: 700px;
    padding: 0.5rem;
  }
}
```

---

### Tips & Customization

- Replace `me.jpg` with an actual image in the same folder to see your photo.  
- Modify color schemes (header/nav background, text colors, etc.) to match your personal preference.  
- Tweak the breakpoints (`max-width: 600px`, `max-width: 900px`) to suit different device sizes or design goals.  
- Add more sections, content, or new classes/IDs if you want to experiment further.

---

**That’s it!** This example demonstrates how to **enhance an existing HTML page** with **polished styling** and **media queries** to achieve a responsive design. The extensive comments should help you and your classmates understand each part of the code. Feel free to adapt this template to your needs, and have fun exploring more possibilities with HTML and CSS.
