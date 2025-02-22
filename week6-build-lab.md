# Week 6 Build Lab

**Due Date:** End of Week 6 Sunday 11:59 PM  
**Points:** 50  
**Submission Format:** Your HTML, CSS, and Javascript code and any supporting files. A screen shot or screen recording of it working is perfectly acceptable and makes it easy for me to check that you are doing well.


### Learning Objectives
- Practice **JavaScript arrays**, **event handling**, and **DOM manipulation** while **keeping everything local**—no internet connections or external APIs required.  
- Reinforce fundamental JS concepts in a straightforward setup, allowing you to just double-click your file and run the code.


## Overview
In this lab, you’ll create a **local random quote feature** that displays quotes from a simple JavaScript array. Each time the user clicks a button, it selects a random quote, updates the page, and requires **no external network** calls or servers—ideal for working purely on your own machine.


## Instructions

1. **Create a New File**  
   - Name it something like `quotes.html`. 

2. **Copy and study the Following Code**  
   - Paste the code below into `quotes.html`.  
   - Feel free to **modify** the array of quotes, colors, or styling to personalize your page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Local Random Quotes</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 2rem;
      background: #f0f0f0;
    }
    h1 {
      text-align: center;
      color: #0066cc;
    }
    #quote-container {
      max-width: 600px;
      margin: 2rem auto;
      background: #fff;
      padding: 2rem;
      text-align: center;
      border-radius: 4px;
    }
    #get-quote-btn {
      background-color: #0066cc;
      color: #fff;
      border: none;
      padding: 0.5rem 1.5rem;
      cursor: pointer;
      border-radius: 4px;
      margin-bottom: 1rem;
      transition: background-color 0.3s;
    }
    #get-quote-btn:hover {
      background-color: #005bb5;
    }
    blockquote {
      font-style: italic;
      color: #555;
      margin-bottom: 1rem;
      min-height: 50px; /* Ensures consistent layout even for short quotes */
    }
    cite {
      display: block;
      color: #888;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <h1>Local Random Quotes</h1>
  <div id="quote-container">
    <button id="get-quote-btn">Get a Quote</button>
    <blockquote id="quote-text">Click the button to see a quote!</blockquote>
    <cite id="quote-author"></cite>
  </div>

  <script>
    // Our local quotes array (no network needed)
    const quotes = [
      {
        text: "Act as if what you do makes a difference. It does.",
        author: "William James"
      },
      {
        text: "Success is not final, failure is not fatal: it is the courage to continue that counts.",
        author: "Winston Churchill"
      },
      {
        text: "Never bend your head. Always hold it high. Look the world straight in the eye.",
        author: "Helen Keller"
      },
      {
        text: "What you get by achieving your goals is not as important as what you become by achieving your goals.",
        author: "Zig Ziglar"
      },
      {
        text: "Believe you can and you're halfway there.",
        author: "Theodore Roosevelt"
      }
      // Feel free to add or change quotes here!
    ];

    // Select our HTML elements
    const getQuoteBtn = document.getElementById('get-quote-btn');
    const quoteText = document.getElementById('quote-text');
    const quoteAuthor = document.getElementById('quote-author');

    // On button click, choose a random quote from the array
    getQuoteBtn.addEventListener('click', () => {
      // Generate a random index
      const randomIndex = Math.floor(Math.random() * quotes.length);
      // Retrieve the quote object
      const selectedQuote = quotes[randomIndex];

      // Update the DOM
      quoteText.textContent = selectedQuote.text;
      quoteAuthor.textContent = `— ${selectedQuote.author}`;
    });
  </script>
</body>
</html>
```

4. **Open in Your Browser**  
   - Simply **double-click** `quotes.html` or open it with “Open With -> Browser.”  
   - You should see the page load with a **“Get a Quote”** button and a placeholder quote.  
   - **Click** the button to randomly display a quote from the array.

5. **Experiment & Customize**  
   - **Add more quotes**: Just extend the `quotes` array with your own inspiring phrases.  
   - **Change the look**: Update fonts, colors, or layout in the `<style>` block.  
   - **Show/Hide the quote**: Extend the JavaScript logic if you want to hide the quote before it displays, or toggle additional info.

---

## Submission
1. **Submit your `quotes.html` file** (the single file) via the designated method (LMS, GitHub, etc.).  
2. Also, submit a **screen video of your working quotes** functionality in class.

---

## Grading Criteria
1. **Working JavaScript (40%)**  
   - Randomly selects a quote and displays it on the page upon button click.  
2. **HTML/CSS Organization (30%)**  
   - Uses a clear structure and presentable styling.  
3. **Code Quality (20%)**  
   - Properly commented or well-organized code.  
   - No syntax errors or broken references.  
4. **Originality & Effort (10%)**  
   - At least one creative tweak (e.g., styling changes, additional quotes, etc.).  

---

**That’s it!** By completing this local quotes build lab, you’ve combined **HTML**, **CSS**, and **JavaScript** in a single file that runs offline, free of network restrictions or servers. This approach reinforces your understanding of arrays and event-driven interactions in JavaScript. Good luck, and have fun adding your own personal flavor to the quotes!
