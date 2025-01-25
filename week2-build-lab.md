**Week 2 Assignment: “Expanding Our HTML with Semantic Elements”**  

### Objective
- Build on last week’s assignment by incorporating **semantic HTML elements** to enhance structure and readability.  
- Practice using `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, and `<footer>` in a single page.  
- Reinforce your understanding of headings, paragraphs, images, and lists in a more organized layout.

---

### Overview
This week, you’ll create a **new HTML page** (without any CSS or JavaScript) that showcases proper use of semantic elements. Semantic elements convey the purpose of different sections of your webpage, making it easier for both developers and browsers (including assistive technologies) to understand the content’s structure.

---

### Instructions

1. **Create a New File and Folder**  
   - Make a folder named `week2_html_assignment`.  
   - Inside that folder, create a file named `index.html`.

2. **Basic Skeleton**  
   - Start with the standard HTML doctype and structure:

     ```html
     <!DOCTYPE html>
     <html lang="en">
     <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Week 2 Semantic HTML</title>
     </head>
     <body>
       <!-- Your content will go here -->
     </body>
     </html>
     ```

3. **Header & Navigation**  
   - In your `<body>`, create a `<header>` that includes a prominent heading for the page (e.g., “My Personal Blog” or “My Travel Journal”).  
   - Below the heading, add a `<nav>` containing a simple list of navigation links (e.g., “Home,” “About,” “Contact”). These can be placeholder links for now:

     ```html
     <header>
       <h1>My Personal Blog</h1>
       <nav>
         <ul>
           <li><a href="#">Home</a></li>
           <li><a href="#">About</a></li>
           <li><a href="#">Contact</a></li>
         </ul>
       </nav>
     </header>
     ```

4. **Main Content**  
   - Add a `<main>` element to represent the central part of your page.  
   - Inside `<main>`, break your content into logical `<section>` or `<article>` elements.  
   - For example, you might have:
     - A `<section>` about your hobbies.  
     - Another `<section>` for a brief biography.  
     - Within each section, use headings (`<h2>`, `<h3>`, etc.), paragraphs (`<p>`), and lists (`<ul>` or `<ol>`) just like in Week 1.  
   - Make sure to **reuse** or **expand** on the content you created last week, but now organize it within these new semantic elements.

     ```html
     <main>
       <section>
         <h2>My Hobbies</h2>
         <p>Here is a list of things I enjoy doing:</p>
         <ul>
           <li>Painting</li>
           <li>Hiking</li>
           <li>Reading</li>
         </ul>
       </section>

       <section>
         <h2>About Me</h2>
         <p>I am a first-year student at Albright College, passionate about web development...</p>
         <img src="me.jpg" alt="A photo of me" width="200">
       </section>
     </main>
     ```

5. **Aside (Optional, But Encouraged)**  
   - If you have some additional or **side content** (like “Featured Post,” “Upcoming Events,” or “Fun Facts”), put it inside an `<aside>`:

     ```html
     <aside>
       <h3>Fun Fact</h3>
       <p>I once traveled to three countries in one month!</p>
     </aside>
     ```

6. **Footer**  
   - At the bottom of your page, include a `<footer>` with relevant information, such as your name, the course title, or a brief copyright:

     ```html
     <footer>
       <p>&copy; 2025 by [Your Name]. All rights reserved.</p>
     </footer>
     ```

7. **Validate & Review**  
   - Check that your HTML is well-structured:  
     - The `<header>` is above `<main>`.  
     - `<main>` contains your primary content, subdivided into `<section>`/`<article>`.  
     - `<aside>` is optional but placed where it makes sense (likely within `<main>` or after it).  
     - `<footer>` is at the bottom of the page.  
   - Make sure the content **flows logically** and is easy to read.  
   - **Open `index.html` in your browser** to verify that your headings, paragraphs, images, lists, and semantic elements display correctly (though unstyled for now).

8. **Submission**  
   - Upload or submit your `index.html` file in the manner specified (via LMS or Git repo link).  
   - **Due Date:** End of Week 2.  

---

### Grading Criteria
1. **Semantic Structure (40%)**: Correct use of `<header>`, `<nav>`, `<main>`, `<section>`, `<aside>`, and `<footer>`.  
2. **HTML Fundamentals (30%)**: Proper headings, paragraphs, lists, and images.  
3. **Organization & Readability (20%)**: Logical content flow and clarity of code.  
4. **Timeliness & Effort (10%)**: Submission by deadline and evidence of thoughtful planning.

---

**That’s it!** By completing this assignment, you’ll gain confidence in creating more meaningful HTML layouts. Next, we’ll explore how to style these semantic elements with CSS, but for now, focus on structure and semantics to build a solid foundation. Good luck!
