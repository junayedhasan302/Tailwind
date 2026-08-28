# Tailwind CSS — Basic Revision Notes

## 1. What is Tailwind CSS?

Tailwind CSS is a **utility-first CSS framework**.

Instead of writing custom CSS classes:

```css
.btn {
  background: orange;
  padding: 10px 20px;
}
```

we can use utility classes directly in HTML:

```html
<button class="bg-orange-500 px-5 py-2">
  Click Me
</button>
```

> Tailwind does not replace CSS concepts. It gives us utility classes to write CSS faster.

---

# 2. Basic Syntax

Most Tailwind classes represent a single CSS property or a small group of related properties.

```html
<div class="p-5 bg-white rounded-lg shadow">
  Hello
</div>
```

Common examples:
---------------------------------------
| Tailwind      |   CSS idea          |
|---------------|----------------------
| `p-4`         |   padding           |
| `m-4`         |   margin            |
| `text-center` |   text-align        |
| `font-bold`   |   font-weight       |
| `bg-blue-500` |   background color  |
| `text-white`  |   text color        |
| `rounded-lg`  |   border-radius     |
| `shadow`      |   box-shadow        |
| `flex`        |   display: flex     |
| `grid`        |   display: grid     |
---------------------------------------
---

# 3. Colors

Tailwind commonly uses a color + shade system.

```html
<p class="text-blue-500">Hello</p>
<div class="bg-green-500">Content</div>
```

Examples:

```text
red-500
blue-500
green-500
yellow-500
purple-500
gray-500
black
white
```

Different shades:

```html
<p class="text-blue-300">Light</p>
<p class="text-blue-500">Normal</p>
<p class="text-blue-700">Dark</p>
```

---

# 4. Text Color

```html
<p class="text-red-500">Red text</p>
<p class="text-gray-600">Gray text</p>
<p class="text-white">White text</p>
```

Syntax:

```text
text-{color}-{shade}
```

---

# 5. Background Color

```html
<div class="bg-blue-500">
  Content
</div>
```

Syntax:

```text
bg-{color}-{shade}
```

---

# 6. Font Size

Common classes:

```html
<p class="text-xs">Extra Small</p>
<p class="text-sm">Small</p>
<p class="text-base">Normal</p>
<p class="text-lg">Large</p>
<p class="text-xl">Extra Large</p>
<p class="text-2xl">2XL</p>
<p class="text-4xl">4XL</p>
```

Useful heading example:

```html
<h1 class="text-4xl font-bold">
  My Website
</h1>
```

---

# 7. Font Weight

```html
<p class="font-light">Light</p>
<p class="font-normal">Normal</p>
<p class="font-medium">Medium</p>
<p class="font-semibold">Semi Bold</p>
<p class="font-bold">Bold</p>
<p class="font-extrabold">Extra Bold</p>
```

---

# 8. Text Alignment

```html
<p class="text-left">Left</p>
<p class="text-center">Center</p>
<p class="text-right">Right</p>
```

---

# 9. Margin

`m` means margin.

```html
<div class="m-4"></div>
```

Common directional classes:

```text
m-4   → all sides
mt-4  → margin-top
mb-4  → margin-bottom
ml-4  → margin-left
mr-4  → margin-right
mx-4  → left + right
my-4  → top + bottom
```

Example:

```html
<div class="mt-5 mb-10">
  Content
</div>
```

---

# 10. Padding

`p` means padding.

```text
p-4   → all sides
pt-4  → padding-top
pb-4  → padding-bottom
pl-4  → padding-left
pr-4  → padding-right
px-4  → left + right
py-4  → top + bottom
```

Example:

```html
<div class="px-6 py-4">
  Content
</div>
```

---

# 11. Width

Common classes:

```html
<div class="w-full"></div>
<div class="w-1/2"></div>
<div class="w-1/3"></div>
<div class="w-1/4"></div>
<div class="w-screen"></div>
```

Examples:

```text
w-full   → 100%
w-1/2    → 50%
w-1/3    → 33.33%
w-1/4    → 25%
w-screen → viewport width
```

---

# 12. Height

```html
<div class="h-20"></div>
<div class="h-32"></div>
<div class="h-screen"></div>
```

