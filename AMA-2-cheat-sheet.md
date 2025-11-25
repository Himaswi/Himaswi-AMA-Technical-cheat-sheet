## HTML & CSS Technical Questions  
### 1. What are CSS selectors?
CSS selectors are patterns used to select and style HTML elements. They tell the browser *which elements* a CSS rule should apply to. 
Common selectors include:
- element selectors (`p`)
- class selectors (`.box`)
- ID selectors (`#header`)
- attribute selectors, and pseudo-classes.

---
### 2. What is the difference between ID and Class selector?
* **ID Selector (`#id`)**
  * Unique for each element  
  * Cannot be reused  
  * Specificity is higher  
  * Example: `#main-title { color: red; }`

* **Class Selector (`.class`)**
  * Can be reused for multiple elements  
  * Lower specificity  
  * Example: `.highlight { color: blue; }`
---

### 3. What is the use of font in CSS?
The `font` properties in CSS are used to style text. They control:
* Font family (`font-family`)
* Font size (`font-size`)
* Font weight (`font-weight`)
* Font style (`font-style`)
* Line height (`line-height`)

**Example:**
```css
p {
  font-family: Arial;
  font-size: 16px;
  font-weight: bold;
}
```
---
### 4. What is the use of meta tag?
Meta tags provide information about the webpage to browsers and search engines. They are used for:
- SEO descriptions
- Responsive design (viewport)
- Character encoding (charset)
- Social media previews (Open Graph)
  
**Example:**
```html
<meta name="description" content="My website description">
```
---
### 5. What is the use of HAVING clause?
The HAVING clause filters groups of data after aggregation. It is used with GROUP BY, and can use aggregate functions such as COUNT, SUM, AVG.

**Example:**
```sql
SELECT department, COUNT(*) 
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```
---
### 6. Explain display in CSS.
The display property controls how an element behaves in the layout.
Common values:
- block – takes full width, starts on a new line
- inline – takes only content width, no new line
- inline-block – inline element with width/height support
- flex – enables flexbox layout
- grid – enables CSS grid layout
- none – hides element completely
  
**Example:**
```css
div {
  display: flex;
}
```
---
### 7. Which has more priority: internal or external CSS?
Internal CSS has more priority than external CSS because it is placed inside the <style> tag in the same HTML file.
However, inline CSS has the highest priority (except !important).
Priority order:
- Inline CSS
- Internal CSS
- External CSS
---
### 8. What is the difference between div and span?
| Element | Type | Behavior | Usage |
|---------|------|----------|--------|
| `div`   | Block element | Starts on a new line and takes full width | Used for layout, sections, containers |
| `span`  | Inline element | Does not start on a new line and only takes the required width | Used for styling small parts of text |

---
### 9. What is a class selector?
A class selector applies styles to elements that share the same class name. It is reusable and low specificity.

**Example:**
```css
.card {
  background: lightgray;
}
```
```html
<div class="card">Box 1</div>
<div class="card">Box 2</div>
```
---
### 10. What is Flexbox used for?
Flexbox is used to create one-dimensional layouts. It aligns and distributes space among items in a row or column.
Uses:
- Centering elements
- Creating navbars
- Making responsive layouts
- Equal height columns
  
**Example:**
```css
.container {
  display: flex;
  justify-content: center;
}
```
---
### 11. What is block and inline element?
**Block Elements:**
- Start on a new line
- Take full width
- Can set width/height
  
**Examples:** div, p, h1

**Inline Elements:**
- Do not start on a new line
- Take only required width
- Cannot set width/height
  
**Examples:** span, a, strong

---
### 12. Difference Between display: none; and visibility: hidden;
| Property             | What It Does                       | Space Taken?       |
|----------------------|-------------------------------------|---------------------|
| `display: none;`     | Hides the element completely        | No space taken      |
| `visibility: hidden;`| Makes the element invisible         | Space is preserved  |

### Example
```css
.hidden1 {
  display: none;
}

.hidden2 {
  visibility: hidden;
}
```

