# Elite Layouts Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Elite Layouts landing page. This documentation is designed for beginners with no prior coding experience.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting Guide](#troubleshooting-guide)

---

## Getting Started

### What You'll Need

Before you begin customizing this landing page, you'll need:

- A text editor (we recommend **Visual Studio Code**, **Sublime Text**, or even **Notepad++**)
- The `index.html` file open in your editor
- Basic understanding of HTML tags (covered in this guide)
- A web browser to preview changes (Chrome, Firefox, Safari, or Edge)

### How to Open and Edit the File

1. **Locate your `index.html` file** on your computer
2. **Right-click** on the file and select "Open With" → choose your text editor
3. **Make your changes** in the text editor
4. **Save the file** using `Ctrl+S` (Windows) or `Cmd+S` (Mac)
5. **View changes** by opening the HTML file in your browser or refreshing the page

### Important: Never Delete Important Code

When editing, be careful to:
- ✅ Only change text between opening `<` and closing `>` tags
- ✅ Keep all HTML structure intact
- ❌ Don't remove any `<div>`, `<section>`, or closing `</div>` tags
- ❌ Don't delete CSS classes (the words in `class="..."`)

---

## Understanding the Page Structure

The landing page is organized into distinct sections. Here's what each section does:

### Page Sections Overview

| Section | Location | Purpose |
|---------|----------|---------|
| **Announcement Bar** | Top of page | Displays promotional message |
| **Header & Navigation** | Below announcement | Logo, menu, and CTA button |
| **Hero Section** | First full-screen area | Main headline and image |
| **Features Section** | Below hero | Three feature cards |
| **Benefits Section** | Middle of page | Three benefit sections with images |
| **About Section** | After benefits | Company information |
| **Testimonials Section** | After about | Client reviews |
| **FAQ Section** | After testimonials | Frequently asked questions |
| **CTA Section** | Near bottom | Final call-to-action |
| **Contact Section** | Before footer | Contact information |
| **Footer** | Bottom of page | Links, policies, social media |

### Finding Sections in Your Code

Each major section has an ID (identifier) that makes it easy to find. Search for these in your code:

```html
<section id="home">        <!-- Hero section -->
<section id="features">    <!-- Features section -->
<section id="benefits">    <!-- Benefits section -->
<section id="about">       <!-- About section -->
<section id="testimonials"><!-- Testimonials section -->
<section id="faq">         <!-- FAQ section -->
<section id="contact">     <!-- Contact section -->
```

**How to find a section:**
1. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac) to open the Find dialog
2. Type the ID name (e.g., `id="features"`)
3. Click "Next" to jump to that section

---

## Updating Text Content

This section explains how to change the words on your landing page while keeping everything else intact.

### Golden Rule of Text Editing

**Only change the text between the tags, never touch the tags themselves.**

Example:
```html
<!-- ✅ CORRECT - Only change the text -->
<h1>My New Headline Here</h1>

<!-- ❌ WRONG - Don't change the tags -->
<h1>My New Headline Here</h2>  <!-- Tag mismatch! -->
```

---

### 1. Updating the Announcement Bar

**Location:** Near the very top of the HTML file

**Current Code:**
```html
<div class="announcement-bar bg-gradient-to-r from-gray-900 to-gray-800 text-white py-3 px-4 text-center text-sm font-medium">
    <i class="fas fa-shipping-fast mr-2"></i>Fast Worldwide Shipping (5 days delivery) | 100% Satisfaction Guarantee
</div>
```

**How to Change It:**

1. Find the announcement bar text: `Fast Worldwide Shipping (5 days delivery) | 100% Satisfaction Guarantee`
2. Replace it with your message, for example:
   ```html
   <i class="fas fa-shipping-fast mr-2"></i>Get 20% Off Your First Website Design | Limited Time Offer
   ```