Useful:

```text
h-screen → viewport height
min-h-screen → minimum height of viewport
```

---

# 13. Max Width

Very useful for containers:

```html
<div class="max-w-6xl mx-auto">
  Content
</div>
```

`mx-auto` centers the element horizontally when its width allows it.

Common max-width classes:

```text
max-w-sm
max-w-md
max-w-lg
max-w-xl
max-w-2xl
max-w-4xl
max-w-6xl
max-w-7xl
```

---

# 14. Display

```html
<div class="block"></div>
<div class="inline"></div>
<div class="inline-block"></div>
<div class="hidden"></div>
```

Important:

```text
hidden → display: none
```

The element is removed from the layout.

---

# 15. Flexbox

Use:

```html
<div class="flex">
```

Equivalent concept:

```css
display: flex;
```

Common flex classes:

```text
flex
flex-row
flex-col
flex-wrap
```

---

# 16. Justify Content

```text
justify-start
justify-center
justify-end
justify-between
justify-around
justify-evenly
```

Example:

```html
<div class="flex justify-between">
  <span>Logo</span>
  <span>Menu</span>
</div>
```

Equivalent CSS idea:

```css
display: flex;
justify-content: space-between;
```

---

# 17. Align Items

```text
items-start
items-center
items-end
items-stretch
```

Example:

```html
<div class="flex items-center">
  Content
</div>
```

---

# 18. Gap

For spacing between flex/grid children:

```html
<div class="flex gap-4">
  ...
</div>
```

Other examples:

```text
gap-2
gap-4
gap-6
gap-8
```

Directional gap:

```text
gap-x-4
gap-y-4
```

---

# 19. Grid

Basic grid:

```html
<div class="grid">
```

Two columns:

```html
<div class="grid grid-cols-2">
```

Three columns:

```html
<div class="grid grid-cols-3">
```

Four columns:

```html
<div class="grid grid-cols-4">
```

With gap:

```html
<div class="grid grid-cols-3 gap-6">
```

---

# 20. Border

```html
<div class="border">
  Content
</div>
```

Border width:

```text
border
border-2
border-4
```

Border color:

```html
<div class="border border-gray-300">
```

---

# 21. Border Radius

```text
rounded
rounded-sm
rounded-md
rounded-lg
rounded-xl
rounded-2xl
rounded-full
```

Example:

```html
<button class="rounded-lg">
  Login
</button>
```

For a pill/circle style:

```html
<button class="rounded-full">
  Button
</button>
```

---

# 22. Shadow

```html
<div class="shadow">
  Card
</div>
```

Common:

```text
shadow-sm
shadow
shadow-md
shadow-lg
shadow-xl
shadow-2xl
```

---

# 23. Buttons

Example:

```html
<button class="bg-blue-500 text-white px-5 py-2 rounded-lg font-semibold">
  Login
</button>
```

Breakdown:

```text
bg-blue-500     → background
text-white      → text color
px-5            → horizontal padding
py-2            → vertical padding
rounded-lg      → rounded corners
font-semibold   → font weight
```

---

# 24. Hover

Use `hover:` before a class.

```html
<button class="bg-blue-500 hover:bg-blue-700 text-white">
  Hover Me
</button>
```

Meaning:

```text
Normal → blue-500
Hover  → blue-700
```

Other examples:

```html
<button class="hover:scale-105">
  Button
</button>
```

---

# 25. Focus

Useful for inputs:

```html
<input class="border focus:border-blue-500 outline-none">
```

`focus:` applies styles when the element is focused.

---

# 26. Transition

For smoother changes:

```html
<button class="transition duration-300 hover:bg-blue-700">
  Hover Me
</button>
```

Common:

```text
transition
duration-150
duration-300
duration-500
```

---

# 27. Transform

Examples:

```html
<div class="hover:scale-105">
  Card
</div>
```

Other utilities:

```text
scale-105
rotate-6
translate-x-2
translate-y-2
```

---

# 28. Position

Tailwind position utilities:

```text
static
relative
absolute
fixed
sticky
```

Example:

```html
<div class="relative">
  <span class="absolute top-2 right-2">
    Badge
  </span>
</div>
```

This is especially useful for badges, icons, overlays, etc.

