# Week 3 In-Class Project: Personal Profile Page with Contact Form

## Project Overview
In this project, you'll build a personal profile page that showcases your information and includes a contact form. This project combines the HTML semantic elements you learned in your prep work with CSS styling and introduces HTML forms.

**Files:** `index.html` and `style.css`

## Learning Objectives
- Apply semantic HTML5 structure
- Implement CSS basics and box model concepts
- Create and style HTML forms
- Practice external CSS workflow
- Use Chrome DevTools for debugging

---

## Phase 1: HTML Structure Setup

### Step 1: Create the Semantic Structure
Using the semantic HTML elements from your Chapter 2 prep work, create the basic page structure:

```html
<header>
    <h1>Your Name</h1>
    <p class="tagline">Your Title/Role</p>
</header>

<nav>
    <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>

<main>
    <!-- We'll add sections here -->
</main>

<footer>
    <p>&copy; 2025 Your Name</p>
</footer>
```

### Step 2: Add Content Sections
Inside your `<main>` element, add these sections:

```html
<section id="about">
    <h2>About Me</h2>
    <p>Write a brief paragraph about yourself...</p>
    <p>Add another paragraph about your interests...</p>
</section>

<section id="skills">
    <h2>Skills & Interests</h2>
    <ul class="skills-list">
        <li>HTML5 & Semantic Markup</li>
        <li>CSS3 & Responsive Design</li>
        <li>Add your other skills...</li>
    </ul>
</section>

<section id="contact">
    <h2>Get In Touch</h2>
    <p>We'll add a contact form here next!</p>
</section>
```

**🎯 Goal:** By the end of this phase, you should have a complete HTML structure using semantic elements.

---

## Phase 2: Contact Form Creation

### Step 3: Understanding HTML Forms
Forms are used to collect user input. The basic structure is:
- `<form>` - container for the entire form
- `<input>` - various input types (text, email, etc.)
- `<textarea>` - multi-line text input
- `<button>` - submit button

### Step 4: Build the Contact Form
Replace the paragraph in your contact section with this form:

```html
<form action="#" method="post" class="contact-form">
    <div class="form-group">
        <label for="name">Your Name:</label>
        <input type="text" id="name" name="name" required>
    </div>
    
    <div class="form-group">
        <label for="email">Your Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    
    <div class="form-group">
        <label for="subject">Subject:</label>
        <input type="text" id="subject" name="subject">
    </div>
    
    <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" name="message" rows="5" required></textarea>
    </div>
    
    <button type="submit">Send Message</button>
</form>
```

**Key Form Concepts:**
- `action="#"` - where form data is sent (we'll keep it simple for now)
- `method="post"` - HTTP method for sending data
- `for` attribute connects labels to inputs
- `required` attribute makes fields mandatory
- Different input types: `text`, `email`, `textarea`

**🎯 Goal:** Your page now has a functional contact form structure.

---

## Phase 3: CSS Styling

### Step 5: Base Styles and Box Model
Add these styles to your `style.css`:

```css
/* Reset and base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f4f4f4;
}
```

### Step 6: Header Styling
```css
header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    text-align: center;
    padding: 3rem 0;
}

header h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

.tagline {
    font-size: 1.2rem;
    opacity: 0.9;
}
```

### Step 7: Navigation Styling
```css
nav {
    background-color: white;
    padding: 1rem 0;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 2rem;
}

nav a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}

nav a:hover {
    background-color: #667eea;
    color: white;
}
```

### Step 8: Content and Form Styling
```css
main {
    max-width: 800px;
    margin: 2rem auto;
    padding: 0 1rem;
}

section {
    background-color: white;
    margin-bottom: 2rem;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

/* Form styling */
.form-group {
    margin-bottom: 1.5rem;
}

label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
}

input[type="text"],
input[type="email"],
textarea {
    width: 100%;
    padding: 0.75rem;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 1rem;
}

input:focus,
textarea:focus {
    outline: none;
    border-color: #667eea;
}

button {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 0.75rem 2rem;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
```

**🎯 Goal:** Your page should now have professional styling with proper box model implementation.

---

## Phase 4: Debugging & Refinement

### Step 9: Chrome DevTools Practice
1. Right-click on any element and select "Inspect"
2. In the Elements tab, hover over elements to see the box model
3. Try modifying CSS values directly in the DevTools
4. Notice how the box model shows content, padding, border, and margin

### Step 10: Final Touches
- Check that all form elements are properly aligned
- Verify navigation links work (they should scroll to sections)
- Test the responsive behavior by resizing your browser
- Make any final adjustments to colors or spacing

**🎯 Goal:** Your page is complete, responsive, and debugged using DevTools.

---

## 🎉 Project Complete!

You've successfully created a personal profile page that demonstrates:
- ✅ Semantic HTML5 structure
- ✅ CSS box model implementation  
- ✅ HTML form creation and styling
- ✅ External CSS workflow
- ✅ Chrome DevTools usage

## Next Steps
- Customize the content with your own information
- Try different color schemes
- Add more sections (projects, experience, etc.)
- Experiment with different form field types

## Troubleshooting

**Form not displaying correctly?**
- Check that you have both opening and closing tags
- Verify the `class` attributes match your CSS

**Styles not applying?**
- Make sure your CSS file is linked correctly
- Check for typos in class names and selectors
- Use DevTools to see which styles are active

**Layout issues?**
- Remember the box model: content + padding + border + margin
- Use DevTools to visualize the box model
- Check for missing `box-sizing: border-box`