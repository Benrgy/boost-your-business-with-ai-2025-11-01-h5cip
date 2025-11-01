# AI Automation Bureau Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your AI Automation Bureau landing page. This document is designed for beginners with little to no coding experience.

---

## Table of Contents

1. [Overview](#overview)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Working with Tailwind CSS Classes](#working-with-tailwind-css-classes)
5. [Fixing Broken Links](#fixing-broken-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Common Issues & Troubleshooting](#common-issues--troubleshooting)
8. [Best Practices](#best-practices)

---

## Overview

Your landing page is built using:
- **HTML**: The structure and content of your page
- **Tailwind CSS**: A utility-based CSS framework that handles styling and responsive design
- **Font Awesome**: Icons (the robot icon, stars, checkmarks, etc.)
- **JavaScript**: Interactive features like the mobile menu

This guide will help you safely modify any part of the page without breaking its functionality.

---

## Understanding the Page Structure

### Main Sections

Your landing page contains the following major sections:

```
Header & Navigation (sticky at top)
    ↓
Hero Section (main banner with headline)
    ↓
Features Section (3 feature cards)
    ↓
Benefits Section (6 benefit items)
    ↓
Testimonials Section (4 client testimonials)
    ↓
About Section (company information)
    ↓
CTA Section (call-to-action banner)
    ↓
Footer (links and company info)
```

### File Organization

Your landing page consists of one main file:
- **index.html** - Contains all HTML, CSS, and JavaScript

**Related files you may need to create:**
- **privacy.html** - Privacy policy page
- **terms.html** - Terms of service page
- **blog.html** - Blog page (referenced in footer)

---

## Updating Text Content

### 1. Header & Navigation Text

**Location:** Lines 37-48 (Desktop Menu)

The header contains your logo and navigation menu. Here's how to update it:

#### Update the Logo Text

**Find this code:**
```html
<span class="text-xl font-bold text-black hidden sm:inline">AI Bureau</span>
```

**To change the logo text:**
1. Open `index.html` in a text editor
2. Find the line above
3. Replace `AI Bureau` with your company name
4. Save the file

**Example:**
```html
<!-- Before -->
<span class="text-xl font-bold text-black hidden sm:inline">AI Bureau</span>

<!-- After -->
<span class="text-xl font-bold text-black hidden sm:inline">AutoMate Solutions</span>
```

#### Update Navigation Menu Links

**Find this section (Lines 42-48):**
```html
<a href="#features" class="text-black font-semibold hover:text-gray-600...">Features</a>
<a href="#benefits" class="text-black font-semibold hover:text-gray-600...">Benefits</a>
<a href="#testimonials" class="text-black font-semibold hover:text-gray-600...">Testimonials</a>
<a href="#about" class="text-black font-semibold hover:text-gray-600...">About</a>
<a href="https://example.com" class="retro-button bg-black text-white...">Get Started</a>
```

**To change menu items:**
1. Change the text between `>` and `</a>` tags
2. Update the `href` attribute (the link destination)

**Example:**
```html
<!-- Before -->
<a href="#features" class="text-black font-semibold hover:text-gray-600...">Features</a>

<!-- After: Change text and link -->
<a href="#features" class="text-black font-semibold hover:text-gray-600...">Our Services</a>
```

### 2. Hero Section Text

**Location:** Lines 73-95

This is the main headline and description your visitors see first.

#### Update the Main Headline

**Find this code (Line 77):**
```html
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold text-black leading-tight tracking-tight">
    Boost Your Business with <span class="relative">
        <span class="relative z-2">AI</span>
        <span class="absolute -bottom-2 left-0 w-full h-4 bg-yellow-300 -z-1 border-2 border-black"></span>
    </span>
</h1>
```

**To update the headline:**
1. Keep the structure intact (all the `<span>` tags)
2. Change only the text: `Boost Your Business with`
3. Keep the `AI` highlighted (don't remove the inner `<span>` tags)

**Example:**
```html
<!-- Before -->
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold text-black leading-tight tracking-tight">
    Boost Your Business with <span class="relative">
        <span class="relative z-2">AI</span>
        ...
    </span>
</h1>

<!-- After -->
<h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold text-black leading-tight tracking-tight">
    Transform Your Workflow with <span class="relative">
        <span class="relative z-2">Automation</span>
        ...
    </span>
</h1>
```

#### Update the Hero Description

**Find this code (Lines 82-85):**
```html
<p class="text-lg sm:text-xl lg:text-2xl text-gray-700 max-w-3xl mx-auto leading-relaxed font-light">
    Small business, big automation. Our AI Automation Bureau simplifies sophisticated technology, making it accessible and impactful for startups and SMBs. Transform your operations without the complexity.
</p>
```

**To update the description:**
1. Find the paragraph (`<p>` tag)
2. Replace the text between `>` and `</p>`
3. Keep the class attributes unchanged

**Example:**
```html
<!-- Before -->
<p class="text-lg sm:text-xl lg:text-2xl text-gray-700 max-w-3xl mx-auto leading-relaxed font-light">
    Small business, big automation. Our AI Automation Bureau simplifies sophisticated technology, making it accessible and impactful for startups and SMBs. Transform your operations without the complexity.
</p>

<!-- After -->
<p class="text-lg sm:text-xl lg:text-2xl text-gray-700 max-w-3xl mx-auto leading-relaxed font-light">
    Streamline your business processes with intelligent automation. We help companies of all sizes work smarter, faster, and more efficiently.
</p>
```

#### Update Hero Button Text

**Find these lines (Lines 89-95):**
```html
<a href="https://example.com" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">
    Start Your Automation Journey
</a>
<button class="retro-button bg-white text-black px-8 py-4 font-bold text-lg border-4 border-black hover:bg-gray-100">
    Learn More
</button>
```

**To update button text:**
1. Change only the text between `>` and `</a>` or `</button>`
2. Keep all class names and attributes the same

**Example:**
```html
<!-- Before -->
<a href="https://example.com" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">
    Start Your Automation Journey
</a>

<!-- After -->
<a href="https://example.com" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">
    Get Started Free
</a>
```

#### Update Trust Badge Text

**Find this code (Lines 99-107):**
```html
<div class="pt-8 flex justify-center items-center space-x-2">
    <div class="flex space-x-1">
        <i class="fas fa-star text-yellow-500"></i>
        <!-- More stars... -->
    </div>
    <span class="text-black font-semibold">Trusted by 500+ businesses</span>
</div>
```

**To update the trust statement:**
1. Change the text in the `<span>` tag: `Trusted by 500+ businesses`
2. Keep the stars and structure intact

**Example:**
```html
<!-- Before -->
<span class="text-black font-semibold">Trusted by 500+ businesses</span>

<!-- After -->
<span class="text-black font-semibold">Used by 1000+ companies worldwide</span>
```

### 3. Features Section Text

**Location:** Lines 113-187

This section has three feature cards. Each card has a title, description, and bullet points.

#### Update Feature Card 1 (Budget-Friendly AI)

**Find this section (Lines 122-145):**
```html
<div class="retro-card bg-white p-8 border-4 border-black hover:shadow-2xl">
    <div class="w-16 h-16 bg-yellow-300 border-4 border-black rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-piggy-bank text-2xl text-black"></i>
    </div>
    <h3 class="text-2xl font-bold text-black mb-4">Budget-Friendly AI</h3>
    <p class="text-gray-700 mb-4 leading-relaxed">
        Enterprise-grade artificial intelligence without the enterprise-level price tag...
    </p>
    <ul class="space-y-2 text-gray-700">
        <li class="flex items-center space-x-2">
            <i class="fas fa-check text-black font-bold"></i>
            <span>No hidden fees or surprise charges</span>
        </li>
        <!-- More list items... -->
    </ul>
</div>
```

**To update the feature title:**
```html
<!-- Before -->
<h3 class="text-2xl font-bold text-black mb-4">Budget-Friendly AI</h3>

<!-- After -->
<h3 class="text-2xl font-bold text-black mb-4">Affordable Pricing</h3>
```

**To update the feature description:**
```html
<!-- Before -->
<p class="text-gray-700 mb-4 leading-relaxed">
    Enterprise-grade artificial intelligence without the enterprise-level price tag. Our flexible pricing models scale with your business, ensuring you only pay for what you use. Perfect for startups and SMBs looking to maximize ROI.
</p>

<!-- After -->
<p class="text-gray-700 mb-4 leading-relaxed">
    Get powerful automation tools at prices that work for your budget. Our flexible plans grow with your business, so you only pay for what you need.
</p>
```

**To update bullet points:**
```html
<!-- Before -->
<li class="flex items-center space-x-2">
    <i class="fas fa-check text-black font-bold"></i>
    <span>No hidden fees or surprise charges</span>
</li>

<!-- After -->
<li class="flex items-center space-x-2">
    <i class="fas fa-check text-black font-bold"></i>
    <span>Transparent pricing with no surprises</span>
</li>
```

**Repeat this process for Features 2 and 3** (located at approximately lines 147-170 and 172-195)

### 4. Benefits Section Text

**Location:** Lines 199-336

The benefits section has 6 benefit items with icons and descriptions.

#### Update Benefit 1 (Save 15+ Hours Per Week)

**Find this code (Lines 207-223):**
```html
<div class="flex gap-6 items-start">
    <div class="flex-shrink-0">
        <div class="w-14 h-14 bg-yellow-300 border-3 border-black rounded-full flex items-center justify-center">
            <i class="fas fa-clock text-2xl text-black font-bold"></i>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold text-black mb-3">Save 15+ Hours Per Week</h3>
        <p class="text-gray-700 leading-relaxed mb-3">
            Eliminate repetitive manual tasks and free up your team...
        </p>
        <p class="text-gray-600 text-sm">
            That's over 780 hours annually...
        </p>
    </div>
</div>
```

**To update the benefit title:**
```html
<!-- Before -->
<h3 class="text-2xl font-bold text-black mb-3">Save 15+ Hours Per Week</h3>

<!-- After -->
<h3 class="text-2xl font-bold text-black mb-3">Reclaim 20+ Hours Weekly</h3>
```

**To update the main benefit description:**
```html
<!-- Before -->
<p class="text-gray-700 leading-relaxed mb-3">
    Eliminate repetitive manual tasks and free up your team to focus on strategic, high-value work. Our clients report an average time savings of 15+ hours weekly within the first month.
</p>

<!-- After -->
<p class="text-gray-700 leading-relaxed mb-3">
    Automate repetitive work and let your team focus on what matters most. Experience significant productivity gains from day one.
</p>
```

**Repeat this process for Benefits 2-6** (approximately lines 225-336)

### 5. Testimonials Section Text

**Location:** Lines 355-432

Each testimonial card contains a quote, author name, and job title.

#### Update Testimonial 1

**Find this code (Lines 364-382):**
```html
<div class="retro-card bg-white p-8 border-4 border-black">
    <div class="flex items-center mb-4">
        <div class="flex space-x-1">
            <!-- Stars -->
        </div>
    </div>
    <p class="text-gray-700 text-lg mb-6 leading-relaxed">
        "This platform transformed how we handle customer data. We went from spending 8 hours daily on data entry to just 30 minutes..."
    </p>
    <div class="border-t-2 border-black pt-4">
        <p class="font-bold text-black text-lg">Sarah Chen</p>
        <p class="text-gray-600">Founder & CEO, TechStart Solutions</p>
    </div>
</div>
```

**To update the testimonial quote:**
```html
<!-- Before -->
<p class="text-gray-700 text-lg mb-6 leading-relaxed">
    "This platform transformed how we handle customer data. We went from spending 8 hours daily on data entry to just 30 minutes. The user-friendly interface meant our entire team was productive within hours of setup. Absolutely game-changing for our growing startup."
</p>

<!-- After -->
<p class="text-gray-700 text-lg mb-6 leading-relaxed">
    "We saw immediate results. The setup was simple, and our team was using it productively on day one. Highly recommended!"
</p>
```

**To update the author name:**
```html
<!-- Before -->
<p class="font-bold text-black text-lg">Sarah Chen</p>

<!-- After -->
<p class="font-bold text-black text-lg">John Smith</p>
```

**To update the author's title/company:**
```html
<!-- Before -->
<p class="text-gray-600">Founder & CEO, TechStart Solutions</p>

<!-- After -->
<p class="text-gray-600">CEO, Digital Innovations Inc.</p>
```

**Repeat for Testimonials 2-4** (approximately lines 384-432)

### 6. About Section Text

**Location:** Lines 447-478

The about section contains two paragraphs about your company.

#### Update Company History Paragraph

**Find this code (Lines 453-465):**
```html
<div class="retro-card bg-white p-8 border-4 border-black">
    <p class="text-lg text-gray-700 leading-relaxed mb-4">
        Founded in 2020 by a team of former enterprise automation consultants and software engineers, AI Automation Bureau emerged from a simple observation...
    </p>
    <p class="text-lg text-gray-700 leading-relaxed">
        Today, we're proud to serve over 500 businesses across 15 countries...
    </p>
</div>
```

**To update the first paragraph:**
```html
<!-- Before -->
<p class="text-lg text-gray-700 leading-relaxed mb-4">
    Founded in 2020 by a team of former enterprise automation consultants and software engineers, AI Automation Bureau emerged from a simple observation: powerful AI and automation technology existed, but it remained inaccessible to small businesses and startups.
</p>

<!-- After -->
<p class="text-lg text-gray-700 leading-relaxed mb-4">
    We started with a mission to make automation accessible to every business, regardless of size or budget. Since our founding, we've helped hundreds of companies streamline their operations and achieve their growth goals.
</p>
```

**To update the second paragraph:**
```html
<!-- Before -->
<p class="text-lg text-gray-700 leading-relaxed">
    Today, we're proud to serve over 500 businesses across 15 countries, from scrappy startups to established SMBs.
</p>

<!-- After -->
<p class="text-lg text-gray-700 leading-relaxed">
    Today, we continue to innovate and improve our platform based on customer feedback. Our team is dedicated to your success.
</p>
```

#### Update Mission & Values Paragraph

**Find this code (Lines 467-478):**
```html
<div class="retro-card bg-white p-8 border-4 border-black">
    <p class="text-lg text-gray-700 leading-relaxed mb-4">
        Our mission is to empower small businesses with AI-driven automation...
    </p>
    <p class="text-lg text-gray-700 leading-relaxed">
        Our core values guide everything we do...
    </p>
</div>
```

**Update similarly to the history section above.**

### 7. Footer Text

**Location:** Lines 524-587

The footer contains company info, links, and contact information.

#### Update Footer Logo/Brand

**Find this code (Lines 532-537):**
```html
<div class="flex items-center space-x-2 mb-4">
    <div class="w-10 h-10 bg-yellow-300 border-2 border-yellow-300 flex items-center justify-center">
        <i class="fas fa-robot text-black text-lg"></i>
    </div>
    <span class="text-xl font-bold">AI Bureau</span>
</div>
```

**To update the footer logo text:**
```html
<!-- Before -->
<span class="text-xl font-bold">AI Bureau</span>

<!-- After -->
<span class="text-xl font-bold">AutoMate Solutions</span>
```

#### Update Footer Description

**Find this code (Lines 538-541):**
```html
<p class="text-gray-400 text-sm leading-relaxed">
    Empowering small businesses with accessible AI automation technology.
</p>
```

**To update:**
```html
<!-- Before -->
<p class="text-gray-400 text-sm leading-relaxed">
    Empowering small businesses with accessible AI automation technology.
</p>

<!-- After -->
<p class="text-gray-400 text-sm leading-relaxed">
    Making business automation simple, affordable, and accessible for everyone.
</p>
```

#### Update Footer Contact Email

**Find this code (Line 581):**
```html
<p>Contact: <a href="mailto:bengrauwde@hotmail.com" class="text-yellow-300 hover:underline">bengrauwde@hotmail.com</a></p>
```

**To update your contact email:**
```html
<!-- Before -->
<a href="mailto:bengrauwde@hotmail.com" class="text-yellow-300 hover:underline">bengrauwde@hotmail.com</a>

<!-- After -->
<a href="mailto:your-email@yourcompany.com" class="text-yellow-300 hover:underline">your-email@yourcompany.com</a>
```

#### Update Copyright Year

**Find this code (Line 577):**
```html
<p class="text-gray-400 text-sm">
    &copy; 2025 AI Automation Bureau. All rights reserved.
</p>
```

**To update:**
```html
<!-- Before -->
&copy; 2025 AI Automation Bureau. All rights reserved.

<!-- After -->
&copy; 2025 Your Company Name. All rights reserved.
```

---

## Working with Tailwind CSS Classes

### What Are Tailwind CSS Classes?

Tailwind CSS is a utility-based framework that lets you style elements using predefined class names. Instead of writing custom CSS, you add classes directly to HTML elements.

**Example:**
```html
<!-- This creates a blue button with padding and rounded corners -->
<button class="bg-blue-500 px-4 py-2 rounded-lg text-white">Click Me</button>
```

### Understanding Common Tailwind Classes in Your Landing Page

#### Spacing Classes

These control padding and margins:

| Class | What It Does | Example |
|-------|-------------|---------|
| `p-8` | Padding (internal space) of 8 units | `<div class="p-8">` |
| `px-4` | Horizontal padding (left & right) | `<div class="px-4">` |
| `py-4` | Vertical padding (top & bottom) | `<div class="py-4">` |
| `mb-4` | Margin bottom (space below) | `<div class="mb-4">` |
| `mt-4` | Margin top (space above) | `<div class="mt-4">` |
| `space-x-2` | Space between horizontal items | `<div class="space-x-2">` |
| `gap-8` | Space between grid items | `<div class="gap-8">` |

#### Color Classes

These control text and background colors:

| Class | What It Does |
|-------|-------------|
| `text-black` | Black text |
| `text-white` | White text |
| `text-gray-700` | Dark gray text |
| `text-gray-400` | Light gray text |
| `bg-white` | White background |
| `bg-black` | Black background |
| `bg-yellow-300` | Yellow background |
| `bg-gray-50` | Very light gray background |

#### Text Classes

These control how text appears:

| Class | What It Does |
|-------|-------------|
| `text-xl` | Extra large text |
| `text-lg` | Large text |
| `text-sm` | Small text |
| `font-bold` | Bold text |
| `font-semibold` | Semi-bold text |
| `leading-relaxed` | More space between lines |
| `text-center` | Center text |

#### Display & Layout Classes

| Class | What It Does |
|-------|-------------|
| `flex` | Create a flexible layout |
| `grid` | Create a grid layout |
| `hidden` | Hide element |
| `block` | Display as block |
| `inline` | Display inline |
| `justify-between` | Space items apart |
| `items-center` | Center items vertically |

#### Responsive Classes

These apply styles only on certain screen sizes:

| Class | Screen Size | When It Applies |
|-------|------------|-----------------|
| `sm:` | Small (640px+) | Tablets and up |
| `md:` | Medium (768px+) | Larger tablets and up |
| `lg:` | Large (1024px+) | Desktops and up |
| `hidden md:flex` | Hidden on mobile, visible on tablets+ | Mobile-first design |

**Example:**
```html
<!-- This text is large on desktop, medium on tablets, small on mobile -->
<h1 class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl">My Headline</h1>
```

### Modifying Tailwind Classes in Your Landing Page

#### Changing Colors

**Example 1: Change button color**

**Find this code:**
```html
<a href="https://example.com" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">
    Start Your Automation Journey
</a>
```

**To change from black to blue:**
```html
<!-- Before: Black button -->
<a href="https://example.com" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">

<!-- After: Blue button -->
<a href="https://example.com" class="retro-button bg-blue-600 text-white px-8 py-4 font-bold text-lg hover:bg-blue-700 border-4 border-blue-600">
```

**Available colors:** `red`, `yellow`, `green`, `blue`, `purple`, `pink`, `orange`, `gray`, `black`, `white`

**Example 2: Change background color of a section**

**Find this code:**
```html
<section id="features" class="py-20 sm:py-24 lg:py-32 bg-white">
```

**To change to light gray:**
```html
<!-- Before -->
<section id="features" class="py-20 sm:py-24 lg:py-32 bg-white">

<!-- After -->
<section id="features" class="py-20 sm:py-24 lg:py-32 bg-gray-50">
```

#### Changing Spacing

**Example: Increase padding in a card**

**Find this code:**
```html
<div class="retro-card bg-white p-8 border-4 border-black">
```

**To increase padding:**
```html
<!-- Before: p-8 (32px padding) -->
<div class="retro-card bg-white p-8 border-4 border-black">

<!-- After: p-12 (48px padding) -->
<div class="retro-card bg-white p-12 border-4 border-black">
```

**Padding scale:** `p-4` (small), `p-6` (medium), `p-8` (large), `p-10` (larger), `p-12` (largest)

#### Changing Text Size

**Example: Make a heading larger**

**Find this code:**
```html
<h2 class="text-4xl sm:text-5xl font-bold text-black">Why Choose Our AI Automation?</h2>
```

**To make even larger:**
```html
<!-- Before -->
<h2 class="text-4xl sm:text-5xl font-bold text-black">

<!-- After -->
<h2 class="text-5xl sm:text-6xl font-bold text-black">
```

**Text size scale:** `text-sm` (small), `text-base` (normal), `text-lg` (large), `text-xl` (extra large), `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`, `text-7xl`

#### Changing Borders

**Example: Change border thickness**

**Find this code:**
```html
<div class="retro-card bg-white p-8 border-4 border-black">
```

**To make border thicker:**
```html
<!-- Before: border-4 (4px) -->
<div class="retro-card bg-white p-8 border-4 border-black">

<!-- After: border-8 (8px) -->
<div class="retro-card bg-white p-8 border-8 border-black">
```

**Border width options:** `border-2`, `border-4`, `border-8`

#### Changing Grid Columns

**Example: Change how many feature cards show per row**

**Find this code:**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 lg:gap-10">
```

This means:
- `grid-cols-1`: 1 column on mobile
- `md:grid-cols-3`: 3 columns on tablets and up
- `gap-8`: 8 units of space between items

**To change to 2 columns on tablets:**
```html
<!-- Before: 3 columns on tablets -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 lg:gap-10">

<!-- After: 2 columns on tablets -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-8 lg:gap-10">
```

### Responsive Design Best Practices

Your landing page uses a "mobile-first" approach. This means:

1. **Base classes apply to mobile** (smallest screens)
2. **Prefixed classes apply to larger screens** (`sm:`, `md:`, `lg:`)

**Example:**
```html
<div class="text-sm md:text-base lg:text-lg">
    Text is small on mobile, medium on tablets, large on desktop
</div>
```

**When modifying, always consider:**
- How it looks on mobile (base classes)
- How it looks on tablets (sm:, md:)
- How it looks on desktop (lg:)

---

## Fixing Broken Links

### Understanding Links in Your Landing Page

Links are created using the `<a>` tag with an `href` attribute:

```html
<a href="destination-url">Link Text</a>
```

### All Links in Your Landing Page

Here's a complete list of every link in your page:

#### Navigation Links (Header)

**Location:** Lines 42-48

```html
<!-- Desktop Navigation -->
<a href="#features">Features</a>           <!-- Links to features section -->
<a href="#benefits">Benefits</a>           <!-- Links to benefits section -->
<a href="#testimonials">Testimonials</a>   <!-- Links to testimonials section -->
<a href="#about">About</a>                 <!-- Links to about section -->
<a href="https://example.com">Get Started</a>  <!-- ⚠️ BROKEN - Replace with real URL -->
```

#### Mobile Navigation Links (Header)

**Location:** Lines 56-62

```html
<!-- Mobile Navigation -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#about">About</a>
<a href="https://example.com">Get Started</a>  <!-- ⚠️ BROKEN - Replace with real URL -->
```

#### Hero Section Links

**Location:** Lines 89-95

```html
<a href="https://example.com">Start Your Automation Journey</a>  <!-- ⚠️ BROKEN -->
<button>Learn More</button>  <!-- This is a button, not a link -->
```

#### CTA Section Links

**Location:** Lines 490-497

```html
<a href="https://example.com">Start Your Free Trial</a>  <!-- ⚠️ BROKEN -->
<button>Schedule a Demo</button>  <!-- This is a button, not a link -->
```

#### Footer Links - Product Column

**Location:** Lines 551-558

```html
<a href="#features">Features</a>           <!-- ✓ Works -->
<a href="#benefits">Benefits</a>           <!-- ✓ Works -->
<a href="#">Pricing</a>                    <!-- ⚠️ BROKEN - # goes nowhere -->
<a href="#">Integrations</a>               <!-- ⚠️ BROKEN -->
<a href="#">API Docs</a>                   <!-- ⚠️ BROKEN -->
```

#### Footer Links - Company Column

**Location:** Lines 561-568

```html
<a href="#about">About Us</a>              <!-- ✓ Works -->
<a href="blog.html">Blog</a>               <!-- ⚠️ BROKEN - blog.html doesn't exist yet -->
<a href="#">Careers</a>                    <!-- ⚠️ BROKEN -->
<a href="#">Press</a>                      <!-- ⚠️ BROKEN -->
<a href="#">Contact</a>                    <!-- ⚠️ BROKEN -->
```

#### Footer Links - Legal Column

**Location:** Lines 571-578

```html
<a href="privacy.html">Privacy Policy</a>  <!-- ⚠️ BROKEN - privacy.html doesn't exist yet -->
<a href="terms.html">Terms of Service</a>  <!-- ⚠️ BROKEN - terms.html doesn't exist yet -->
<a href="#">Cookie Policy</a>              <!-- ⚠️ BROKEN -->
<a href="#">Security</a>                   <!-- ⚠️ BROKEN -->
<a href="#">Accessibility</a>              <!-- ⚠️ BROKEN -->
```

#### Footer Social Links

**Location:** Lines 542-550

```html
<a href="#">Facebook</a>                   <!-- ⚠️ BROKEN -->
<a href="#">Twitter</a>                    <!-- ⚠️ BROKEN -->
<a href="#">LinkedIn</a>                   <!-- ⚠️ BROKEN -->
<a href="#">Instagram</a>                  <!-- ⚠️ BROKEN -->
```

#### Footer Contact Email

**Location:** Line 581

```html
<a href="mailto:bengrauwde@hotmail.com">bengrauwde@hotmail.com</a>  <!-- ✓ Works (email) -->
```

### How to Fix Broken Links

#### Step 1: Identify the Link

Find the broken link in the code. Look for `href="https://example.com"` or `href="#"`.

**Example:**
```html
<a href="https://example.com">Get Started</a>
```

#### Step 2: Determine the Correct URL

Decide what the link should point to:

- **Internal pages** (within your site): Use relative paths like `pricing.html` or `pages/pricing.html`
- **External websites**: Use full URLs like `https://www.yourwebsite.com/pricing`
- **Sections on current page**: Use `#section-id` like `#features`
- **Email**: Use `mailto:email@example.com`
- **Phone**: Use `tel:+1-555-0123`

#### Step 3: Replace the href Attribute

Replace the content inside `href=""` with the correct URL.

**Example:**
```html
<!-- Before: Broken link -->
<a href="https://example.com">Get Started</a>

<!-- After: Correct link -->
<a href="https://www.yourcompany.com/signup">Get Started</a>
```

### Fixing Specific Broken Links

#### Fix "Get Started" Buttons (Appears 3 times)

**Location 1: Line 48 (Desktop Navigation)**
```html
<!-- Before -->
<a href="https://example.com" class="retro-button bg-black text-white px-6 py-2 font-bold hover:bg-gray-800">Get Started</a>

<!-- After: Replace with your signup page -->
<a href="https://www.yourcompany.com/signup" class="retro-button bg-black text-white px-6 py-2 font-bold hover:bg-gray-800">Get Started</a>
```

**Location 2: Line 62 (Mobile Navigation)**
```html
<!-- Before -->
<a href="https://example.com" class="block retro-button bg-black text-white px-6 py-2 font-bold text-center mt-4">Get Started</a>

<!-- After -->
<a href="https://www.yourcompany.com/signup" class="block retro-button bg-black text-white px-6 py-2 font-bold text-center mt-4">Get Started</a>
```

**Location 3: Line 93 (Hero Section)**
```html
<!-- Before -->
<a href="https://example.com" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">
    Start Your Automation Journey
</a>

<!-- After -->
<a href="https://www.yourcompany.com/signup" class="retro-button bg-black text-white px-8 py-4 font-bold text-lg hover:bg-gray-800 border-4 border-black">
    Start Your Automation Journey
</a>
```

#### Fix Social Media Links (Footer)

**Location: Lines 542-550**

```html
<!-- Before: All broken -->
<a href="#" class="text-gray-400 hover:text-yellow-300 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- After: Add your social media URLs -->
<a href="https://www.facebook.com/yourcompany" class="text-gray-400 hover:text-yellow-300 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

**Replace with your social media URLs:**
- Facebook: `https://www.facebook.com/yourcompany`
- Twitter: `https://www.twitter.com/yourcompany`
- LinkedIn: `https://www.linkedin.com/company/yourcompany`
- Instagram: `https://www.instagram.com/yourcompany`

#### Fix Footer Product Links

**Location: Lines 551-558**

```html
<!-- Before -->
<li><a href="#">Pricing</a></li>
<li><a href="#">Integrations</a></li>
<li><a href="#">API Docs</a></li>

<!-- After: Create pages or link to external resources -->
<li><a href="pricing.html">Pricing</a></li>
<li><a href="integrations.html">Integrations</a></li>
<li><a href="https://docs.yourcompany.com">API Docs</a></li>
```

#### Fix Footer Company Links

**Location: Lines 561-568**

```html
<!-- Before -->
<li><a href="#">Careers</a></li>
<li><a href="#">Press</a></li>
<li><a href="#">Contact</a></li>

<!-- After -->
<li><a href="careers.html">Careers</a></li>
<li><a href="press.html">Press</a></li>
<li><a href="contact.html">Contact</a></li>
```

#### Fix Footer Legal Links

**Location: Lines 571-578**

```html
<!-- Before -->
<li><a href="#">Cookie Policy</a></li>
<li><a href="#">Security</a></li>
<li><a href="#">Accessibility</a></li>

<!-- After -->
<li><a href="cookies.html">Cookie Policy</a></li>
<li><a href="security.html">Security</a></li>
<li><a href="accessibility.html">Accessibility</a></li>
```

### Testing Your Links

After fixing links:

1. **Save your file** (Ctrl+S or Cmd+S)
2. **Open the page** in your browser
3. **Click each link** to verify it works
4. **Check that:**
   - Internal links scroll to the correct section
   - External links open in a new tab (if desired)
   - Email links open your email client
   - No broken links show 404 errors

---

## Linking Privacy and Terms Pages

### Step-by-Step Guide to Create and Link Privacy & Terms Pages

#### Step 1: Create the Privacy Policy Page

1. **Create a new file** named `privacy.html` in the same folder as `index.html`
2. **Copy this template** and paste it into `privacy.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - AI Automation Bureau">
    <meta name="author" content="AI Automation Bureau">
    <title>Privacy Policy - AI Automation Bureau</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Courier+Prime:wght@400;700&family=Space+Mono:wght@400;700&display=swap');
        
        body {
            font-family: 'Space Mono', monospace;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Courier Prime', monospace;
            font-weight: 700;
        }
        
        .retro-pattern {
            background-image: 
                repeating-linear-gradient(
                    45deg,
                    transparent,
                    transparent 10px,
                    rgba(0, 0, 0, 0.03) 10px,
                    rgba(0, 0, 0, 0.03) 20px
                );
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white border-b-4 border-black retro-pattern">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo -->
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-black border-2 border-black flex items-center justify-center">
                    <i class="fas fa-robot text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-black hidden sm:inline">AI Bureau</a>
            </div>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-black font-semibold hover:text-gray-600 transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-black font-semibold hover:text-gray-600 transition-colors duration-300">Features</a>
                <a href="index.html" class="text-black font-semibold hover:text-gray-600 transition-colors duration-300 border-b-2 border-black">Back to Home</a>
            </div>

            <!-- Mobile Menu Button -->
            <button class="md:hidden mobile-menu-button text-black text-2xl p-2 hover:bg-gray-100 transition-colors duration-300 border-2 border-black rounded" aria-label="Toggle mobile menu">
                <i class="fas fa-bars"></i>
            </button>
        </nav>

        <!-- Mobile Menu -->
        <div class="mobile-menu hidden md:hidden border-t-4 border-black bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 space-y-3">
                <a href="index.html" class="block text-black font-semibold py-2 px-3 hover:bg-gray-100 transition-colors duration-300">Home</a>
                <a href="index.html#features" class="block text-black font-semibold py-2 px-3 hover:bg-gray-100 transition-colors duration-300">Features</a>
            </div>
        </div>
    </header>

    <!-- Content Section -->
    <section class="py-20 sm:py-24 lg:py-32 bg-white">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold text-black mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none space-y-6 text-gray-700">
                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">1. Introduction</h2>
                    <p>
                        AI Automation Bureau ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">2. Information We Collect</h2>
                    <p>We may collect information about you in a variety of ways. The information we may collect on the site includes:</p>
                    <ul class="list-disc list-inside space-y-2">
                        <li><strong>Personal Data:</strong> Name, email address, phone number, and other identifying information you provide.</li>
                        <li><strong>Usage Data:</strong> Information about how you interact with our website, including IP address, browser type, and pages visited.</li>
                        <li><strong>Cookies:</strong> We use cookies and similar tracking technologies to track activity on our website.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">3. Use of Your Information</h2>
                    <p>Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the site to:</p>
                    <ul class="list-disc list-inside space-y-2">
                        <li>Generate a personal profile about you so that future visits to the site will be personalized.</li>
                        <li>Increase the efficiency and operation of the site.</li>
                        <li>Monitor and analyze usage and trends to improve your experience with the site.</li>
                        <li>Process your transactions and send you related information.</li>
                        <li>Notify you about updates to the site.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">4. Disclosure of Your Information</h2>
                    <p>We may share information we have collected about you in certain situations:</p>
                    <ul class="list-disc list-inside space-y-2">
                        <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information is necessary to comply with the law.</li>
                        <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties who perform services for us.</li>
                        <li><strong>Business Transfers:</strong> If we are involved in a merger, acquisition, or asset sale, your information may be transferred.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">5. Security of Your Information</h2>
                    <p>
                        We use administrative, technical, and physical security measures to help protect your personal information. While we have taken reasonable steps to secure the personal information you provide to us, please be aware that no security measures are perfect or impenetrable.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">6. Contact Us</h2>
                    <p>
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-2">
                        <strong>Email:</strong> <a href="mailto:privacy@yourcompany.com" class="text-blue-600 hover:underline">privacy@yourcompany.com</a>
                    </p>
                </div>

                <div class="mt-8 p-4 bg-gray-50 border-2 border-black">
                    <p class="text-sm text-gray-600">
                        <strong>Last Updated:</strong> January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-white border-t-4 border-yellow-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    &copy; 2025 AI Automation Bureau. All rights reserved.
                </p>
                <a href="index.html" class="text-yellow-300 hover:underline">Back to Home</a>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

3. **Save the file** as `privacy.html` in the same folder as `index.html`

#### Step 2: Create the Terms of Service Page

1. **Create a new file** named `terms.html` in the same folder as `index.html`
2. **Copy this template** and paste it into `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - AI Automation Bureau">
    <meta name="author" content="AI Automation Bureau">
    <title>Terms of Service - AI Automation Bureau</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Courier+Prime:wght@400;700&family=Space+Mono:wght@400;700&display=swap');
        
        body {
            font-family: 'Space Mono', monospace;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Courier Prime', monospace;
            font-weight: 700;
        }
        
        .retro-pattern {
            background-image: 
                repeating-linear-gradient(
                    45deg,
                    transparent,
                    transparent 10px,
                    rgba(0, 0, 0, 0.03) 10px,
                    rgba(0, 0, 0, 0.03) 20px
                );
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white border-b-4 border-black retro-pattern">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo -->
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-black border-2 border-black flex items-center justify-center">
                    <i class="fas fa-robot text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-black hidden sm:inline">AI Bureau</a>
            </div>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-black font-semibold hover:text-gray-600 transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-black font-semibold hover:text-gray-600 transition-colors duration-300">Features</a>
                <a href="index.html" class="text-black font-semibold hover:text-gray-600 transition-colors duration-300 border-b-2 border-black">Back to Home</a>
            </div>

            <!-- Mobile Menu Button -->
            <button class="md:hidden mobile-menu-button text-black text-2xl p-2 hover:bg-gray-100 transition-colors duration-300 border-2 border-black rounded" aria-label="Toggle mobile menu">
                <i class="fas fa-bars"></i>
            </button>
        </nav>

        <!-- Mobile Menu -->
        <div class="mobile-menu hidden md:hidden border-t-4 border-black bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 space-y-3">
                <a href="index.html" class="block text-black font-semibold py-2 px-3 hover:bg-gray-100 transition-colors duration-300">Home</a>
                <a href="index.html#features" class="block text-black font-semibold py-2 px-3 hover:bg-gray-100 transition-colors duration-300">Features</a>
            </div>
        </div>
    </header>

    <!-- Content Section -->
    <section class="py-20 sm:py-24 lg:py-32 bg-white">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold text-black mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none space-y-6 text-gray-700">
                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">1. Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on AI Automation Bureau's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on AI Automation Bureau's website are provided on an 'as is' basis. AI Automation Bureau makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">4. Limitations</h2>
                    <p>
                        In no event shall AI Automation Bureau or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on AI Automation Bureau's website could include technical, typographical, or photographic errors. AI Automation Bureau does not warrant that any of the materials on the website are accurate, complete, or current. AI Automation Bureau may make changes to the materials contained on the website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">6. Links</h2>
                    <p>
                        AI Automation Bureau has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by AI Automation Bureau of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">7. Modifications</h2>
                    <p>
                        AI Automation Bureau may revise these terms of service for the website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-black mb-4">8. Contact Us</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-2">
                        <strong>Email:</strong> <a href="mailto:legal@yourcompany.com" class="text-blue-600 hover:underline">legal@yourcompany.com</a>
                    </p>
                </div>

                <div class="mt-8 p-4 bg-gray-50 border-2 border-black">
                    <p class="text-sm text-gray-600">
                        <strong>Last Updated:</strong> January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-white border-t-4 border-yellow-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    &copy; 2025 AI Automation Bureau. All rights reserved.
                </p>
                <a href="index.html" class="text-yellow-300 hover:underline">Back to Home</a>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

3. **Save the file** as `terms.html` in the same folder as `index.html`

#### Step 3: Verify Links Are Already in Your Footer

**Good news!** Your `index.html` already has the correct links to these pages in the footer. Here's where they are:

**Location: Lines 571-578**

```html
<li><a href="privacy.html" class="hover:text-yellow-300 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-yellow-300 transition-colors duration-300">Terms of Service</a></li>
```

These links will now work because you've created the `privacy.html` and `terms.html` files.

#### Step 4: Test Your Links

1. **Save all files** (index.html, privacy.html, terms.html)
2. **Open index.html** in your browser
3. **Scroll to the footer**
4. **Click on "Privacy Policy"** - should open privacy.html
5. **Click on "Terms of Service"** - should open terms.html
6. **Click "Back to Home"** on either page - should return to index.html

### Customizing Your Privacy and Terms Pages

#### Update Company Name

In both `privacy.html` and `terms.html`, find and replace:

**Find:**
```html
AI Automation Bureau
```

**Replace with:**
```html
Your Company Name
```

**Locations to update:**
- Page title: `<title>Privacy Policy - AI Automation Bureau</title>`
- Meta description: `<meta name="description" content="...">`
- Meta author: `<meta name="author" content="...">`
- Header logo link text
- Footer copyright: `&copy; 2025 AI Automation Bureau`
- Throughout the content

#### Update Contact Email

**In privacy.html, find (around line 47):**
```html
<strong>Email:</strong> <a href="mailto:privacy@yourcompany.com" class="text-blue-600 hover:underline">privacy@yourcompany.com</a>
```

**Replace with your email:**
```html
<strong>Email:</strong> <a href="mailto:your-email@yourcompany.com" class="text-blue-600 hover:underline">your-email@yourcompany.com</a>
```

**In terms.html, find (around line 77):**
```html
<strong>Email:</strong> <a href="mailto:legal@yourcompany.com" class="text-blue-600 hover:underline">legal@yourcompany.com</a>
```

**Replace with your email:**
```html
<strong>Email:</strong> <a href="mailto:your-email@yourcompany.com" class="text-blue-600 hover:underline">your-email@yourcompany.com</a>
```

#### Update Last Updated Date

**In both files, find:**
```html
<strong>Last Updated:</strong> January 2025
```

**Replace with current date:**
```html
<strong>Last Updated:</strong> December 2024
```

#### Add Your Actual Policy Content

The templates provided are generic. You should:

1. **Review the content** to ensure it matches your actual practices
2. **Replace placeholder text** with your real policies
3. **Consult with a lawyer** if you handle sensitive data
4. **Update specific details** about your data practices

### File Structure After Setup

After completing these steps, your folder should look like this:

```
your-website-folder/
├── index.html          (your main landing page)
├── privacy.html        (privacy policy - newly created)
├── terms.html          (terms of service - newly created)
└── (other assets if any)
```

---

## Common Issues & Troubleshooting

### Issue 1: Links Don't Work

**Problem:** You click a link but nothing happens or you get a 404 error.

**Solution:**
1. **Check the file path** - Make sure `privacy.html` and `terms.html` are in the same folder as `index.html`
2. **Verify the filename** - File names are case-sensitive on some servers. Use lowercase: `privacy.html` not `Privacy.html`
3. **Check for typos** - In the `href` attribute, make sure you spelled the filename correctly
4. **Test in browser** - Type the URL directly in the address bar: `http://localhost/privacy.html`

**Example:**
```html
<!-- Wrong: -->
<a href="Privacy.html">Privacy Policy</a>  <!-- Capital P -->

<!-- Correct: -->
<a href="privacy.html">Privacy Policy</a>  <!-- Lowercase -->
```

### Issue 2: Page Styling Looks Broken

**Problem:** Your custom pages (privacy.html, terms.html) don't have the same styling as index.html.

**Solution:**
1. **Check the `<head>` section** - Make sure you copied all the `<link>` and `<style>` tags
2. **Verify Tailwind CSS is loaded** - Look for this line: `<script src="https://cdn.tailwindcss.com"></script>`
3. **Check Font Awesome** - Look for this line: `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">`

### Issue 3: Mobile Menu Not Working

**Problem:** On mobile, the menu button doesn't open/close the menu.

**Solution:**
1. **Check the JavaScript** - Make sure the `<script>` section at the bottom is included
2. **Verify class names** - The script looks for elements with specific class names - don't change them
3. **Check for errors** - Open browser console (F12) and look for JavaScript errors

### Issue 4: Text Changes Don't Appear

**Problem:** You edited text but the changes don't show on your page.

**Solution:**
1. **Save the file** - Use Ctrl+S (Windows) or Cmd+S (Mac)
2. **Hard refresh browser** - Press Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac) to clear cache
3. **Check for typos** - Make sure you edited the correct section
4. **Verify file location** - Make sure you're editing the right file

### Issue 5: Colors Look Different Than Expected

**Problem:** Your color changes don't match what you expected.

**Solution:**
1. **Check Tailwind color names** - Tailwind uses specific color names: `blue-600`, `yellow-300`, etc.
2. **Verify the shade number** - Numbers go from 50-900 (50 is lightest, 900 is darkest)
3. **Test in browser** - Different browsers may display colors slightly differently
4. **Check for conflicting classes** - Multiple color classes might override each other

**Example of Tailwind colors:**
```
Red: red-50, red-100, ..., red-900
Blue: blue-50, blue-100, ..., blue-900
Yellow: yellow-50, yellow-100, ..., yellow-900
```

### Issue 6: Responsive Design Broken

**Problem:** Your page doesn't look right on mobile or tablet.

**Solution:**
1. **Don't remove responsive classes** - Classes like `md:` and `lg:` are important
2. **Test on actual devices** - Use browser developer tools (F12) to test different screen sizes
3. **Check viewport meta tag** - This line should be in your `<head>`: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
4. **Verify grid columns** - Make sure you haven't changed grid layout classes

### Issue 7: Button Not Clickable

**Problem:** A button looks right but doesn't work when clicked.

**Solution:**
1. **Check if it's a `<button>` or `<a>`** - Buttons need JavaScript to work, links need an `href`
2. **Verify the href attribute** - Make sure the `href` has a valid URL
3. **Check for JavaScript errors** - Open console (F12) and look for errors
4. **Test the URL directly** - Copy the URL from `href` and try it in the address bar

**Example:**
```html
<!-- This is a link - needs href -->
<a href="https://example.com">Click Me</a>

<!-- This is a button - needs JavaScript -->
<button onclick="doSomething()">Click Me</button>
```

### Issue 8: Fonts Not Loading

**Problem:** Text doesn't look like it should - fonts appear generic.

**Solution:**
1. **Check font import** - Look for this line in `<style>`: `@import url('https://fonts.googleapis.com/css2?family=...')`
2. **Verify internet connection** - Fonts are loaded from the internet
3. **Check browser console** - Look for failed font downloads (F12)
4. **Wait for page to load** - Sometimes fonts take a moment to load

### Issue 9: Images Not Showing

**Problem:** You see a broken image icon instead of an image.

**Solution:**
1. **Check the image path** - Make sure the file exists and the path is correct
2. **Verify file extension** - Use lowercase extensions: `.jpg`, `.png`, not `.JPG`
3. **Check for spaces in filenames** - Use hyphens or underscores instead: `my-image.jpg` not `my image.jpg`
4. **Test with full URL** - Try using a complete URL instead of a relative path

---

## Best Practices

### 1. Always Backup Before Making Changes

**Why:** If something goes wrong, you can restore the original.

**How:**
1. Before making edits, save a copy of your file
2. Name it something like `index-backup.html`
3. Keep this backup safe
4. If you break something, you can copy from the backup

### 2. Make One Change at a Time

**Why:** If something breaks, you'll know exactly what caused it.

**Process:**
1. Make one small change
2. Save the file
3. Test in browser
4. If it works, move to the next change
5. If it breaks, undo that change

### 3. Use a Text Editor with Syntax Highlighting

**Recommended editors:**
- **Visual Studio Code** (Free, powerful) - https://code.visualstudio.com
- **Sublime Text** (Free trial) - https://www.sublimetext.com
- **Atom** (Free) - https://atom.io
- **Notepad++** (Free, Windows only) - https://notepad-plus-plus.org

**Why:** These show you:
- Color-coded HTML tags
- Matching parentheses and brackets
- Line numbers for easier navigation
- Errors before you save

### 4. Test on Multiple Devices

**Always test your changes on:**
- Desktop/Laptop
- Tablet
- Mobile phone
- Different browsers (Chrome, Firefox, Safari, Edge)

**Use browser dev tools:**
1. Press F12 to open developer tools
2. Click the mobile icon (top left)
3. Test different screen sizes

### 5. Keep Your Links Updated

**Maintain a link checklist:**
1. Every month, click all your links
2. Make sure they still work
3. Update any that are broken
4. Remove dead links

### 6. Version Control (Advanced)

**For serious projects, use Git:**
1. Track all changes to your files
2. Revert to previous versions if needed
3. Collaborate with others safely

**Popular platforms:**
- GitHub (Free) - https://github.com
- GitLab (Free) - https://gitlab.com
- Bitbucket (Free) - https://bitbucket.org

### 7. Security Best Practices

**Protect your site:**
1. **Use HTTPS** - Your site should have a lock icon in the browser
2. **Keep backups** - Store copies in multiple locations
3. **Update regularly** - Keep your code and dependencies current
4. **Validate forms** - Check user input before processing
5. **Use strong passwords** - Protect your hosting account

### 8. Performance Tips

**Make your site faster:**
1. **Compress images** - Use tools like TinyPNG.com
2. **Minimize CSS/JavaScript** - Remove unnecessary code
3. **Use a CDN** - Distribute content globally
4. **Cache aggressively** - Store files locally in browsers
5. **Monitor speed** - Use Google PageSpeed Insights

### 9. SEO Best Practices

**Help people find your site:**
1. **Update meta descriptions** - Describe each page in 160 characters
2. **Use proper headings** - H1 for main title, H2 for sections, etc.
3. **Add alt text to images** - Describe what images show
4. **Use descriptive links** - "Click here" is bad, "Learn about our features" is good
5. **Create a sitemap** - List all your pages

### 10. Accessibility Best Practices

**Make your site usable for everyone:**
1. **Use proper heading hierarchy** - Don't skip from H1 to H3
2. **Add alt text** - Describe all images for screen readers
3. **Use good color contrast** - Make text readable
4. **Label form fields** - Help users understand what to enter
5. **Test with screen readers** - Use tools like NVDA (free)

### 11. Documentation

**Keep notes about your site:**
1. **Document all changes** - What you changed and why
2. **Keep a changelog** - Track version history
3. **Document custom code** - Explain any JavaScript you added
4. **Store important info** - Hosting details, passwords (securely), contacts

### 12. Regular Maintenance Checklist

**Monthly:**
- [ ] Test all links
- [ ] Check mobile responsiveness
- [ ] Review analytics
- [ ] Update content if needed

**Quarterly:**
- [ ] Backup entire site
- [ ] Update dependencies (Tailwind, Font Awesome, etc.)
- [ ] Review security
- [ ] Check for broken images

**Annually:**
- [ ] Full content audit
- [ ] Update copyright year
- [ ] Review and update privacy/terms
- [ ] Plan updates and improvements

---

## Quick Reference Guide

### File Locations for Common Updates

| What to Update | File | Approximate Line |
|---|---|---|
| Logo text | index.html | 37 |
| Navigation menu | index.html | 42-48 |
| Hero headline | index.html | 77 |
| Hero description | index.html | 82 |
| Feature titles | index.html | 130, 152, 174 |
| Benefit titles | index.html | 218, 230, 242, 254, 266, 278 |
| Testimonial quotes | index.html | 373, 393, 413, 433 |
| About text | index.html | 455, 469 |
| Footer text | index.html | 532-587 |

### Common Tailwind Classes Quick Reference

```html
<!-- Spacing -->
<div class="p-4">          <!-- Padding: 4 units (16px) -->
<div class="px-8">         <!-- Horizontal padding: 8 units -->
<div class="mb-4">         <!-- Margin bottom: 4 units -->
<div class="gap-8">        <!-- Gap between items: 8 units -->

<!-- Colors -->
<div class="bg-black">     <!-- Black background -->
<div class="text-white">   <!-- White text -->
<div class="bg-yellow-300"><!-- Yellow background -->
<div class="text-gray-700"><!-- Dark gray text -->

<!-- Text -->
<div class="text-lg">      <!-- Large text -->
<div class="font-bold">    <!-- Bold text -->
<div class="text-center">  <!-- Centered text -->

<!-- Layout -->
<div class="flex">         <!-- Flexible layout -->
<div class="grid">         <!-- Grid layout -->
<div class="hidden">       <!-- Hide element -->

<!-- Responsive -->
<div class="hidden md:flex"><!-- Hidden on mobile, visible on tablets+ -->
<div class="text-sm md:text-lg"><!-- Small on mobile, large on tablets+ -->
```

### HTML Tag Reference

```html
<!-- Text elements -->
<h1>Main heading</h1>
<h2>Section heading</h2>
<p>Paragraph of text</p>
<span>Inline text</span>

<!-- Links -->
<a href="url">Link text</a>

<!-- Lists -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>

<!-- Buttons -->
<button>Click me</button>

<!-- Sections -->
<section>Content here</section>
<div>Container</div>

<!-- Comments (not visible) -->
<!-- This is a comment -->
```

---

## Getting Help

### Resources

1. **Tailwind CSS Documentation** - https://tailwindcss.com/docs
2. **HTML Reference** - https://developer.mozilla.org/en-US/docs/Web/HTML
3. **CSS Reference** - https://developer.mozilla.org/en-US/docs/Web/CSS
4. **Font Awesome Icons** - https://fontawesome.com/icons
5. **Web Accessibility** - https://www.w3.org/WAI/

### Community Support

1. **Stack Overflow** - https://stackoverflow.com (Q&A for developers)
2. **Tailwind CSS Discord** - https://discord.gg/tailwindcss
3. **Reddit** - r/web_design, r/webdev
4. **CSS-Tricks** - https://css-tricks.com

### When Asking for Help

Provide:
1. **Exact error message** (if any)
2. **Screenshot** of the problem
3. **Code snippet** that's causing issues
4. **What you've already tried**
5. **Your browser and device**

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing your AI Automation Bureau landing page. Remember:

- **Start small** - Make one change at a time
- **Test frequently** - Check your work after each change
- **Backup regularly** - Always have a copy of working files
- **Keep learning** - Web technologies evolve constantly
- **Ask for help** - Don't hesitate to reach out to the community

Good luck with your landing page! 🚀