---

# 29. Z-Index

```html
<div class="relative">
  <div class="absolute z-10">
    Above content
  </div>
</div>
```

Common:

```text
z-0
z-10
z-20
z-30
z-40
z-50
```

---

# 30. Responsive Design

This is one of the most important Tailwind concepts.

Tailwind uses responsive prefixes:

```text
sm:
md:
lg:
xl:
2xl:
```

Example:

```html
<div class="text-center md:text-left">
  Hello
</div>
```

Meaning:

```text
Small screen → text-center
md and above → text-left
```

---

# 31. Responsive Breakpoints

The default Tailwind breakpoints are commonly:

```text
sm → 640px
md → 768px
lg → 1024px
xl → 1280px
2xl → 1536px
```

Important concept:

Tailwind is generally **mobile-first**.

So:

```html
<div class="text-center md:text-left">
```

means:

```text
Default/mobile → center
md and larger → left
```

---

# 32. Responsive Grid Example

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
```

Meaning:

```text
Mobile  → 1 column
Tablet  → 2 columns
Desktop → 3 columns
```

This is a very common Tailwind pattern.

---

# 33. Responsive Flex Example

```html
<div class="flex flex-col md:flex-row">
```

Meaning:

```text
Mobile → column
md+    → row
```

---

# 34. Responsive Font Size

```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
  Hello
</h1>
```

Meaning:

```text
Mobile  → text-2xl
Tablet  → text-4xl
Desktop → text-6xl
```

---

# 35. Responsive Spacing

```html
<div class="p-4 md:p-8 lg:p-12">
```

Meaning:

```text
Mobile  → p-4
Tablet  → p-8
Desktop → p-12
```

---

# 36. Responsive Width

```html
<div class="w-full md:w-1/2 lg:w-1/3">
```

Meaning:

```text
Mobile  → 100%
Tablet  → 50%
Desktop → 33.33%
```

---

# 37. Container Pattern

A very common layout:

```html
<div class="max-w-7xl mx-auto px-4">
  Website content
</div>
```

Meaning:

```text
max-w-7xl → maximum width
mx-auto   → center horizontally
px-4      → horizontal padding
```

---

# 38. Images

Basic responsive image:

```html
<img src="image.jpg" class="w-full h-auto" alt="Image">
```

For fixed dimensions:

```html
<img src="image.jpg" class="w-64 h-64 object-cover" alt="Image">
```

Useful object utilities:

```text
object-cover
object-contain
object-fill
```

`object-cover` is especially common for cards.

---

# 39. Overflow

```text
overflow-hidden
overflow-auto
overflow-scroll
overflow-x-auto
overflow-y-auto
```

Example:

```html
<div class="overflow-hidden">
  Content
</div>
```

---

# 40. Cursor

```html
<button class="cursor-pointer">
  Click
</button>
```

Common:

```text
cursor-pointer
cursor-not-allowed
cursor-default
```

---

# 41. Opacity

```html
<div class="opacity-50">
  Semi transparent
</div>
```

Examples:

```text
opacity-0
opacity-25
opacity-50
opacity-75
opacity-100
```

---

# 42. Important `space-*` Utilities

Instead of manually adding margins between children:

```html
<div class="space-y-4">
  <p>One</p>
  <p>Two</p>
  <p>Three</p>
</div>
```

`space-y-4` adds vertical spacing between children.

Horizontal:

```html
<div class="space-x-4">
```

---

# 43. Arbitrary Values

Sometimes the default Tailwind values are not enough.

You can write custom values using square brackets:

```html
<div class="w-[430px]">
```

```html
<div class="bg-[#123456]">
```

```html
<div class="text-[22px]">
```

This gives you custom values without writing a separate CSS class.

---

# 44. Combining Classes

You can combine many utility classes:

```html
<div class="bg-white p-6 rounded-xl shadow-md max-w-md mx-auto">
  <h2 class="text-2xl font-bold text-gray-800">
    Hello
  </h2>

  <p class="mt-2 text-gray-600">
    Welcome to my website.
  </p>

  <button class="mt-4 bg-blue-500 hover:bg-blue-700 text-white px-5 py-2 rounded-lg transition">
    Learn More
  </button>
