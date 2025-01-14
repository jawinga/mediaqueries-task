# Media Queries Task: ROADMAP

## Step 1: Learning the Basics of Media Queries

### What are media queries?

Media queries allow websites to be **responsive** by applying different CSS rules based on **screen size, device type, or resolution**.

### Key Concepts

- `@media` → Activates media queries.
- `screen` / `all` / `print` / `speech` → Defines the type of media.
- `min-width` / `max-width` → Adjust styles based on **width**.
- `min-height` / `max-height` → Adjust styles based on **height**.
- `orientation: landscape | portrait` → Detects **device rotation**.
- `resolution`, `aspect-ratio` → More advanced techniques.

---

## Step 2: Handling Overlapping Styles

### Problem

I tried using **four conditions** (`max-width`, `min-width`, `max-height`, `min-height`) to change the background color.

### Challenges Faced

- The queries **overlapped**, making the styles unpredictable.
- The approach was **not scalable** or **readable**.

### Lesson Learned

- **Using too many conditions is inefficient.**
- **Simplifying the logic** makes it easier to debug and adjust.

---

## Step 3: Using `max-width` for Simplicity

### Why `max-width`?

- More **readable**, **easier to adjust**, and **scales well**.
- Works well in **mobile-first** responsive design.

---

## Step 4: Choosing Desktop-First vs. Mobile-First Approach

### Why Desktop-First (`max-width`)?

- **Best for desktop-optimized applications**.
- **Easier for complex layouts** (e.g., dashboards, enterprise tools).
- **Media queries are ordered from biggest to smallest**.

### Alternative: Mobile-First (`min-width`)

- **Best for mobile-first applications**.
- **Starts from smallest screens and scales up**.

### Challenges Faced

- Deciding which approach to choose from.

---

## Step 5: Adjusting Font Sizes & Adding Smooth Transitions

### Font Size Adjustments

- When screens get **smaller**, font size **increases** for readability.
- **Used `em` instead of `px`** for consistency across devices.

### Smooth Background Transitions

- Instead of **instantly changing colors**, I used:
  ```css
  body {
    transition: background-color 0.5s ease-in-out;
  }
  ```

## Next steps:

**Learn accessibility features**

-prefers-reduced-motion for low-budget phones that have limitations.
-prefer-contrast
-inverted-colours

**Apply media queries to containers such as Grids.**
