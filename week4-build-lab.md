**Week 4 Assignment: “Enhancing Our Web Page with Advanced CSS & Media Queries”**

### Objective
- Improve your Week 3 web page design by adding **polished styles** and **basic media queries** for a responsive layout.  
- Continue practicing effective CSS with clear comments, so you and your peers can easily understand how the code works.  

---

### Overview
In Week 3, you combined HTML and CSS to style your page. Now, we’ll **refine** that design and make it **responsive** with **media queries**. You’ll learn how to adapt your site to different screen sizes (mobile, tablet, desktop) so it remains user-friendly on any device.

---

### Instructions

1. **Set Up Your Workspace**  
   - Make a new folder named `week4_responsive_assignment`.  
   - Copy your `index.html` and `styles.css` from Week 3 into this folder.

2. **Link Files & Confirm**  
   - Ensure your `index.html` properly links to `styles.css` (just like Week 3).  
   - Open `index.html` in the browser to verify your current (Week 3) styling is still intact.

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

---

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

---

**That’s it!** By applying **media queries** and a more polished CSS design, you’ll experience the power of **responsive web development**. Keep experimenting, ask questions, and enjoy seeing your page come to life on screens of all sizes!