</div>
```

---

# 45. A Complete Responsive Card

```html
<div class="max-w-sm mx-auto bg-white rounded-xl shadow-lg overflow-hidden">

  <img
    src="image.jpg"
    class="w-full h-48 object-cover"
    alt="Card image"
  >

  <div class="p-6">
    <h2 class="text-2xl font-bold text-gray-800">
      Web Development
    </h2>

    <p class="mt-2 text-gray-600">
      Learn modern web development with HTML, CSS and JavaScript.
    </p>

    <button class="mt-4 bg-blue-500 hover:bg-blue-700 text-white px-5 py-2 rounded-lg transition">
      Learn More
    </button>
  </div>

</div>
```

---

# 46. Common Utility Cheat Sheet

## Spacing

```text
p-4       padding
px-4      padding left/right
py-4      padding top/bottom
m-4       margin
mx-auto   horizontal auto margin
mt-4      margin-top
mb-4      margin-bottom
gap-4     gap
```

## Typography

```text
text-lg
text-2xl
font-bold
font-semibold
text-center
text-gray-600
```

## Layout

```text
block
hidden
flex
grid
grid-cols-2
grid-cols-3
justify-center
justify-between
items-center
```

## Size

```text
w-full
w-1/2
w-1/3
h-screen
max-w-7xl
```

## Design

```text
bg-blue-500
border
border-gray-300
rounded-lg
rounded-full
shadow-md
opacity-50
```

## Position

```text
relative
absolute
fixed
sticky
top-0
right-0
bottom-0
left-0
z-10
```

## Interaction

```text
hover:
focus:
transition
duration-300
cursor-pointer
```

## Responsive

```text
sm:
md:
lg:
xl:
2xl:
```

---

# 47. Most Important Patterns to Memorize

### Center an element

```html
<div class="mx-auto">
```

### Center flex content

```html
<div class="flex justify-center items-center">
```

### Responsive columns

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
```

### Responsive flex

```html
<div class="flex flex-col md:flex-row">
```

### Responsive width

```html
<div class="w-full md:w-1/2 lg:w-1/3">
```

### Responsive text

```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
```

### Card

```html
<div class="bg-white p-6 rounded-xl shadow-md">
```

### Button

```html
<button class="bg-blue-500 hover:bg-blue-700 text-white px-5 py-2 rounded-lg">
```

### Absolute badge

```html
<div class="relative">
  <span class="absolute top-2 right-2 z-10">
    Most Popular
  </span>
</div>
```

---

# 48. Tailwind vs Normal CSS

Normal CSS:

```css
.card {
  background: white;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 10px #ddd;
}
```

Tailwind:

```html
<div class="bg-white p-6 rounded-xl shadow">
```

The CSS knowledge is still the same.

Tailwind simply provides ready-made utility classes.

---

# 49. Common Beginner Mistakes

### Mistake 1 — Forgetting mobile-first behavior

Wrong mindset:

```text
md = mobile
lg = tablet
```

Instead remember:

```text
Default = mobile/base style
sm = small breakpoint and above
md = medium breakpoint and above
lg = large breakpoint and above
```

### Mistake 2 — Using too many unnecessary classes

Don't add classes randomly. Each class should have a purpose.

### Mistake 3 — Forgetting `relative` for absolute children

Usually:

```html
<div class="relative">
  <span class="absolute top-0 right-0">
    Badge
  </span>
</div>
```

### Mistake 4 — Confusing `gap` and margin

Use `gap-*` for spacing between flex/grid children when appropriate.

### Mistake 5 — Forgetting `mx-auto`

For a max-width container:

```html
<div class="max-w-6xl mx-auto">
```

---

# 50. Final Revision Formula

Think of Tailwind in this order:

```text
Layout
↓
Spacing
↓
Size
↓
Typography
↓
Colors
↓
Border / Radius / Shadow
↓
Position
↓
Hover / Focus
↓
Responsive
```

Example:

```html
<div
  class="
    max-w-6xl mx-auto
    p-6
    bg-white
    rounded-xl shadow-md
    flex flex-col md:flex-row
    gap-6
  "
>
```

If you understand these basic utilities, you have a strong foundation for starting Tailwind projects.
