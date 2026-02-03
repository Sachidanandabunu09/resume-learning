# 📚 HTML & CSS Complete Learning Guide

> Your roadmap to mastering web development fundamentals through this resume project.

---

## 🌐 What is HTML?

**HTML** (HyperText Markup Language) is the **skeleton** of every webpage.

```
Think of building a house:
HTML = The structure (walls, rooms, doors)
CSS  = The decoration (paint, furniture, style)
```

HTML uses **tags** to describe content:
```html
<tagname>Content goes here</tagname>
```

---

## 🎨 What is CSS?

**CSS** (Cascading Style Sheets) controls how HTML **looks**.

```css
selector {
    property: value;
}
```

**"Cascading"** means styles can override each other based on specificity (more on that below!)

---

## 📐 The Box Model (CRITICAL!)

Every HTML element is a **box** with 4 layers:

```
┌─────────────────────────────────────┐
│            MARGIN                   │  ← Space OUTSIDE the box
│   ┌─────────────────────────────┐   │
│   │        BORDER               │   │  ← The box edge (visible line)
│   │   ┌─────────────────────┐   │   │
│   │   │     PADDING         │   │   │  ← Space INSIDE the box
│   │   │   ┌─────────────┐   │   │   │
│   │   │   │   CONTENT   │   │   │   │  ← Your actual content
│   │   │   └─────────────┘   │   │   │
│   │   └─────────────────────┘   │   │
│   └─────────────────────────────┘   │
└─────────────────────────────────────┘
```

**Golden Rule:** Always use `box-sizing: border-box;`
- This makes width/height include padding and border
- Without it, adding padding makes elements bigger than expected!

---

## 🎯 CSS Selectors Cheat Sheet

| Selector | Example | What it selects |
|----------|---------|-----------------|
| Element | `p { }` | All `<p>` elements |
| Class | `.card { }` | Elements with `class="card"` |
| ID | `#header { }` | Element with `id="header"` |
| Descendant | `.nav a { }` | `<a>` inside `.nav` |
| Child | `.nav > a { }` | Direct `<a>` children of `.nav` |
| Multiple | `h1, h2, h3 { }` | All h1, h2, and h3 |
| Pseudo-class | `a:hover { }` | Link when mouse hovers |
| Pseudo-element | `p::first-line { }` | First line of paragraphs |

### Specificity (Which Style Wins?)

```
!important     →  1000 points (avoid using!)
Inline style   →  1000
ID             →  100
Class          →  10
Element        →  1
```

Higher score wins! If tied, last one in code wins.

---

## 📏 CSS Units Guide

| Unit | Type | Best For |
|------|------|----------|
| `px` | Absolute | Borders, shadows (fixed sizes) |
| `rem` | Relative | Font sizes, spacing (accessibility) |
| `em` | Relative | Spacing relative to current font |
| `%` | Relative | Widths relative to parent |
| `vw/vh` | Viewport | Full-screen sections |
| `fr` | Fraction | Grid column/row sizes |

**Best Practice:** Use `rem` for most things — it respects user's browser font settings!

---

## 📦 Flexbox Quick Reference

```css
.container {
    display: flex;
    
    /* Main axis (horizontal for row) */
    justify-content: center | space-between | flex-start | flex-end;
    
    /* Cross axis (vertical for row) */
    align-items: center | stretch | flex-start | flex-end;
    
    /* Direction */
    flex-direction: row | column | row-reverse | column-reverse;
    
    /* Wrapping */
    flex-wrap: wrap | nowrap;
    
    /* Gap between items */
    gap: 20px;
}
```

**When to use Flexbox:** 1-dimensional layouts (rows OR columns)
- Navigation bars
- Centering content
- Spacing items evenly
- Card rows

---

## 🔲 CSS Grid Quick Reference

```css
.container {
    display: grid;
    
    /* Define columns */
    grid-template-columns: 1fr 1fr 1fr;           /* 3 equal columns */
    grid-template-columns: repeat(3, 1fr);         /* Same as above */
    grid-template-columns: 200px 1fr 200px;        /* Fixed + flexible */
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Responsive! */
    
    /* Gap between items */
    gap: 20px;
}
```

**When to use Grid:** 2-dimensional layouts (rows AND columns)
- Page layouts
- Card grids
- Image galleries
- Complex forms

---

## 📱 Responsive Design Pattern

```css
/* Mobile styles first (base) */
.element {
    font-size: 16px;
    padding: 10px;
}

/* Tablet (768px and up) */
@media (min-width: 768px) {
    .element {
        font-size: 18px;
        padding: 20px;
    }
}

/* Desktop (1024px and up) */
@media (min-width: 1024px) {
    .element {
        font-size: 20px;
        padding: 30px;
    }
}
```

**Mobile-first** is preferred because:
- Simpler base styles
- Better performance on mobile
- Progressive enhancement

---

## ✨ Common Hover Effects

```css
/* Color change */
.button:hover {
    background-color: #e94560;
    color: white;
}

/* Float up effect */
.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
}

/* Scale (grow) */
.image:hover {
    transform: scale(1.05);
}

/* ALWAYS add transition to the base state! */
.card {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}
```

---

## ✅ HTML Best Practices

1. **One `<h1>` per page** — your main title
2. **Don't skip heading levels** — go h1 → h2 → h3, not h1 → h3
3. **Use semantic elements** — `<header>`, `<main>`, `<section>`, `<footer>`
4. **Always add `alt` to images** — for accessibility
5. **Use `<button>` for actions, `<a>` for navigation**
6. **Include viewport meta tag** — essential for mobile

---

## ✅ CSS Best Practices

1. **Use CSS variables** — for consistent theming
2. **Always set `box-sizing: border-box`**
3. **Never remove `:focus` styles** — accessibility!
4. **Use `rem` for font sizes** — better accessibility
5. **Add transitions to base state, not hover**
6. **Mobile-first with `min-width` queries**

---

## 🚀 Next Steps

After mastering this resume, explore:

1. **CSS Animations** — `@keyframes` for complex animations
2. **CSS Custom Properties** — advanced theming
3. **Accessibility (a11y)** — making sites usable for everyone
4. **CSS Preprocessors** — Sass/SCSS for advanced features
5. **JavaScript** — add interactivity!

---

## 📁 Project Files

| File | Purpose |
|------|---------|
| `index.html` | Structure + 20 HTML lessons |
| `styles.css` | Styling + 17 CSS lessons |
| `LEARN.md` | This reference guide |

**To view:** Open `index.html` in any web browser!

---

*Happy coding! 🎉*
