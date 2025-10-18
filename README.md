# Learn SEO Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Learn SEO landing page. This documentation is designed for developers of all skill levels, from beginners to experienced professionals.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Customizing Colors and Branding](#customizing-colors-and-branding)
8. [Managing Images](#managing-images)
9. [JavaScript Functionality](#javascript-functionality)
10. [Troubleshooting Common Issues](#troubleshooting-common-issues)
11. [SEO Best Practices](#seo-best-practices)
12. [Performance Optimization](#performance-optimization)

---

## Getting Started

### Prerequisites

Before you begin maintaining this landing page, you should have:

- A text editor (VS Code, Sublime Text, Notepad++, or even Notepad)
- Basic understanding of HTML tags and structure
- A web browser for testing changes
- FTP or file manager access to upload files to your server

### File Structure

Your Learn SEO landing page consists of:

```
project-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy Policy - needs to be created)
├── terms.html          (Terms of Service - needs to be created)
├── blog.html           (Blog page - needs to be created)
└── css/
    └── (Optional: custom CSS files)
```

### How to Edit the HTML File

1. **Locate the file**: Find `index.html` on your computer or server
2. **Open with text editor**: Right-click → "Open with" → Choose your text editor
3. **Make changes**: Edit the content as needed
4. **Save the file**: Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)
5. **Upload to server**: Use FTP or your hosting control panel to upload the updated file
6. **Refresh browser**: Visit your website and press `Ctrl+F5` to see changes (bypass cache)

---

## Understanding the Page Structure

### Main Sections of Your Landing Page

Your landing page is organized into the following sections:

| Section | ID | Purpose | Location in HTML |
|---------|----|---------|----|
| **Header/Navigation** | `<header>` | Site logo, menu links, mobile toggle | Lines 143-177 |
| **Hero Section** | `#home` | Main headline and call-to-action | Lines 179-212 |
| **Features Section** | `#features` | Course features and benefits | Lines 214-264 |
| **Benefits Section** | `#benefits` | Detailed benefit explanations | Lines 266-385 |
| **Video Section** | N/A | Embedded YouTube video | Lines 387-405 |
| **About Section** | `#about` | Company story and mission | Lines 407-455 |
| **Testimonials Section** | `#testimonials` | Student reviews and ratings | Lines 457-544 |
| **FAQ Section** | `#faq` | Frequently asked questions | Lines 546-620 |
| **CTA Section** | N/A | Call-to-action with enrollment link | Lines 622-650 |
| **Contact Section** | `#contact` | Contact information | Lines 652-707 |
| **Footer** | `<footer>` | Links, social media, copyright | Lines 709-825 |

### Key HTML Elements Explained

**Anchors (Navigation Links)**
```html
<a href="#features">Features</a>
```
- `href="#features"` - Links to the section with `id="features"`
- These create smooth scrolling to different parts of the page

**Section IDs**
```html
<section id="features">
```
- The `id` attribute is like a bookmark for that section
- Navigation links use these IDs to jump to sections

**Classes (Styling)**
```html
<div class="text-3xl md:text-4xl font-bold text-gray-900">
```
- Classes are instructions for how to style elements
- Multiple classes are separated by spaces
- We'll explain how to modify these in the Tailwind section

---

## Updating Text Content

### How Text Updates Work

Text content on your page is contained within HTML tags. To update text, you simply find the text you want to change and replace it, keeping the HTML tags intact.

### Step-by-Step: Updating Headline Text

**Example: Changing the Hero Section Headline**

**Current text (Line 188):**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">Learn SEO</h1>
```

**To change it to "Master SEO in 8 Weeks":**

1. Open `index.html` in your text editor
2. Find the line with `<h1 class="text-4xl...">Learn SEO</h1>`
3. Replace `Learn SEO` with `Master SEO in 8 Weeks`
4. Keep all the HTML tags exactly as they are
5. Your result should look like:
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">Master SEO in 8 Weeks</h1>
```

### Key Text Sections and Their Locations

#### 1. **Navigation Menu** (Lines 157-163)
```html
<a href="#home" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
<a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Benefits</a>
```
- **What to change**: The text between `>` and `</a>` (e.g., "Home", "Features")
- **What NOT to change**: The `href="#"` parts or class names
- **Note**: These menu items should match the section IDs on the page

#### 2. **Hero Section Main Headline** (Line 188)
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">Learn SEO</h1>
```
- **Change**: The text "Learn SEO"
- **Keep**: All the class attributes

#### 3. **Hero Section Subtitle** (Line 189)
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed max-w-3xl mx-auto">Learn SEO Today</p>
```
- **Change**: "Learn SEO Today"
- **Purpose**: This is the secondary headline

#### 4. **Hero Section Description** (Lines 190-191)
```html
<p class="text-lg md:text-xl text-gray-200 mb-12 leading-relaxed max-w-2xl mx-auto">Master search engine optimization at your own pace with our comprehensive, beginner-friendly modules designed to transform your digital presence.</p>
```
- **Change**: The entire paragraph text
- **Keep**: The `<p>` tags and class attributes

#### 5. **Button Text** (Lines 194-195)
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-lg shadow-lg transition-all duration-300">
    Start Learning Now
</a>
```
- **Change**: "Start Learning Now"
- **Keep**: The `href="https://seo.com"` and all class attributes

#### 6. **Feature Section Heading** (Line 217)
```html
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4 tracking-tight">Why Choose Our SEO Course?</h2>
```
- **Change**: "Why Choose Our SEO Course?"

#### 7. **Feature Cards** (Lines 228-244)
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">For Beginners</h3>
<p class="text-gray-600 leading-relaxed mb-4">Our course is specifically designed for beginners...</p>
```
- **Change**: Feature title and description
- **Keep**: HTML structure and classes

### Common Text Elements to Update

| Element | Location | Example |
|---------|----------|---------|
| Page Title | Line 11 | `<title>Learn SEO Today - Master Search Engine Optimization</title>` |
| Meta Description | Line 8 | `<meta name="description" content="...">` |
| Section Headings | Various | All `<h2>` and `<h3>` tags |
| Paragraphs | Various | All `<p>` tags |
| Button Text | Lines 194-195, 201-203, etc. | Text between `<a>` tags |
| Feature Descriptions | Lines 228-244, 253-269 | `<p>` tags inside feature cards |
| Testimonial Text | Lines 477-483, etc. | Quotes and reviewer names |
| FAQ Answers | Lines 559-564, etc. | Content inside accordion-content divs |

### Best Practices for Text Updates

✅ **DO:**
- Keep HTML tags exactly as they are
- Maintain proper spacing and line breaks
- Use consistent terminology throughout the page
- Test your changes in a browser before publishing

❌ **DON'T:**
- Delete or modify HTML tags
- Remove class attributes
- Change `href` attributes unless intentional
- Use special characters without proper encoding
- Delete closing tags like `</p>` or `</div>`

### Updating Meta Tags (SEO-Important Text)

Meta tags help search engines understand your page. Update these for your specific business:

**Page Title (Line 11):**
```html
<title>Learn SEO Today - Master Search Engine Optimization</title>
```
Change to your actual page title (keep under 60 characters).

**Meta Description (Line 8):**
```html
<meta name="description" content="Learn SEO Today - Master search engine optimization at your own pace with our comprehensive beginner-friendly modules.">
```
Change to your description (keep under 160 characters).

**Meta Keywords (Line 9):**
```html
<meta name="keywords" content="SEO, Search Engine Optimization, Learn SEO, Digital Marketing">
```
Change to relevant keywords for your business.

**Author (Line 10):**
```html
<meta name="author" content="Learn SEO">
```
Change to your company name.

---

## Modifying Tailwind CSS Classes

### What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework that uses predefined classes to style elements. Instead of writing custom CSS, you apply classes directly to HTML elements.

**Example:**
```html
<div class="text-3xl font-bold text-blue-600 mb-4">
```

- `text-3xl` = Makes text large (3xl size)
- `font-bold` = Makes text bold
- `text-blue-600` = Makes text blue (shade 600)
- `mb-4` = Adds margin (space) below the element

### Common Tailwind Classes Used in Your Page

#### Text Sizing Classes

| Class | Effect | Where Used |
|-------|--------|-----------|
| `text-sm` | Small text | Footer, small descriptions |
| `text-base` | Normal text | Body text |
| `text-lg` | Large text | Descriptions |
| `text-xl` | Extra large | Subheadings |
| `text-2xl` | 2x large | Section descriptions |
| `text-3xl` | 3x large | Medium headings |
| `text-4xl` | 4x large | Large headings |
| `text-5xl` | 5x large | Very large headings |
| `text-6xl` | 6x large | Hero section heading |

**Example - Changing Hero Headline Size:**

Current (Line 188):
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">Learn SEO</h1>
```

To make it smaller (text-3xl instead of text-4xl):
```html
<h1 class="text-3xl md:text-5xl font-bold text-white mb-6 leading-tight tracking-tight">Learn SEO</h1>
```

#### Font Weight Classes

| Class | Effect |
|-------|--------|
| `font-light` | Light/thin text |
| `font-normal` | Regular text |
| `font-semibold` | Semi-bold text |
| `font-bold` | Bold text |

**Example - Making text lighter:**

Current:
```html
<p class="text-gray-600 font-bold">Description</p>
```

Changed:
```html
<p class="text-gray-600 font-normal">Description</p>
```

#### Color Classes

Colors in Tailwind follow this pattern: `[property]-[color]-[shade]`

**Text Colors:**
```html
<p class="text-gray-900">Dark text</p>
<p class="text-blue-600">Blue text</p>
<p class="text-white">White text</p>
```

**Background Colors:**
```html
<div class="bg-blue-600">Blue background</div>
<div class="bg-gray-50">Light gray background</div>
<div class="bg-white">White background</div>
```

**Common Color Shades:**
- 50 = Very light
- 100 = Light
- 200 = Light-medium
- 600 = Medium
- 700 = Dark
- 900 = Very dark

**Example - Changing Feature Card Background:**

Current (Line 225):
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl">
```

To make it light blue:
```html
<div class="feature-card bg-blue-50 p-8 rounded-lg shadow-md hover:shadow-xl">
```

#### Spacing Classes

Tailwind uses a consistent spacing scale:

**Margin (Space Outside):**
- `m-4` = Margin on all sides
- `mb-4` = Margin bottom
- `mt-4` = Margin top
- `mx-4` = Margin left and right

**Padding (Space Inside):**
- `p-8` = Padding on all sides
- `px-4` = Padding left and right
- `py-6` = Padding top and bottom

**Values:** 0, 1, 2, 3, 4, 6, 8, 12, 16, 20, 24, 32, etc.

**Example - Adding more space around feature cards:**

Current (Line 225):
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl">
```

To add more padding:
```html
<div class="feature-card bg-white p-12 rounded-lg shadow-md hover:shadow-xl">
```

#### Responsive Design Classes

The `md:` prefix means "on medium screens and larger" (tablets and desktops).

**Example:**
```html
<h1 class="text-4xl md:text-6xl">
```
- On mobile: `text-4xl` (smaller)
- On tablets/desktop: `md:text-6xl` (larger)

**Common Breakpoints:**
- `sm:` = Small screens (640px+)
- `md:` = Medium screens (768px+)
- `lg:` = Large screens (1024px+)
- `xl:` = Extra large screens (1280px+)

**Example - Making a section full-width on mobile:**

Current:
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```
- Mobile: 1 column
- Tablet/Desktop: 2 columns

To make it 3 columns on large screens:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

#### Flexbox Classes

Flexbox helps arrange elements in rows or columns:

| Class | Effect |
|-------|--------|
| `flex` | Enable flexbox |
| `flex-row` | Arrange horizontally |
| `flex-col` | Arrange vertically |
| `items-center` | Vertically center items |
| `justify-center` | Horizontally center items |
| `justify-between` | Space items apart |
| `gap-4` | Space between items |

**Example - Centering button text:**

Current (Line 194):
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-lg shadow-lg transition-all duration-300">
```

This is already a button, but if you wanted to center content inside a flex container:
```html
<div class="flex items-center justify-center gap-4">
```

#### Border and Rounded Corner Classes

| Class | Effect |
|-------|--------|
| `border` | Add border |
| `border-gray-200` | Border color |
| `rounded-lg` | Slightly rounded corners |
| `rounded-full` | Completely rounded (circle) |

**Example - Changing feature card corners:**

Current (Line 225):
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl">
```

To make more rounded:
```html
<div class="feature-card bg-white p-8 rounded-2xl shadow-md hover:shadow-xl">
```

#### Shadow Classes

| Class | Effect |
|-------|--------|
| `shadow-sm` | Small shadow |
| `shadow-md` | Medium shadow |
| `shadow-lg` | Large shadow |
| `shadow-xl` | Extra large shadow |

**Example - Adding more shadow to a card:**

Current (Line 225):
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl">
```

To increase shadow:
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-lg hover:shadow-2xl">
```

### Step-by-Step: Changing Feature Card Styling

Let's make the feature cards have a light blue background and more rounded corners:

**Current code (Lines 225 and 252):**
```html
<div class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl">
```

**Step 1:** Find both feature card `<div>` tags (there are two)

**Step 2:** Identify what to change:
- `bg-white` = White background → Change to `bg-blue-50`
- `rounded-lg` = Slightly rounded → Change to `rounded-2xl`
- `shadow-md` = Medium shadow → Change to `shadow-lg`

**Step 3:** Apply changes:
```html
<div class="feature-card bg-blue-50 p-8 rounded-2xl shadow-lg hover:shadow-2xl">
```

**Step 4:** Save and refresh your browser to see the changes

### Step-by-Step: Changing Button Styling

Let's change the primary button color from blue to green:

**Current code (Line 194):**
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-lg shadow-lg transition-all duration-300">
```

**Step 1:** Find all buttons with `bg-blue-600` (there are several)

**Step 2:** Change the colors:
- `bg-blue-600` → `bg-green-600`
- `hover:bg-blue-700` → `hover:bg-green-700`

**Step 3:** Updated button:
```html
<a href="https://seo.com" class="btn-primary inline-block bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-8 rounded-lg shadow-lg transition-all duration-300">
```

**Step 4:** Find and update all similar buttons on the page

### Step-by-Step: Making Text Larger on Mobile

Let's increase paragraph text size on mobile devices:

**Current code (Line 190):**
```html
<p class="text-lg md:text-xl text-gray-200 mb-12 leading-relaxed max-w-2xl mx-auto">
```

**Step 1:** Identify the current mobile size: `text-lg`

**Step 2:** Make it larger: `text-lg` → `text-xl`

**Step 3:** Updated code:
```html
<p class="text-xl md:text-2xl text-gray-200 mb-12 leading-relaxed max-w-2xl mx-auto">
```

Now it's `text-xl` on mobile and `text-2xl` on larger screens.

### Tailwind Classes Quick Reference for Your Page

**Hero Section (Lines 188-191):**
```html
class="text-4xl md:text-6xl font-bold text-white mb-6"
```
- `text-4xl` = Mobile heading size
- `md:text-6xl` = Desktop heading size
- `font-bold` = Bold text
- `text-white` = White color
- `mb-6` = Space below

**Feature Card (Line 225):**
```html
class="feature-card bg-white p-8 rounded-lg shadow-md hover:shadow-xl"
```
- `bg-white` = White background
- `p-8` = Padding inside
- `rounded-lg` = Rounded corners
- `shadow-md` = Shadow effect
- `hover:shadow-xl` = Bigger shadow on hover

**Navigation (Line 157):**
```html
class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium"
```
- `text-gray-700` = Gray text
- `hover:text-blue-600` = Blue on hover
- `transition-colors` = Smooth color change
- `duration-300` = Animation speed (300ms)
- `font-medium` = Medium weight

### Common Tailwind Modifications Cheat Sheet

| Goal | Change This | To This |
|------|-------------|---------|
| Make text bigger | `text-lg` | `text-2xl` |
| Make text smaller | `text-2xl` | `text-lg` |
| Change background color | `bg-white` | `bg-blue-50` |
| Change text color | `text-gray-600` | `text-gray-900` |
| Add more space | `p-4` | `p-8` |
| Reduce space | `mb-12` | `mb-6` |
| Make corners rounder | `rounded-lg` | `rounded-2xl` |
| Add more shadow | `shadow-md` | `shadow-lg` |
| Make 2 columns on mobile | `grid-cols-1 md:grid-cols-2` | `grid-cols-2` |
| Change button color | `bg-blue-600` | `bg-green-600` |

---

## Fixing and Managing Links

### Understanding Links in Your Page

Your landing page contains two types of links:

1. **Internal Links** - Links to sections within the same page (using `#`)
2. **External Links** - Links to other websites (using `https://`)

### All Links in Your Page - Complete List

#### Navigation Menu Links (Lines 157-163)

**Desktop Menu:**
```html
<a href="#home" class="...">Home</a>
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#about" class="...">About</a>
<a href="#testimonials" class="...">Testimonials</a>
<a href="#faq" class="...">FAQ</a>
<a href="#contact" class="...">Contact</a>
```

**Mobile Menu (Lines 169-175):**
Same links are repeated for mobile menu.

**Status:** ✅ These links are correct - they link to sections on the page.

#### Hero Section Call-to-Action Buttons (Lines 194-203)

**Button 1 - "Start Learning Now":**
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600...">
    Start Learning Now
</a>
```

**Button 2 - "Learn More":**
```html
<a href="#features" class="btn-secondary inline-block bg-white...">
    Learn More
</a>
```

**Status:** ⚠️ `https://seo.com` is a placeholder - needs to be updated to your actual course URL.

#### Features Section Buttons

**Lines 245-248:** "Explore Modules" button
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600...">
    Explore Modules
</a>
```

**Status:** ⚠️ Placeholder URL needs updating.

#### Benefits Section Buttons

**Line 313:** "Start Learning Online" button
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600...">
    Start Learning Online
</a>
```

**Line 336:** "Join Our Community" button
```html
<a href="https://seo.com" class="btn-primary inline-block bg-blue-600...">
    Join Our Community
</a>
```

**Status:** ⚠️ Both need updating to your actual URLs.

#### CTA Section Buttons (Lines 643-653)

**Button 1 - "Enroll Now":**
```html
<a href="https://seo.com" class="btn-primary inline-block bg-white...">
    Enroll Now
</a>
```

**Button 2 - "Contact Us":**
```html
<a href="#contact" class="btn-secondary inline-block bg-blue-600...">
    Contact Us
</a>
```

**Status:** ⚠️ First button needs updating; second is correct.

#### Contact Section Links (Lines 665-679)

**Email Link:**
```html
<a href="mailto:admin@seo.com" class="text-blue-600 hover:text-blue-700 font-bold...">
    admin@seo.com
</a>
```

**Website Link:**
```html
<a href="https://seo.com" target="_blank" class="text-blue-600 hover:text-blue-700 font-bold...">
    https://seo.com
</a>
```

**Status:** ⚠️ Both need updating to your actual email and website.

#### Footer Links (Lines 747-770)

**Quick Links Section:**
```html
<a href="#home">Home</a>
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#about">About Us</a>
<a href="#testimonials">Testimonials</a>
```

**Status:** ✅ These are correct - they link to sections on the page.

**Resources Section:**
```html
<a href="blog.html">Blog</a>
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

**Status:** ⚠️ `blog.html`, `privacy.html`, and `terms.html` need to be created or updated.

**Contact Section in Footer:**
```html
<a href="mailto:admin@seo.com">admin@seo.com</a>
<a href="https://seo.com" target="_blank">https://seo.com</a>
```

**Status:** ⚠️ Both need updating.

**Bottom Footer Links (Lines 809-813):**
```html
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="blog.html">Blog</a>
```

**Status:** ⚠️ These pages need to be created.

### Step-by-Step: Updating Your Course URL

Let's update all instances of `https://seo.com` to your actual course platform URL. For this example, we'll use `https://learnseo.com/enroll`.

**Step 1: Find all occurrences**

Use your text editor's Find & Replace feature:
- **Windows:** Press `Ctrl+H`
- **Mac:** Press `Cmd+Option+F`

**Step 2: Enter search and replace values**

- **Find:** `https://seo.com`
- **Replace with:** `https://learnseo.com/enroll`

**Step 3: Review replacements**

The Find & Replace dialog will show you each match. Look for:
- Line 194: "Start Learning Now" button
- Line 245: "Explore Modules" button
- Line 313: "Start Learning Online" button
- Line 336: "Join Our Community" button
- Line 643: "Enroll Now" button
- Line 679: Website link in Contact section
- Line 799: Website link in Footer

**Step 4: Replace all**

Click "Replace All" to update all instances at once.

**Step 5: Verify changes**

Search for `https://seo.com` again to make sure none remain.

### Step-by-Step: Updating Your Email Address

Let's update all instances of `admin@seo.com` to your actual email.

**Step 1: Open Find & Replace**
- **Windows:** `Ctrl+H`
- **Mac:** `Cmd+Option+F`

**Step 2: Enter values**

- **Find:** `admin@seo.com`
- **Replace with:** `your-email@yourdomain.com`

**Step 3: Replace all**

This will update:
- Line 124: Meta author (optional)
- Line 593: FAQ answer
- Line 679: Contact section email link
- Line 799: Footer contact email

**Step 4: Save and test**

Save the file and test the email link by clicking it.

### Understanding href Attributes

The `href` attribute tells the browser where a link should go.

**Types of hrefs:**

1. **Internal page sections (anchor links):**
```html
<a href="#features">Features</a>
```
- Starts with `#`
- Links to an element with matching `id`
- No page reload needed

2. **External websites:**
```html
<a href="https://example.com">Visit Example</a>
```
- Full URL starting with `http://` or `https://`
- Opens in same tab by default

3. **Email links:**
```html
<a href="mailto:email@example.com">Email Us</a>
```
- Starts with `mailto:`
- Opens user's default email client

4. **Phone links:**
```html
<a href="tel:+1234567890">Call Us</a>
```
- Starts with `tel:`
- Opens phone dialer on mobile

5. **Other pages on your site:**
```html
<a href="privacy.html">Privacy Policy</a>
```
- Relative path (no domain needed)
- Links to file in same folder

### Verifying All Links Are Working

**Complete Link Verification Checklist:**

| Link | Current Value | Location | Status | Action Needed |
|------|---------------|----------|--------|---------------|
| Start Learning Now | `https://seo.com` | Line 194 | ⚠️ | Update to your course URL |
| Learn More | `#features` | Line 201 | ✅ | None |
| Explore Modules | `https://seo.com` | Line 245 | ⚠️ | Update to your course URL |
| Start Learning Online | `https://seo.com` | Line 313 | ⚠️ | Update to your course URL |
| Join Our Community | `https://seo.com` | Line 336 | ⚠️ | Update to your course URL |
| Enroll Now | `https://seo.com` | Line 643 | ⚠️ | Update to your course URL |
| Contact Us | `#contact` | Line 651 | ✅ | None |
| Blog | `blog.html` | Line 755 | ⚠️ | Create blog.html or update URL |
| Privacy Policy | `privacy.html` | Line 759 | ⚠️ | Create privacy.html |
| Terms of Service | `terms.html` | Line 763 | ⚠️ | Create terms.html |
| Email (Contact) | `mailto:admin@seo.com` | Line 679 | ⚠️ | Update to your email |
| Website (Contact) | `https://seo.com` | Line 683 | ⚠️ | Update to your website |
| Email (Footer) | `mailto:admin@seo.com` | Line 799 | ⚠️ | Update to your email |
| Website (Footer) | `https://seo.com` | Line 803 | ⚠️ | Update to your website |

### Troubleshooting Link Issues

**Problem: Link doesn't work or goes to wrong page**

1. Check the `href` value is correct
2. Make sure there are no typos in the URL
3. For internal links, verify the `id` matches exactly (case-sensitive)
4. For external links, verify the full URL including `https://`

**Problem: Email link doesn't open email client**

Make sure the link starts with `mailto:` exactly:
```html
<a href="mailto:your-email@example.com">Email Us</a>
```

**Problem: Navigation menu links don't scroll to sections**

Verify that:
1. The link has `href="#section-name"`
2. The section has matching `id="section-name"`
3. The id and href match exactly (case-sensitive)

**Example:**
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Must match exactly -->
<section id="features">
```

### Adding Links with target="_blank"

To open links in a new tab, add `target="_blank"`:

```html
<!-- Opens in same tab (default) -->
<a href="https://example.com">Visit</a>

<!-- Opens in new tab -->
<a href="https://example.com" target="_blank">Visit</a>
```

**When to use `target="_blank"`:**
- External website links
- Links to social media
- Links to partner websites

**Current page uses it for:**
- Line 683: Website link in Contact section
- Line 803: Website link in Footer

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

Privacy Policy and Terms of Service pages are:
- **Legal requirements** for many jurisdictions
- **Trust builders** for your audience
- **SEO-friendly** content
- **Referenced in your footer** and navigation

### Step 1: Creating the Privacy Policy Page

**Create a new file called `privacy.html` in the same folder as `index.html`**

Copy and paste this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Learn SEO">
    <meta name="robots" content="index, follow">
    <title>Privacy Policy - Learn SEO</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-graduation-cap text-blue-600 text-2xl"></i>
                <span class="text-2xl font-bold text-gray-900">Learn SEO</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg text-gray-600 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>Learn SEO ("we", "us", "our", or "Company") operates the Learn SEO website. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information Collection and Use</h2>
                <p>We collect several different types of information for various purposes to provide and improve our Service to you.</p>
                <h3 class="text-xl font-semibold text-gray-900 mt-4 mb-2">Types of Data Collected:</h3>
                <ul class="list-disc pl-6 space-y-2">
                    <li><strong>Personal Data:</strong> While using our Service, we may ask you to provide us with certain personally identifiable information that can be used to contact or identify you ("Personal Data"). This may include, but is not limited to:
                        <ul class="list-disc pl-6 mt-2 space-y-1">
                            <li>Email address</li>
                            <li>First name and last name</li>
                            <li>Phone number</li>
                            <li>Address, State, Province, ZIP/Postal code, City</li>
                            <li>Cookies and Usage Data</li>
                        </ul>
                    </li>
                    <li><strong>Usage Data:</strong> We may also collect information on how the Service is accessed and used ("Usage Data"). This may include information such as your computer's Internet Protocol address (e.g. IP address), browser type, browser version, the pages you visit, the time and date of your visit, the time spent on those pages, and other diagnostic data.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Data</h2>
                <p>Learn SEO uses the collected data for various purposes:</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>To provide and maintain the Service</li>
                    <li>To notify you about changes to our Service</li>
                    <li>To allow you to participate in interactive features of our Service when you choose to do so</li>
                    <li>To provide customer care and support</li>
                    <li>To gather analysis or valuable information so that we can improve the Service</li>
                    <li>To monitor the usage of the Service</li>
                    <li>To detect, prevent and address technical issues</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Security of Data</h2>
                <p>The security of your data is important to us, but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Changes to This Privacy Policy</h2>
                <p>We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "effective date" at the top of this Privacy Policy.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>If you have any questions about this Privacy Policy, please contact us at:</p>
                <p class="mt-2">
                    Email: <a href="mailto:admin@seo.com" class="text-blue-600 hover:text-blue-700">admin@seo.com</a><br>
                    Website: <a href="https://seo.com" class="text-blue-600 hover:text-blue-700">https://seo.com</a>
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 text-sm mb-4">
                    &copy; <span id="year"></span> Learn SEO. All rights reserved.
                </p>
                <div class="flex justify-center space-x-6">
                    <a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

### Step 2: Creating the Terms of Service Page

**Create a new file called `terms.html` in the same folder as `index.html`**

Copy and paste this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Learn SEO">
    <meta name="robots" content="index, follow">
    <title>Terms of Service - Learn SEO</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-graduation-cap text-blue-600 text-2xl"></i>
                <span class="text-2xl font-bold text-gray-900">Learn SEO</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg text-gray-600 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>By accessing and using the Learn SEO website and service, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>Permission is granted to temporarily download one copy of the materials (information or software) on Learn SEO for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the site</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>The materials on Learn SEO are provided on an 'as is' basis. Learn SEO makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>In no event shall Learn SEO or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Learn SEO, even if Learn SEO or an authorized representative has been notified orally or in writing of the possibility of such damage.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>The materials appearing on Learn SEO could include technical, typographical, or photographic errors. Learn SEO does not warrant that any of the materials on its website are accurate, complete, or current. Learn SEO may make changes to the materials contained on its website at any time without notice.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>Learn SEO has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Learn SEO of the site. Use of any such linked website is at the user's own risk.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>Learn SEO may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>These terms and conditions are governed by and construed in accordance with the laws of [Your Jurisdiction], and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Information</h2>
                <p>If you have any questions about these Terms of Service, please contact us at:</p>
                <p class="mt-2">
                    Email: <a href="mailto:admin@seo.com" class="text-blue-600 hover:text-blue-700">admin@seo.com</a><br>
                    Website: <a href="https://seo.com" class="text-blue-600 hover:text-blue-700">https://seo.com</a>
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 text-sm mb-4">
                    &copy; <span id="year"></span> Learn SEO. All rights reserved.
                </p>
                <div class="flex justify-center space-x-6">
                    <a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

### Step 3: Verify Links Work in index.html

The footer in `index.html` already has links to these pages. Verify they're in place:

**In the Footer (Lines 759-763):**
```html
<li>
    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
</li>
<li>
    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
</li>
```

**At the bottom of Footer (Lines 809-813):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
```

These links are already correct! ✅

### Step 4: Customize Your Privacy and Terms Pages

**In both `privacy.html` and `terms.html`, update:**

1. **Email address** (appears in Contact Us section):
```html
<!-- Find this -->
<a href="mailto:admin@seo.com" class="text-blue-600 hover:text-blue-700">admin@seo.com</a>

<!-- Change to your email -->
<a href="mailto:your-email@yourdomain.com" class="text-blue-600 hover:text-blue-700">your-email@yourdomain.com</a>
```

2. **Website URL** (appears in Contact Us section):
```html
<!-- Find this -->
<a href="https://seo.com" class="text-blue-600 hover:text-blue-700">https://seo.com</a>

<!-- Change to your website -->
<a href="https://yourdomain.com" class="text-blue-600 hover:text-blue-700">https://yourdomain.com</a>
```

3. **In terms.html only** - Governing Law (Line 94):
```html
<!-- Find this -->
<p>These terms and conditions are governed by and construed in accordance with the laws of [Your Jurisdiction], and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>

<!-- Change to your jurisdiction -->
<p>These terms and conditions are governed by and construed in accordance with the laws of California, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>
```

### Step 5: Upload Files to Your Server

1. Save `privacy.html` in the same folder as `index.html`
2. Save `terms.html` in the same folder as `index.html`
3. Upload both files to your web server using FTP or your hosting control panel

### Step 6: Test the Links

1. Visit your website in a browser
2. Scroll to the footer
3. Click "Privacy Policy" - should load `privacy.html`
4. Click "Terms of Service" - should load `terms.html`
5. Click "Back to Home" link on those pages - should return to `index.html`

### Optional: Create a Blog Page

If you want to create a blog page, follow the same process as above. Create a new file called `blog.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - Learn SEO">
    <meta name="robots" content="index, follow">
    <title>Blog - Learn SEO</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-graduation-cap text-blue-600 text-2xl"></i>
                <span class="text-2xl font-bold text-gray-900">Learn SEO</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Blog</h1>
        <p class="text-gray-600 text-lg">Blog content coming soon...</p>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 text-sm mb-4">
                    &copy; <span id="year"></span> Learn SEO. All rights reserved.
                </p>
                <div class="flex justify-center space-x-6">
                    <a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Home</a>
                    <a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Blog</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300 text-sm">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

---

## Customizing Colors and Branding

### Current Color Scheme

Your landing page uses the following colors:

| Element | Color | Tailwind Class | Hex Code |
|---------|-------|-----------------|----------|
| Primary Accent | Blue | `blue-600` | #2563eb |
| Primary Hover | Dark Blue | `blue-700` | #1d4ed8 |
| Text (Dark) | Gray | `gray-900` | #111827 |
| Text (Light) | Light Gray | `gray-200` | #e5e7eb |
| Background (Dark) | Dark Gray | `gray-900` | #111827 |
| Background (Light) | Off-white | `gray-50` | #f9fafb |
| Accents | Green | `green-500` | #10b981 |

### Tailwind Color Palette

Tailwind includes a comprehensive color palette. Common colors:

**Blues:**
- `blue-50` to `blue-900` (light to dark)
- `blue-600` is commonly used for primary actions

**Greens:**
- `green-50` to `green-900`
- `green-500` or `green-600` for accents

**Reds:**
- `red-50` to `red-900`
- Good for error messages or warnings

**Purples:**
- `purple-50` to `purple-900`
- Professional and modern

**Grays:**
- `gray-50` to `gray-900`
- Used for text and backgrounds

### Step-by-Step: Changing Primary Color from Blue to Green

Let's change all blue elements to green throughout the page.

**Step 1: Open Find & Replace** (`Ctrl+H` or `Cmd+Option+F`)

**Step 2: Replace blue-600 with green-600**
- Find: `bg-blue-600`
- Replace with: `bg-green-600`
- Replace all occurrences

**Step 3: Replace blue-700 with green-700**
- Find: `hover:bg-blue-700`
- Replace with: `hover:bg-green-700`
- Replace all occurrences

**Step 4: Replace text-blue-600 with text-green-600**
- Find: `text-blue-600`
- Replace with: `text-green-600`
- Replace all occurrences

**Step 5: Replace border colors if any**
- Find: `border-blue`
- Replace with: `border-green`

**Step 6: Update accent colors in CSS**

Find this section in the `<style>` tag (around line 41):
```html
.btn-primary:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 25px -5px rgba(59, 130, 246, 0.3);
}
```

Change the rgba values:
- `rgba(59, 130, 246, 0.3)` (blue shadow) to `rgba(16, 185, 129, 0.3)` (green shadow)

**Step 7: Test your changes**

Save and refresh your browser to see all blue elements turn green.

### Step-by-Step: Changing Primary Color from Blue to Purple

Follow the same process as above, but replace:
- `bg-blue-600` → `bg-purple-600`
- `bg-blue-700` → `bg-purple-700`
- `text-blue-600` → `text-purple-600`
- `text-blue-400` → `text-purple-400`

And update the shadow color in CSS:
- `rgba(59, 130, 246, 0.3)` → `rgba(147, 51, 234, 0.3)`

### Changing Icon Colors

Icons use the same color classes. To change icon colors:

**Current (Line 152):**
```html
<i class="fas fa-graduation-cap text-blue-600 text-2xl"></i>
```

**Change to green:**
```html
<i class="fas fa-graduation-cap text-green-600 text-2xl"></i>
```

### Changing Feature Card Icon Backgrounds

**Current (Line 232):**
```html
<div class="flex items-center justify-center w-16 h-16 bg-blue-100 rounded-lg mb-6">
    <i class="fas fa-users text-blue-600 text-2xl"></i>
</div>
```

**To change to green:**
```html
<div class="flex items-center justify-center w-16 h-16 bg-green-100 rounded-lg mb-6">
    <i class="fas fa-users text-green-600 text-2xl"></i>
</div>
```

### Changing Button Hover Effects

The button classes have custom CSS for hover effects. Find these in the `<style>` section:

```css
.btn-primary:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 25px -5px rgba(59, 130, 246, 0.3);
}
```

To change the shadow color:
1. Find the rgba color code
2. Replace with your new color's rgba value

**Common Color RGB Values:**
- Blue: `rgba(59, 130, 246, 0.3)`
- Green: `rgba(16, 185, 129, 0.3)`
- Purple: `rgba(147, 51, 234, 0.3)`
- Red: `rgba(239, 68, 68, 0.3)`

### Creating a Custom Brand Color

If you want to use a custom color not in Tailwind, you'll need to add custom CSS.

**Example: Using a custom teal color (#0d9488)**

1. Find the `<style>` section in your HTML
2. Add this custom class:

```css
.bg-custom-teal {
    background-color: #0d9488;
}

.text-custom-teal {
    color: #0d9488;
}

.hover\:bg-custom-teal:hover {
    background-color: #0f766e;
}
```

3. Use it in your HTML:
```html
<a href="#" class="bg-custom-teal hover:bg-custom-teal-dark text-white">Button</a>
```

### Brand Color Reference

| Brand | Primary Color | Hex | Tailwind Equivalent |
|-------|---------------|-----|-------------------|
| Facebook | Blue | #1877F2 | `blue-600` |
| LinkedIn | Blue | #0A66C2 | `blue-700` |
| Google | Blue | #4285F4 | `blue-500` |
| Apple | Black | #000000 | `gray-900` |
| Spotify | Green | #1DB954 | `green-500` |
| Twitter | Blue | #1DA1F2 | `blue-500` |
| Amazon | Orange | #FF9900 | `orange-500` |

---

## Managing Images

### Current Images in Your Page

Your landing page uses external images from Unsplash (a free image service). Here's where they're used:

| Location | Current URL | Purpose | Line |
|----------|------------|---------|------|
| Hero Background | `https://images.unsplash.com/photo-1516321318423-f06f70504504?w=1200&h=800&fit=crop` | Hero section background | 182 |
| Benefit 1 | `https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=400&fit=crop` | Module learning image | 291 |
| Benefit 2 | `https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=600&h=400&fit=crop` | Online platform image | 307 |