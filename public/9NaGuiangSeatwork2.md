# Seatwork #2 - Getting to know CSS Position and z-index

**Name:** Jenna Angela Guiang
<br>
**Date:** March 29, 2026  

---

## Step 1 (Static vs Relative)

**Answer:**

When `position: relative` is applied, the element moves from its original position using top and left values, but it still keeps its original space in the layout.

Compared to static positioning, the sidebar shifts visually (down and right by 20px), but other elements behave as if it is still in its original place.

---

## Step 2 (Fixed)

**Answer:**

When scrolling the page, the footer stays at the bottom of the screen and does not move.

This happens because `position: fixed` attaches the element to the viewport, unlike relative which moves based on its original position in the document.

---

## Step 3 (Absolute)

**Answer:**

`position: absolute` removes the element from the normal document flow and positions it based on its nearest positioned ancestor (or the page if none exists).

Unlike fixed, absolute elements move when the page is scrolled, while fixed elements stay in place.

---

## Step 4 (Absolute + z-index)

**Answer:**

The notice appears on top because it has a higher `z-index` (2) than the content (1).

If the values are swapped, the content will cover the notice instead.

---

## Challenge

### 1. Position .notice at the top right corner of .content

```css
.content {
  position: relative;
}

.notice {
  position: absolute;
  top: 0;
  right: 0;
}
```

---

### 2. Observations when changing .content position

- **Relative:** The notice positions correctly inside the content box.  
- **Fixed:** The content stays in place while scrolling, and the notice moves with it.  

---

### 3. Effect of z-index

The z-index controls which element appears on top. Higher values appear in front, while lower values appear behind.

---

## Reflection Questions

### a. Differences between CSS position values

- **Static:** Default, no positioning applied.  
- **Relative:** Moves relative to its original position.  
- **Absolute:** Positioned relative to the nearest positioned parent.  
- **Fixed:** Positioned relative to the screen and does not move when scrolling.  

---

### b. How absolute depends on parent

Absolute positioning depends on the nearest parent with a position other than static. If none exists, it uses the entire page as reference.

---

### c. Sticky vs Fixed

- **Fixed:** Always stays in place on the screen.  
- **Sticky:** Acts like relative until a scroll threshold is reached, then behaves like fixed.  

---

### d. Application in a school event webpage

Positioning can be used to highlight important elements such as:

- A **fixed header** for navigation so users can always access menu options.  
- A **sticky announcement bar** for important reminders.  
- An **absolute positioned banner** to highlight event details.  
- A **floating notice box** for urgent announcements like schedule changes.  

These help make important information more visible and accessible.