**Tips:**
- Keep the message short (under 80 characters)
- The `<i class="fas fa-shipping-fast mr-2"></i>` is an icon—you can change it to other icons (see [Icon Reference](#icon-reference) below)
- The `|` character separates two messages

---

### 2. Updating the Logo and Company Name

**Location:** In the header section

**Current Code:**
```html
<a href="#" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition duration-300">
    <i class="fas fa-code text-blue-600 mr-2"></i>Elite Layouts
</a>
```

**How to Change It:**

1. Replace `Elite Layouts` with your company name:
   ```html
   <i class="fas fa-code text-blue-600 mr-2"></i>Your Company Name
   ```

2. To change the icon, replace `fa-code` with a different icon (see [Icon Reference](#icon-reference))

---

### 3. Updating the Hero Section

**Location:** Search for `<section id="home">`

**Current Code:**
```html
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    South Africa's #1 Website Design Company
</h1>
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed max-w-3xl mx-auto font-light">
    Build your professional website today with confidence
</p>
```

**How to Change It:**

1. Replace the main headline:
   ```html
   <h1>Your New Headline Here</h1>
   ```

2. Replace the subheading:
   ```html
   <p>Your new subheading text here</p>
   ```

3. Replace the button text:
   ```html
   <a href="#" class="cta-button ...">
       Your Button Text Here
       <i class="fas fa-arrow-right ml-3"></i>
   </a>
   ```

**Example:**
```html
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Professional Web Design for Your Business
</h1>
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed max-w-3xl mx-auto font-light">
    Launch your online presence in just 4 weeks
</p>
```

---

### 4. Updating Feature Cards

**Location:** Search for `<section id="features">`

The Features section has three cards. Here's the structure:

**Current Code:**
```html
<!-- Feature 1 -->
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 shadow-md hover:shadow-xl">
    <div class="flex items-center justify-center w-14 h-14 bg-blue-100 rounded-lg mb-6">
        <i class="fas fa-palette text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Full-Service Web Design</h3>
    <p class="text-gray-600 leading-relaxed">
        From concept to launch, we handle every aspect...
    </p>
</div>
```

**How to Change Each Card:**

1. **Change the icon:**
   - Replace `fa-palette` with a different icon
   - Change `bg-blue-100` and `text-blue-600` to different colors (see [Color Reference](#color-reference))

2. **Change the title:**
   ```html
   <h3 class="text-xl font-bold text-gray-900 mb-3">Your New Title</h3>
   ```

3. **Change the description:**
   ```html
   <p class="text-gray-600 leading-relaxed">
       Your new description text here
   </p>
   ```

**Example:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 shadow-md hover:shadow-xl">
    <div class="flex items-center justify-center w-14 h-14 bg-green-100 rounded-lg mb-6">
        <i class="fas fa-rocket text-green-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Lightning Fast Development</h3>
    <p class="text-gray-600 leading-relaxed">
        Get your website live in record time with our agile development process.
    </p>
</div>
```

---

### 5. Updating Benefit Sections

**Location:** Search for `<section id="benefits">`

The Benefits section has three large blocks with images. Each one follows this pattern:

**Current Code (Benefit 1):**
```html
<div class="p-8 md:p-12 order-2 md:order-1">
    <h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4 leading-tight">
        Get Online Fast
    </h3>
    <p class="text-gray-600 text-lg leading-relaxed mb-6">
        Don't wait months to launch your online presence...
    </p>
    <ul class="space-y-3 mb-8">
        <li class="flex items-center text-gray-700">
            <i class="fas fa-check text-green-500 mr-3 font-bold"></i>
            Quick turnaround time
        </li>
        <li class="flex items-center text-gray-700">
            <i class="fas fa-check text-green-500 mr-3 font-bold"></i>
            Hassle-free setup
        </li>
        <li class="flex items-center text-gray-700">
            <i class="fas fa-check text-green-500 mr-3 font-bold"></i>
            Immediate online visibility
        </li>
    </ul>
</div>
```

**How to Change It:**

1. **Change the heading:**
   ```html
   <h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4 leading-tight">
       Your New Heading
   </h3>
   ```

2. **Change the description:**
   ```html
   <p class="text-gray-600 text-lg leading-relaxed mb-6">
       Your new description here
   </p>
   ```

3. **Update each bullet point:**
   ```html
   <li class="flex items-center text-gray-700">
       <i class="fas fa-check text-green-500 mr-3 font-bold"></i>
       Your new bullet point text
   </li>
   ```

4. **Change the button text:**
   ```html
   <a href="#" class="cta-button inline-flex items-center bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-semibold transition duration-300">
       Your Button Text
       <i class="fas fa-arrow-right ml-2"></i>
   </a>
   ```

---

### 6. Updating the About Section

**Location:** Search for `<section id="about">`

**Current Code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    About Elite Layouts
</h2>
<p class="text-xl text-gray-600 leading-relaxed">
    Discover the story behind South Africa's most trusted web design company
</p>
```

**How to Change It:**

1. **Update the main heading:**
   ```html
   <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
       About Your Company
   </h2>
   ```

2. **Update the subheading:**
   ```html
   <p class="text-xl text-gray-600 leading-relaxed">
       Your new subheading here
   </p>
   ```

3. **Update the story sections:**

   Look for the two large colored boxes:
   ```html
   <!-- First box (blue background) -->
   <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl p-8 md:p-12 border border-blue-100">
       <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Journey</h3>
       <p class="text-gray-700 leading-relaxed text-lg">
           Founded in 2015, Elite Layouts emerged from a simple vision...
       </p>
   </div>
   ```

   Replace with your content:
   ```html
   <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl p-8 md:p-12 border border-blue-100">
       <h3 class="text-2xl font-bold text-gray-900 mb-4">Your Section Title</h3>
       <p class="text-gray-700 leading-relaxed text-lg">
           Your company story here
       </p>
   </div>
   ```

4. **Update statistics at the bottom:**
   ```html
   <div class="text-center">
       <div class="text-4xl font-bold text-blue-600 mb-2">500+</div>
       <p class="text-gray-600 font-semibold">Projects Delivered</p>
   </div>
   ```

   Change to:
   ```html
   <div class="text-center">
       <div class="text-4xl font-bold text-blue-600 mb-2">YOUR NUMBER</div>
       <p class="text-gray-600 font-semibold">Your Statistic</p>
   </div>
   ```

---

### 7. Updating Testimonials

**Location:** Search for `<section id="testimonials">`

**Current Code (One Testimonial):**
```html
<div class="testimonial-card bg-white rounded-xl p-8 shadow-md border border-gray-200">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
        </div>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6 italic">
        "Elite Layouts transformed our online presence completely..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Mitchell</p>
        <p class="text-gray-600 text-sm">Marketing Director, TechVision Solutions</p>
    </div>
</div>
```

**How to Change It:**

1. **Adjust the star rating** (1-5 stars):
   - For 5 stars: Keep all 5 `<i class="fas fa-star star-rating"></i>`
   - For 4 stars: Remove one `<i class="fas fa-star star-rating"></i>`
   - For 3 stars: Remove two stars, etc.

2. **Update the testimonial text:**
   ```html
   <p class="text-gray-700 leading-relaxed mb-6 italic">
       "Your client's testimonial text here"
   </p>
   ```

3. **Update the client name:**
   ```html
   <p class="font-bold text-gray-900">Client Name</p>
   ```

4. **Update the client title and company:**
   ```html
   <p class="text-gray-600 text-sm">Job Title, Company Name</p>
   ```

---

### 8. Updating FAQ Questions and Answers

**Location:** Search for `<section id="faq">`

**Current Code (One FAQ Item):**
```html
<div class="faq-item border border-gray-200 rounded-lg overflow-hidden">
    <button class="faq-button w-full px-6 py-5 flex items-center justify-between bg-white hover:bg-gray-50 transition duration-300 text-left font-semibold text-gray-900">
        <span class="flex items-center">
            <i class="fas fa-question-circle text-blue-600 mr-3"></i>
            How long does it take to build a website?
        </span>
        <i class="fas fa-chevron-down faq-icon text-gray-600"></i>
    </button>
    <div class="faq-answer bg-gray-50 px-6 py-4">
        <p class="text-gray-700 leading-relaxed">
            Our rapid development process typically takes 4-8 weeks...
        </p>
    </div>
</div>
```

**How to Change It:**

1. **Update the question:**
   ```html
   <i class="fas fa-question-circle text-blue-600 mr-3"></i>
   Your new question here?
   ```

2. **Update the answer:**
   ```html
   <p class="text-gray-700 leading-relaxed">
       Your answer text here
   </p>
   ```

---

### 9. Updating Contact Information

**Location:** Search for `<section id="contact">`

**Current Code:**
```html
<div class="flex items-center text-white">
    <i class="fas fa-envelope text-blue-400 text-2xl mr-3"></i>
    <a href="mailto:info@elitelayouts.co.za" class="hover:text-blue-400 transition duration-300 font-semibold">
        info@elitelayouts.co.za
    </a>
</div>
<div class="flex items-center text-white">
    <i class="fas fa-phone text-blue-400 text-2xl mr-3"></i>
    <a href="tel:+27115551234" class="hover:text-blue-400 transition duration-300 font-semibold">
        +27 (11) 555-1234
    </a>
</div>
```

**How to Change It:**

1. **Update email:**
   ```html
   <a href="mailto:your-email@company.com" class="hover:text-blue-400 transition duration-300 font-semibold">
       your-email@company.com
   </a>
   ```

2. **Update phone:**
   ```html
   <a href="tel:+27115551234" class="hover:text-blue-400 transition duration-300 font-semibold">
       +27 (11) 555-1234
   </a>
   ```

   Note: Keep the `tel:+` format for phone links to work properly.

---

### 10. Updating Footer Information

**Location:** At the very bottom of the HTML file

**Current Code:**
```html
<h3 class="text-white font-bold text-lg mb-4 flex items-center">
    <i class="fas fa-code text-blue-400 mr-2"></i>Elite Layouts
</h3>
<p class="text-gray-400 leading-relaxed text-sm mb-4">
    South Africa's #1 website design company, creating stunning digital experiences that drive business growth.
</p>
```

**How to Change It:**

1. **Update company name:**
   ```html
   <h3 class="text-white font-bold text-lg mb-4 flex items-center">
       <i class="fas fa-code text-blue-400 mr-2"></i>Your Company Name
   </h3>
   ```

2. **Update company description:**
   ```html
   <p class="text-gray-400 leading-relaxed text-sm mb-4">
       Your company description here
   </p>
   ```

3. **Update copyright year:**
   ```html
   <p class="text-gray-400 text-sm">
       &copy; 2024 Your Company Name. All rights reserved.
   </p>
   ```

---

## Modifying Tailwind CSS Classes

Tailwind CSS uses descriptive class names to control the appearance of elements. This section explains how to modify these without breaking your design.

### What Are Tailwind CSS Classes?

Classes are the words inside `class="..."` that control how elements look. For example:

```html
<h1 class="text-4xl font-bold text-white">Headline</h1>
```

Breaking this down:
- `text-4xl` = Make text very large
- `font-bold` = Make text bold
- `text-white` = Make text white

### Important: Never Delete All Classes

**Always keep the class attribute intact.** Example:

```html
<!-- ✅ CORRECT -->
<h1 class="text-2xl font-bold text-blue-600">My Headline</h1>

<!-- ❌ WRONG - Don't remove the class attribute -->
<h1>My Headline</h1>
```

---

### Common Tailwind Classes Explained

#### Text Size Classes
```
text-sm      = Small text (12px)
text-base    = Normal text (16px)
text-lg      = Large text (18px)
text-xl      = Extra large (20px)
text-2xl     = 2x large (24px)
text-3xl     = 3x large (30px)
text-4xl     = 4x large (36px)
text-5xl     = 5x large (48px)
text-6xl     = 6x large (60px)
```

#### Text Color Classes
```
text-white       = White text
text-gray-600    = Medium gray text
text-gray-900    = Dark gray text
text-blue-600    = Blue text
text-green-500   = Green text
text-red-500     = Red text
```

#### Background Color Classes
```
bg-white         = White background
bg-gray-50       = Very light gray background
bg-gray-900      = Dark gray background
bg-blue-600      = Blue background
bg-green-100     = Light green background
```

#### Padding Classes (Space Inside)
```
p-4    = Small padding all around
p-6    = Medium padding all around
p-8    = Large padding all around
p-12   = Extra large padding all around
px-4   = Padding on left and right only
py-3   = Padding on top and bottom only
```

#### Margin Classes (Space Outside)
```
m-4    = Small margin all around
m-6    = Medium margin all around
m-8    = Large margin all around
mx-auto = Center horizontally
mb-4   = Margin below element
mb-6   = Larger margin below element
mt-2   = Small margin above element
```

#### Border Classes
```
border             = Add a border
border-gray-200    = Gray border
border-blue-100    = Light blue border
rounded-lg         = Slightly rounded corners
rounded-xl         = More rounded corners
```

#### Display Classes
```
flex               = Display as flexible container
grid               = Display as grid
hidden             = Hide element
block              = Display as block
inline-flex        = Display inline with flex properties
```

#### Responsive Classes
These prefixes make elements respond to screen size:

```
sm:  = On small screens (640px and up)
md:  = On medium screens (768px and up)
lg:  = On large screens (1024px and up)
```

**Example:**
```html
<h1 class="text-2xl md:text-4xl lg:text-5xl">
    Responsive Headline
</h1>
```

This means:
- On phones: Use `text-2xl` (24px)
- On tablets: Use `text-4xl` (36px)
- On desktops: Use `text-5xl` (48px)

---

### How to Modify Colors

#### Changing Text Color

**Original:**
```html
<p class="text-gray-600">Your text</p>
```

**To change to blue:**
```html
<p class="text-blue-600">Your text</p>
```

**Available color options:**
```
text-white        text-gray-400     text-blue-600
text-gray-50      text-gray-600     text-green-600
text-gray-100     text-gray-700     text-red-600
text-gray-200     text-gray-900     text-purple-600
text-gray-300
```

#### Changing Background Color

**Original:**
```html
<div class="bg-white">Content</div>
```

**To change to light blue:**
```html
<div class="bg-blue-50">Content</div>
```

**Available background colors:**
```
bg-white          bg-gray-100       bg-blue-50
bg-gray-50        bg-gray-200       bg-green-50
bg-gray-800       bg-gray-900       bg-red-50
```

---

### How to Change Button Styles

#### Location of Button Classes

Find buttons in these sections:
- Navigation: "Get Started" button
- Hero section: "Start Your Journey Today" button
- Benefits sections: "Get Started Now", "Learn More", "Partner With Us" buttons
- CTA section: "Get Your Free Consultation Today" button

#### Current Button Style
```html
<a href="#" class="cta-button bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-lg font-bold text-lg transition duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
    Button Text
    <i class="fas fa-arrow-right ml-3"></i>
</a>
```

#### Changing Button Color

**To make the button green:**
```html
<a href="#" class="cta-button bg-green-600 hover:bg-green-700 text-white px-8 py-4 rounded-lg font-bold text-lg transition duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
    Button Text
    <i class="fas fa-arrow-right ml-3"></i>
</a>
```

**To make the button red:**
```html
<a href="#" class="cta-button bg-red-600 hover:bg-red-700 text-white px-8 py-4 rounded-lg font-bold text-lg transition duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
    Button Text
    <i class="fas fa-arrow-right ml-3"></i>
</a>
```

**Understanding button classes:**
- `bg-blue-600` = Button background color
- `hover:bg-blue-700` = Darker color when you hover over it
- `text-white` = Button text color
- `px-8` = Horizontal padding (space inside left and right)
- `py-4` = Vertical padding (space inside top and bottom)
- `rounded-lg` = Rounded corners

---

### How to Change Section Background Colors

#### Hero Section Background

**Location:** Search for `<section id="home">`

The hero section uses an image with an overlay. To change the overlay color:

**Current:**
```html
<div class="hero-overlay">
    background: linear-gradient(135deg, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.3) 100%);
</div>
```

This creates a dark overlay. To make it lighter:
```html
background: linear-gradient(135deg, rgba(0, 0, 0, 0.3) 0%, rgba(0, 0, 0, 0.1) 100%);
```

To make it darker:
```html
background: linear-gradient(135deg, rgba(0, 0, 0, 0.7) 0%, rgba(0, 0, 0, 0.5) 100%);
```

#### Features Section Background

**Current:**
```html
<section id="features" class="py-24 px-4 sm:px-6 lg:px-8 bg-white">
```

**To change to light gray:**
```html
<section id="features" class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-50">
```

#### Benefits Section Background

**Current:**
```html
<section id="benefits" class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-50">
```

**To change to white:**
```html
<section id="benefits" class="py-24 px-4 sm:px-6 lg:px-8 bg-white">
```

---

### How to Change Spacing

#### Increase Padding (Space Inside Elements)

**Original:**
```html
<div class="p-8">Content</div>
```

**Increase to extra large:**
```html
<div class="p-12">Content</div>
```

**Padding options:**
```
p-4  = 1rem (16px)
p-6  = 1.5rem (24px)
p-8  = 2rem (32px)
p-12 = 3rem (48px)
```

#### Increase Margin (Space Outside Elements)

**Original:**
```html
<h2 class="mb-4">Heading</h2>
```

**Increase margin below:**
```html
<h2 class="mb-8">Heading</h2>
```

**Margin options:**
```
mb-4  = 1rem margin below (16px)
mb-6  = 1.5rem margin below (24px)
mb-8  = 2rem margin below (32px)
mb-12 = 3rem margin below (48px)
```

---

### How to Change Border Styles

#### Adding/Removing Borders

**Original (with border):**
```html
<div class="border border-gray-200">Content</div>
```

**To remove border:**
```html
<div>Content</div>
```

**To change border color:**
```html
<div class="border border-blue-200">Content</div>
```

#### Changing Border Radius (Rounded Corners)

**Original (slightly rounded):**
```html
<div class="rounded-lg">Content</div>
```

**More rounded:**
```html
<div class="rounded-xl">Content</div>
```

**Less rounded:**
```html
<div class="rounded-md">Content</div>
```

**Rounded options:**
```
rounded-md = Slightly rounded
rounded-lg = More rounded
rounded-xl = Very rounded
rounded-2xl = Extremely rounded
rounded-full = Completely round
```

---

### How to Change Box Shadows

#### Adding Shadows

**Original (small shadow):**
```html
<div class="shadow-md">Content</div>
```

**Larger shadow:**
```html
<div class="shadow-lg">Content</div>
```

**Shadow options:**
```
shadow-sm  = Small shadow
shadow-md  = Medium shadow
shadow-lg  = Large shadow
shadow-xl  = Extra large shadow
```

---

### Responsive Design: Mobile, Tablet, Desktop

The landing page automatically adjusts for different screen sizes. Here's how:

#### Understanding Responsive Prefixes

```html
<div class="text-2xl md:text-4xl lg:text-5xl">
    Responsive Text
</div>
```

This means:
- **Mobile phones** (small screens): `text-2xl` (24px)
- **Tablets** (medium screens): `md:text-4xl` (36px)
- **Desktops** (large screens): `lg:text-5xl` (48px)

#### Changing Responsive Behavior

**Original (shows on desktop, hides on mobile):**
```html
<nav class="hidden md:flex">
    Navigation Menu
</nav>
```

**To show on all devices:**
```html
<nav class="flex">
    Navigation Menu
</nav>
```

**To hide on all devices:**
```html
<nav class="hidden">
    Navigation Menu
</nav>
```

#### Common Responsive Patterns

```html
<!-- Hidden on mobile, shown on tablets and up -->
<div class="hidden md:block">Desktop Content</div>

<!-- Shown on mobile, hidden on tablets and up -->
<div class="md:hidden">Mobile Content</div>

<!-- Different padding on mobile vs desktop -->
<div class="px-4 md:px-8 lg:px-12">Content</div>

<!-- Different text size on mobile vs desktop -->
<h1 class="text-2xl md:text-4xl lg:text-5xl">Heading</h1>

<!-- Different grid columns on mobile vs desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
    <!-- 1 column on mobile, 2 on tablet, 3 on desktop -->
</div>
```

---

### Color Reference Chart

#### Text Colors
| Class | Color | Use For |
|-------|-------|---------|
| `text-white` | White | Text on dark backgrounds |
| `text-gray-900` | Dark Gray | Main text, headings |
| `text-gray-700` | Medium Gray | Body text |
| `text-gray-600` | Gray | Secondary text |
| `text-gray-400` | Light Gray | Muted text |
| `text-blue-600` | Blue | Links, highlights |
| `text-green-500` | Green | Success messages |
| `text-red-600` | Red | Errors, warnings |

#### Background Colors
| Class | Color | Use For |
|-------|-------|---------|
| `bg-white` | White | Main background |
| `bg-gray-50` | Very Light Gray | Section backgrounds |
| `bg-gray-900` | Dark Gray | Dark sections |
| `bg-blue-50` | Light Blue | Highlight boxes |
| `bg-green-50` | Light Green | Success boxes |

---

## Fixing and Managing Links

Links are essential for navigation. This section explains how to fix broken links and update them throughout your page.

### Understanding Links

A link has three main parts:

```html
<a href="https://example.com" class="text-blue-600">Click Here</a>
```

Breaking it down:
- `<a>` = Link tag (starts the link)
- `href="https://example.com"` = Where the link goes
- `Click Here` = The text users see and click
- `</a>` = Closes the link

### Types of Links

#### 1. External Links (Go to Another Website)
```html
<a href="https://www.google.com">Visit Google</a>
```

#### 2. Internal Links (Go to Another Page on Your Site)
```html
<a href="about.html">About Us</a>
```

#### 3. Anchor Links (Jump to a Section on Same Page)
```html
<a href="#features">Jump to Features</a>
```

#### 4. Email Links
```html
<a href="mailto:info@company.com">Send Email</a>
```

#### 5. Phone Links
```html
<a href="tel:+27115551234">Call Us</a>
```

---

### Finding All Links in Your Landing Page

Press `Ctrl+F` (Windows) or `Cmd+F` (Mac) and search for `href=` to find all links.

---

### Current Links in the Landing Page

Here's a complete list of all links that need to be reviewed:

#### Navigation Links (Header)

**Location:** In the `<header>` section

```html
<a href="#home" class="nav-link">Home</a>
<a href="#features" class="nav-link">Features</a>
<a href="#benefits" class="nav-link">Benefits</a>
<a href="#about" class="nav-link">About</a>
<a href="#testimonials" class="nav-link">Testimonials</a>
<a href="#faq" class="nav-link">FAQ</a>
<a href="#contact" class="nav-link">Contact</a>
```

**Status:** ✅ These are anchor links and work correctly. No changes needed.

#### CTA Buttons

**Location:** Multiple sections (Hero, Benefits, CTA section)

```html
<a href="#" class="cta-button">Start Your Journey Today</a>
<a href="#" class="cta-button">Get Started Now</a>
<a href="#" class="cta-button">Get Your Free Consultation Today</a>
```

**Status:** ❌ These use `href="#"` which is a placeholder. **You need to update these.**

**How to fix:**
```html
<!-- ❌ WRONG - Placeholder link -->
<a href="#" class="cta-button">Start Your Journey Today</a>

<!-- ✅ CORRECT - Link to your contact form or page -->
<a href="contact.html" class="cta-button">Start Your Journey Today</a>

<!-- OR link to an external form -->
<a href="https://forms.gle/yourformlink" class="cta-button">Start Your Journey Today</a>
```

#### Logo Link

**Location:** Header

```html
<a href="#" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-code text-blue-600 mr-2"></i>Elite Layouts
</a>
```

**Status:** ❌ This uses `href="#"` which is a placeholder.

**How to fix:**
```html
<!-- Link to home page -->
<a href="index.html" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-code text-blue-600 mr-2"></i>Elite Layouts
</a>

<!-- OR to homepage root -->
<a href="/" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-code text-blue-600 mr-2"></i>Elite Layouts
</a>
```

#### Footer Links

**Location:** Footer section at the bottom

**Quick Links:**
```html
<a href="#home">Home</a>
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#about">About Us</a>
<a href="#testimonials">Testimonials</a>
```

**Status:** ✅ These are anchor links and work correctly.

**Services:**
```html
<a href="#">Web Design</a>
<a href="#">Web Development</a>
<a href="#">Hosting & Domains</a>
<a href="#">SEO Services</a>
<a href="#">Digital Marketing</a>
```

**Status:** ❌ These are placeholders. Update them:

```html
<a href="services/web-design.html">Web Design</a>
<a href="services/web-development.html">Web Development</a>
<a href="services/hosting.html">Hosting & Domains</a>
<a href="services/seo.html">SEO Services</a>
<a href="services/marketing.html">Digital Marketing</a>
```

**Resources:**
```html
<a href="blog.html">Blog</a>
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="#contact">Contact Us</a>
<a href="#">Support</a>
```

**Status:** ⚠️ Partially broken. See [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages) section.

#### Contact Information

**Location:** Contact section and footer

**Email:**
```html
<a href="mailto:info@elitelayouts.co.za">info@elitelayouts.co.za</a>
```

**Status:** ✅ Works correctly, but update the email address.

**How to change:**
```html
<a href="mailto:your-email@company.com">your-email@company.com</a>
```

**Phone:**
```html
<a href="tel:+27115551234">+27 (11) 555-1234</a>
```

**Status:** ✅ Works correctly, but update the phone number.

**How to change:**
```html
<a href="tel:+27115551234">+27 (11) 555-1234</a>
```

Note: Keep the `tel:+` format for phone links to work properly.

#### Social Media Links

**Location:** Footer

```html
<a href="#"><i class="fab fa-facebook"></i></a>
<a href="#"><i class="fab fa-twitter"></i></a>
<a href="#"><i class="fab fa-linkedin"></i></a>
<a href="#"><i class="fab fa-instagram"></i></a>
```

**Status:** ❌ These are placeholders.

**How to fix:**
```html
<a href="https://www.facebook.com/yourpage">
    <i class="fab fa-facebook"></i>
</a>
<a href="https://www.twitter.com/yourhandle">
    <i class="fab fa-twitter"></i>
</a>
<a href="https://www.linkedin.com/company/yourcompany">
    <i class="fab fa-linkedin"></i>
</a>
<a href="https://www.instagram.com/yourhandle">
    <i class="fab fa-instagram"></i>
</a>
```

---

### Step-by-Step: Fixing All Links

#### Step 1: Fix CTA Buttons

**Find all CTA buttons:**

Press `Ctrl+F` and search for `class="cta-button"` to find all buttons.

**Update each one:**

```html
<!-- ❌ OLD -->
<a href="#" class="cta-button">Get Started Now</a>

<!-- ✅ NEW -->
<a href="contact.html" class="cta-button">Get Started Now</a>
```

**Locations to update:**
1. Hero section: "Start Your Journey Today"
2. First benefit: "Get Started Now"
3. Second benefit: "Learn More"
4. Third benefit: "Partner With Us"
5. CTA section: "Get Your Free Consultation Today"

#### Step 2: Fix the Logo Link

**Find:** Logo in header
```html
<a href="#" class="text-2xl font-bold text-gray-900">
```

**Change to:**
```html
<a href="index.html" class="text-2xl font-bold text-gray-900">
```

#### Step 3: Fix Service Links

**Find:** Footer Services section
```html
<a href="#">Web Design</a>
```

**Change to:**
```html
<a href="services/web-design.html">Web Design</a>
```

Do this for all service links.

#### Step 4: Fix Social Media Links

**Find:** Footer social media section
```html
<a href="#"><i class="fab fa-facebook"></i></a>
```

**Change to:**
```html
<a href="https://www.facebook.com/yourpage"><i class="fab fa-facebook"></i></a>
```

#### Step 5: Update Contact Information

**Email:**
```html
<!-- Find: -->
<a href="mailto:info@elitelayouts.co.za">info@elitelayouts.co.za</a>

<!-- Change to: -->
<a href="mailto:your-email@company.com">your-email@company.com</a>
```

**Phone:**
```html
<!-- Find: -->
<a href="tel:+27115551234">+27 (11) 555-1234</a>

<!-- Change to: -->
<a href="tel:+27115551234">+27 (11) 555-1234</a>
```

---

### Common Link Mistakes and How to Fix Them

#### Mistake 1: Forgetting the Protocol

**❌ Wrong:**
```html
<a href="www.google.com">Google</a>
```

**✅ Correct:**
```html
<a href="https://www.google.com">Google</a>
```

#### Mistake 2: Using `#` as a Placeholder

**❌ Wrong:**
```html
<a href="#">Click Here</a>
```

**✅ Correct:**
```html
<a href="page.html">Click Here</a>
```

#### Mistake 3: Wrong File Path

**❌ Wrong:**
```html
<a href="about.html">About</a>  <!-- If about.html is in a folder -->
```

**✅ Correct:**
```html
<a href="pages/about.html">About</a>  <!-- Correct path to folder -->
```

#### Mistake 4: Broken Anchor Links

**❌ Wrong:**
```html
<!-- Navigation link -->
<a href="#aboutus">About</a>

<!-- But the section is: -->
<section id="about">  <!-- ID doesn't match! -->
```

**✅ Correct:**
```html
<!-- Navigation link -->
<a href="#about">About</a>

<!-- Section -->
<section id="about">
```

---

### Testing Your Links

After updating links, test them:

1. **Open your HTML file in a browser**
2. **Click each link** to make sure it works
3. **Check that:**
   - External links open in the correct website
   - Internal links go to the correct page
   - Anchor links jump to the correct section
   - Email links open your email client
   - Phone links dial the number

---

## Linking Privacy and Terms Pages

This section provides detailed instructions for creating and linking Privacy Policy and Terms of Service pages.

### Understanding What You Need

You need three files:
1. `index.html` - Your main landing page (already have this)
2. `privacy.html` - Your Privacy Policy page (need to create)
3. `terms.html` - Your Terms of Service page (need to create)

All three files should be in the same folder.

---

### Step 1: Create the Privacy Policy Page

#### Create the File

1. Open your text editor
2. Click **File** → **New File**
3. Save it as `privacy.html` in the same folder as your `index.html`

#### Add Basic Structure

Paste this code into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Elite Layouts">
    <title>Privacy Policy | Elite Layouts</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <a href="index.html" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition duration-300">
                    <i class="fas fa-code text-blue-600 mr-2"></i>Elite Layouts
                </a>
                <a href="index.html" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-lg font-semibold transition duration-300">
                    Back to Home
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p class="text-lg leading-relaxed">
                    <strong>Last Updated:</strong> January 2024
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p class="leading-relaxed">
                    Elite Layouts ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p class="leading-relaxed">
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Personal Data: Name, email address, phone number</li>
                    <li>Device Data: Browser type, IP address, operating system</li>
                    <li>Usage Data: Pages visited, time spent on site, links clicked</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Your Information</h2>
                <p class="leading-relaxed">
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Generate a personal profile about you so that future visits to the Site are personalized</li>
                    <li>Increase the efficiency and operation of the Site</li>
                    <li>Monitor and analyze usage and trends to improve your experience</li>
                    <li>Notify you of updates to the Site</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p class="leading-relaxed">
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>By Law or to Protect Rights</li>
                    <li>Third-Party Service Providers</li>
                    <li>Business Transfers</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p class="leading-relaxed">
                    We use administrative, technical, and physical security measures to protect your personal information. However, perfect security does not exist on the Internet.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p class="leading-relaxed">
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p class="leading-relaxed">
                    <strong>Email:</strong> <a href="mailto:info@elitelayouts.co.za" class="text-blue-600 hover:text-blue-700">info@elitelayouts.co.za</a><br>
                    <strong>Phone:</strong> <a href="tel:+27115551234" class="text-blue-600 hover:text-blue-700">+27 (11) 555-1234</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 text-gray-300 py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    &copy; 2024 Elite Layouts. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

#### Create the File

1. Open your text editor
2. Click **File** → **New File**
3. Save it as `terms.html` in the same folder as your `index.html`

#### Add Basic Structure

Paste this code into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Elite Layouts">
    <title>Terms of Service | Elite Layouts</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <a href="index.html" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition duration-300">
                    <i class="fas fa-code text-blue-600 mr-2"></i>Elite Layouts
                </a>
                <a href="index.html" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-lg font-semibold transition duration-300">
                    Back to Home
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p class="text-lg leading-relaxed">
                    <strong>Last Updated:</strong> January 2024
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p class="leading-relaxed">
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p class="leading-relaxed">
                    Permission is granted to temporarily download one copy of the materials (information or software) on Elite Layouts' website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p class="leading-relaxed">
                    The materials on Elite Layouts' website are provided "as is". Elite Layouts makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p class="leading-relaxed">
                    In no event shall Elite Layouts or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Elite Layouts' website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p class="leading-relaxed">
                    The materials appearing on Elite Layouts' website could include technical, typographical, or photographic errors. Elite Layouts does not warrant that any of the materials on its website are accurate, complete, or current. Elite Layouts may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p class="leading-relaxed">
                    Elite Layouts has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Elite Layouts of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p class="leading-relaxed">
                    Elite Layouts may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p class="leading-relaxed">
                    These terms and conditions are governed by and construed in accordance with the laws of South Africa, and you irrevocably submit to the exclusive jurisdiction of the courts located in South Africa.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Us</h2>
                <p class="leading-relaxed">
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="leading-relaxed">
                    <strong>Email:</strong> <a href="mailto:info@elitelayouts.co.za" class="text-blue-600 hover:text-blue-700">info@elitelayouts.co.za</a><br>
                    <strong>Phone:</strong> <a href="tel:+27115551234" class="text-blue-600 hover:text-blue-700">+27 (11) 555-1234</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 text-gray-300 py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    &copy; 2024 Elite Layouts. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Update Links in index.html

Now you need to update your `index.html` to link to these new pages.

#### Update Footer Links

**Find this section in your `index.html`:**

```html
<li><a href="blog.html" class="text-gray-400 hover:text-blue-400 transition duration-300">Blog</a></li>
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition duration-300">Terms of Service</a></li>
<li><a href="#contact" class="text-gray-400 hover:text-blue-400 transition duration-300">Contact Us</a></li>
<li><a href="#" class="text-gray-400 hover:text-blue-400 transition duration-300">Support</a></li>
```

**Good news:** The links to `privacy.html` and `terms.html` are already correct! No changes needed here.

#### Check Footer Bottom Links

**Find this section:**

```html
<div class="flex justify-start md:justify-end gap-6 text-sm">
    <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition duration-300">Privacy Policy</a>
    <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition duration-300">Terms of Service</a>
    <a href="blog.html" class="text-gray-400 hover:text-blue-400 transition duration-300">Blog</a>
</div>
```

**Good news:** These links are already correct!

---

### Step 4: Verify File Structure

Your files should be organized like this:

```
your-website-folder/
├── index.html          (main landing page)
├── privacy.html        (privacy policy)
└── terms.html          (terms of service)
```

All three files must be in the same folder for the links to work.

---

### Step 5: Test the Links

1. **Open `index.html` in your browser**
2. **Scroll to the footer**
3. **Click on "Privacy Policy"** - Should open `privacy.html`
4. **Click on "Back to Home"** - Should return to `index.html`
5. **Repeat for "Terms of Service"**

---

### Customizing Privacy and Terms Pages

#### Update Company Information

In both `privacy.html` and `terms.html`, find and replace:

```html
<!-- OLD -->
<a href="mailto:info@elitelayouts.co.za">info@elitelayouts.co.za</a>
<a href="tel:+27115551234">+27 (11) 555-1234</a>

<!-- NEW -->
<a href="mailto:your-email@company.com">your-email@company.com</a>
<a href="tel:+27115551234">+27 (11) 555-1234</a>
```

#### Update Last Updated Date

In both files, find:

```html
<strong>Last Updated:</strong> January 2024
```

Change to your current date:

```html
<strong>Last Updated:</strong> January 2025
```

#### Add Your Specific Privacy Information

Customize the content to match your business. For example:

```html
<h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
<p class="leading-relaxed">
    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
</p>
<ul class="list-disc list-inside space-y-2">
    <li>Personal Data: Name, email address, phone number, company name</li>
    <li>Device Data: Browser type, IP address, operating system</li>
    <li>Usage Data: Pages visited, time spent on site, links clicked</li>
    <li>Payment Data: Credit card information (processed securely)</li>
</ul>
```

---

### Creating a Blog Page (Optional)

The footer references a `blog.html` file. If you want to create it:

1. Create a new file called `blog.html`
2. Use the same structure as `privacy.html` and `terms.html`
3. Add your blog content
4. Save in the same folder as `index.html`

---

## Common Customizations

This section covers the most common changes you'll want to make to personalize the landing page.

### 1. Changing the Hero Background Image

**Location:** Search for `<section id="home">`

**Current Code:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" alt="Web Design" class="w-full h-full object-cover">
```

**How to Change:**

1. Find a new image on Unsplash.com or Pexels.com
2. Copy the image URL
3. Replace the `src="..."` value:

```html
<img src="https://your-new-image-url.jpg" alt="Web Design" class="w-full h-full object-cover">
```

**Recommended image sizes:**
- Width: 1600px
- Height: 900px

---

### 2. Changing Benefit Section Images

**Location:** Search for `<section id="benefits">`

There are three benefit sections, each with an image:

```html
<img src="https://images.unsplash.com/photo-1556740714-a8395b3bf30f?w=800&h=600&fit=crop&q=80" alt="Get Online Fast" class="benefit-image w-full h-full object-cover">
```

**How to Change:**

1. Find new images on Unsplash.com or Pexels.com
2. Replace the `src="..."` value with your new image URL
3. Update the `alt="..."` text to describe your image

**Recommended image sizes:**
- Width: 800px
- Height: 600px

---

### 3. Changing the CTA Section Background Image

**Location:** Search for "Ready to Transform"

**Current Code:**
```html
<img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=1600&h=600&fit=crop&q=80" alt="Call to Action Background" class="w-full h-full object-cover">
```

**How to Change:**

```html
<img src="https://your-new-image-url.jpg" alt="Call to Action Background" class="w-full h-full object-cover">
```

---

### 4. Adding More Testimonials

**Location:** Search for `<section id="testimonials">`

**Current Structure (4 testimonials in a 2x2 grid):**
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
    <!-- Testimonial 1 -->
    <!-- Testimonial 2 -->
    <!-- Testimonial 3 -->
    <!-- Testimonial 4 -->
</div>
```

**To add a 5th testimonial:**

1. Copy one complete testimonial card:
```html
<div class="testimonial-card bg-white rounded-xl p-8 shadow-md border border-gray-200">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
        </div>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6 italic">
        "Your testimonial text here"
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Client Name</p>
        <p class="text-gray-600 text-sm">Job Title, Company Name</p>
    </div>
</div>
```

2. Paste it before the closing `</div>` of the grid

3. Update the text with the new testimonial

**To change to 3 columns:**

Change:
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

To:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

---

### 5. Adding More FAQ Items

**Location:** Search for `<section id="faq">`

**Current Structure:**
```html
<div class="space-y-4">
    <!-- FAQ Item 1 -->
    <!-- FAQ Item 2 -->
    <!-- FAQ Item 3 -->
    <!-- FAQ Item 4 -->
</div>
```

**To add a 5th FAQ:**

1. Copy one complete FAQ item:
```html
<div class="faq-item border border-gray-200 rounded-lg overflow-hidden">
    <button class="faq-button w-full px-6 py-5 flex items-center justify-between bg-white hover:bg-gray-50 transition duration-300 text-left font-semibold text-gray-900">
        <span class="flex items-center">
            <i class="fas fa-question-circle text-blue-600 mr-3"></i>
            Your question here?
        </span>
        <i class="fas fa-chevron-down faq-icon text-gray-600"></i>
    </button>
    <div class="faq-answer bg-gray-50 px-6 py-4">
        <p class="text-gray-700 leading-relaxed">
            Your answer text here
        </p>
    </div>
</div>
```

2. Paste it before the closing `</div>` of the space-y-4 container

3. Update the question and answer

---

### 6. Changing Brand Colors

**Current color scheme:** Blue (`#1f2937` → `#3b82f6`)

**To change all blue to green:**

1. Press `Ctrl+H` (or `Cmd+H` on Mac) to open Find and Replace
2. Find: `text-blue-600`
3. Replace with: `text-green-600`
4. Click "Replace All"

**Repeat for:**
- `bg-blue-600` → `bg-green-600`
- `hover:bg-blue-700` → `hover:bg-green-700`
- `bg-blue-100` → `bg-green-100`

---

### 7. Adding a Contact Form

**Location:** In the contact section or before the footer

**Simple Email Form:**
```html
<form method="POST" action="https://formspree.io/f/YOUR_FORM_ID" class="max-w-2xl mx-auto">
    <div class="mb-6">
        <label class="block text-gray-700 font-semibold mb-2">Name</label>
        <input type="text" name="name" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600">
    </div>
    
    <div class="mb-6">
        <label class="block text-gray-700 font-semibold mb-2">Email</label>
        <input type="email" name="email" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600">
    </div>
    
    <div class="mb-6">
        <label class="block text-gray-700 font-semibold mb-2">Message</label>
        <textarea name="message" rows="5" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600"></textarea>
    </div>
    
    <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg font-semibold transition duration-300">
        Send Message
    </button>
</form>
```

---

### 8. Adding Google Analytics

**Location:** In the `<head>` section, before `</head>`

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

Replace `GA_MEASUREMENT_ID` with your actual Google Analytics ID.

---

## Troubleshooting Guide

### Problem: Changes Don't Appear in Browser

**Solution:**
1. Save your HTML file (Ctrl+S or Cmd+S)
2. Refresh your browser (Ctrl+R or Cmd+R)
3. Hard refresh to clear cache (Ctrl+Shift+R or Cmd+Shift+R)

---

### Problem: Text Appears in Wrong Place

**Cause:** You accidentally deleted or moved HTML tags

**Solution:**
1. Undo your changes (Ctrl+Z or Cmd+Z)
2. Only change text between opening and closing tags
3. Never delete `<div>`, `</div>`, `<section>`, `</section>`, etc.

---

### Problem: Buttons Don't Work

**Cause:** Link `href` is broken or incorrect

**Solution:**
1. Check that the link starts with `http://` or `https://` for external links
2. Check that internal links point to correct files (e.g., `contact.html`)
3. Make sure the file exists in the same folder
4. Check for typos in the filename

---

### Problem: Images Don't Display

**Cause:** Image URL is broken or incorrect

**Solution:**
1. Check that the image URL is complete and correct
2. Try copying the image URL directly into your browser to test it
3. Use images from reliable sources (Unsplash, Pexels, Pixabay)
4. Ensure image URLs start with `http://` or `https://`

---

### Problem: Mobile Menu Doesn't Work

**Cause:** JavaScript isn't working or is broken

**Solution:**
1. Make sure you didn't delete the `<script>` section at the bottom
2. Check that all opening `<script>` tags have closing `</script>` tags
3. Ensure the JavaScript code is exactly as provided

---

### Problem: Styling Looks Wrong

**Cause:** Tailwind CSS classes are missing or incorrect

**Solution:**
1. Make sure you didn't delete any classes from `class="..."`
2. Check that class names are spelled correctly
3. Don't remove the `class=` attribute itself
4. Verify the CDN link is still in the `<head>`: `<script src="https://cdn.tailwindcss.com"></script>`

---

### Problem: Links Are Broken

**Cause:** File paths are incorrect or files don't exist

**Solution:**

**For internal links:**
1. Make sure all files are in the same folder
2. Use correct filenames (case-sensitive on some servers)
3. Example correct format: `href="about.html"` or `href="pages/about.html"`

**For external links:**
1. Always include `https://` at the beginning
2. Example correct format: `href="https://www.google.com"`

**For email links:**
1. Use format: `href="mailto:email@example.com"`

**For phone links:**
1. Use format: `href="tel:+27115551234"`

---

### Problem: Colors Don't Match

**Cause:** Tailwind class names are wrong

**Solution:**
1. Use correct color names: `blue`, `green`, `red`, `gray`, etc.
2. Use correct intensity: `50`, `100`, `200`, `600`, `700`, `900`
3. Example correct format: `text-blue-600` or `bg-gray-50`
4. Not: `text-blue` or `bg-grey-600`

---

### Problem: Spacing Is Off

**Cause:** Padding or margin classes are wrong

**Solution:**
1. Check padding classes: `p-4`, `p-8`, `p-12`
2. Check margin classes: `m-4`, `m-8`, `m-12`
3. Check directional classes: `px-4` (horizontal), `py-4` (vertical)
4. Use consistent spacing throughout

---

### Problem: Mobile View Looks Bad

**Cause:** Responsive classes are missing

**Solution:**
1. Check for responsive prefixes: `md:`, `lg:`, `sm:`
2. Example: `class="text-2xl md:text-4xl lg:text-5xl"`
3. Don't remove these prefixes when editing
4. Test on actual mobile devices or browser dev tools

---

## Icon Reference

The landing page uses Font Awesome icons. Here are common icons you can use:

### Navigation & General
```
fa-code          (Code icon - currently used for logo)
fa-arrow-right   (Arrow pointing right)
fa-search        (Search icon)
fa-bars          (Menu bars/hamburger)
fa-check         (Checkmark)
```

### Feature Icons
```
fa-palette       (Design/palette)
fa-server        (Hosting/server)
fa-bolt          (Speed/lightning)
fa-rocket        (Launch/fast)
fa-cog           (Settings/configuration)
fa-shield        (Security)
```

### Contact & Social
```
fa-envelope      (Email)
fa-phone         (Phone)
fa-facebook      (Facebook)
fa-twitter       (Twitter)
fa-linkedin      (LinkedIn)
fa-instagram     (Instagram)
```

### Other Useful Icons
```
fa-star          (Star rating)
fa-heart         (Heart/favorite)
fa-bell          (Notifications)
fa-lock          (Security)
fa-user          (User/profile)
fa-question-circle (Help/FAQ)
fa-chevron-down  (Dropdown arrow)
fa-shipping-fast (Shipping/delivery)
fa-undo          (Return/undo)
```

**How to use:**
```html
<i class="fas fa-code"></i>  <!-- Use the icon name -->
```

---

## Best Practices

### 1. Always Backup Before Major Changes
- Keep a copy of your original `index.html`
- Use version control (Git) if possible

### 2. Test Changes in Multiple Browsers
- Chrome
- Firefox
- Safari
- Edge
- Mobile browsers

### 3. Test on Mobile Devices
- Use browser dev tools (F12)
- Test on actual phones if possible
- Check all responsive sizes

### 4. Keep File Names Consistent
- Use lowercase filenames
- Use hyphens, not spaces: `privacy-policy.html` not `privacy policy.html`
- Keep all files in the same folder

### 5. Update Regularly
- Keep contact information current
- Update testimonials periodically
- Refresh images to keep content fresh
- Update "Last Updated" dates on policy pages

### 6. Monitor Links
- Test all links monthly
- Update broken external links
- Check that internal pages still exist

---

## Getting Help

If you're stuck, try these resources:

1. **Tailwind CSS Documentation:** https://tailwindcss.com/docs
2. **HTML Reference:** https://developer.mozilla.org/en-US/docs/Web/HTML
3. **Font Awesome Icons:** https://fontawesome.com/icons
4. **Unsplash Images:** https://unsplash.com
5. **Online HTML Validators:** https://validator.w3.org

---

## Summary

You now have a comprehensive guide to:

✅ Update text content throughout the page
✅ Modify Tailwind CSS classes for styling
✅ Fix and manage all links
✅ Create and link Privacy and Terms pages
✅ Make common customizations
✅ Troubleshoot common problems

Remember: **Always backup your files before making major changes, and test thoroughly in your browser before deploying.**

Good luck with your Elite Layouts landing page!