# Week 3 Build Lab

**Due Date:** End of Week 3 Sunday 11:59 PM  
**Points:** 50  
**Submission Format:** Your HTML and CSS code and any supporting files

### Learning Objectives
- Enhance your existing HTML from Weeks 1 or 2 by adding **basic, practical CSS** for styling and layout.  
- Practice using common CSS selectors (element, class, ID, pseudo-class) to control colors, fonts, positioning, and spacing.  
- Gain experience separating structure (HTML) from presentation (CSS).


### Overview
In this assignment, you’ll take the same content or HTML structure you created in prior weeks (e.g., the “Week 2 Semantic HTML” page) and apply **introductory CSS** rules. By the end, your webpage will look more polished and professional.


### Instructions

1. **Set Up Your Workspace**  
   - Inside your existing project folder (e.g., `DIG-315 Project`) or whatever yours is named, create a **new HTML file** for Week 3 named `portfolio.html` or something similar. Be sure you have the proper `.html`.  
   - Add in your basic HTML code to this file. Alternately, you can copy your `aboutus.html` code from Week 2 into this new file for a quick setup.  
   - Create a new file named `styles.css` in the same folder. At this point you should have at least your 3 `.html` files and also your new `styles.css` all in your one project folder.

2. **Link Your CSS**  
   - In the `<head>` section of `portfolio.html`, link your new stylesheet:
     ```html
     <link rel="stylesheet" href="styles.css">
     ```

3. **Basic Element Selectors**  
   - Use **element selectors** (e.g., `body`, `h1`, `p`, `section`, `footer`) in `styles.css` to set default styling. For example:
     ```css
     /* Element selectors */
     body {
       margin: 0;
       padding: 0;
       font-family: Arial, sans-serif;
       background-color: #f0f0f0;
     }

     h1, h2, h3 {
       color: #333;
       text-align: center;
     }

     p {
       color: #555;
       line-height: 1.5;
     }
     ```
   - Add margins, padding, or other basic rules to improve readability.

4. **Class & ID Selectors**  
   - Assign **class** or **id** attributes to specific elements in your HTML if you want to style them uniquely:
     ```html
     <header id="main-header">
       <h1>My Personal Blog</h1>
     </header>

     <section class="intro-section">
       <h2>About Me</h2>
       <p>Paragraph text here...</p>
     </section>
     ```
   - In your `styles.css`, target them:
     ```css
     /* ID selector */
     #main-header {
       background-color: #222;
       color: #fff;
       padding: 1rem;
     }

     /* Class selector */
     .intro-section {
       background-color: #fff;
       padding: 2rem;
       margin: 1rem auto;
       max-width: 700px;
     }
     ```

5. **Styling Navigation**  
   - If you have a `<nav>` or menu links, style them to create a simple horizontal menu. For instance:
     ```css
     nav ul {
       list-style: none;
       display: flex; /* or inline-block / flex / or even float */
       justify-content: center;
       gap: 1rem;
       padding: 0;
       margin: 0;
       background-color: #333;
     }

     nav ul li a {
       color: #fff;
       text-decoration: none;
       padding: 0.5rem 1rem;
       display: inline-block;
     }

     /* Pseudo-class for hover effect */
     nav ul li a:hover {
       background-color: #555;
     }
     ```

6. **Positioning & Layout**  
   - Explore **basic positioning** or layout methods (using margins, padding, or `display` properties) to arrange sections on the page:
     ```css
     main {
       margin: 2rem auto;
       max-width: 800px;
       background-color: #fff;
       box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
     }

     aside {
       float: right;
       width: 30%;
       margin: 1rem;
       background-color: #fafafa;
     }
     ```
   - You can also try `display: flex;` for more advanced layouts if you feel comfortable.

7. **Color & Font Choices**  
   - Apply color schemes and fonts (either system fonts or from Google Fonts) to make your page unique:
     ```css
     body {
       background-color: #e6eeff; /* Soft background */
       font-family: 'Roboto', sans-serif; /* If you included this in your <head> */
     }

     h1 {
       color: #0066cc; /* Complementary color for headings */
     }
     ```
   - NOTE: You should only have `body`, `h1`, or any other CSS selector listed in your `styles.css` file, but you can simply add more properties and values to the one that you already have in your CSS.

8. **Optional Transition or Basic Animation**  
   - Add a **hover transition** on buttons or images:
     ```css
     img {
       transition: transform 0.3s;
     }

     img:hover {
       transform: scale(1.05);
     }
     ```
   - Keep it simple; we’ll explore more robust CSS animations in future lessons.

9. **Test & Refine**  
   - **Open `portfolio.html` in your browser** to see if your CSS updates appear.
   - If it's working, GREAT 🎉 -- Keep exploring and refining with various CSS that we've learned this week.
   - If it's not working ❌ -- Go back to the earlier steps and check:
      - Your `<link>` element is in your HTML files `<head>` section properly.
      - Your CSS syntax and structure (the grammar of your code)
   - GET CREATIVE!! Adjust the rules in `styles.css` until you’re happy with how the page looks.

10. **Add Your CSS To All of Your HTML Pages**  
   - Go back to your Week 1 and Week 2 HTML and add the `<link>` to your CSS files (Step #2 above) so that your CSS styles your entire site, not just one page.

11. **Submission**  
   - Submit your `index.html` and `styles.css` files to the LMS or your class repo.
   - Take a screen shot or screen video of your working site with CSS to share with the class.
   - **Due Date:** End of Week 3.


### Grading Criteria
1. **Effective Use of CSS Selectors (40%)**  
   - Demonstrates element, class, ID, and pseudo-class selectors.  
   - Proper styling for headings, paragraphs, lists, images, and navigation.  

2. **Layout & Positioning (25%)**  
   - Shows basic positioning or layout (e.g., margins, floats, or a simple flex layout).  
   - Content is visually well-organized.  

3. **Styling & Design (25%)**  
   - Thoughtful application of color, font choice, and spacing.  
   - Optional hover transitions or minimal animations.  

4. **Overall Presentation & Clarity (10%)**  
   - Page is easy to read, with consistent formatting.  
   - Clear effort to enhance the Week 2 HTML with new CSS.


**That’s it!** You’re now combining **HTML** and **CSS** to create more engaging, visually appealing web pages. As you continue to practice and refine your layouts, you’ll see how powerful this duo is for bringing your ideas to life on the web. Good luck, and have fun experimenting with different styles.
