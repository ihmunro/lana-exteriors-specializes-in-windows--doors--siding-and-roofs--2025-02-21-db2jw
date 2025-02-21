# Lana Exteriors Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Lana Exteriors landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Company Name and Logo
```html
<!-- Located in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">Lana Exteriors</a>
```
To update the company name, simply replace "Lana Exteriors" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight text-gray-900 mb-8">
    Lana Exteriors specializes in windows, doors, siding and roofs.
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    An ideal customer is one that appreciates a job well done
</p>
```
Update these text sections to match your company's message while keeping the surrounding HTML tags intact.

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` - Applies styles on medium screens (768px and up)
- `lg:` - Applies styles on large screens (1024px and up)
- Example:
```html
<div class="text-xl md:text-2xl">
```
This makes text larger on medium screens and up.

#### Common Class Patterns
1. Spacing Classes:
   - `px-4`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-8`: Bottom margin
   - `mt-12`: Top margin

2. Color Classes:
   - `text-gray-900`: Dark text
   - `text-gray-600`: Medium gray text
   - `bg-white`: White background
   - `bg-blue-600`: Blue background

3. Layout Classes:
   - `container`: Centers content
   - `mx-auto`: Horizontal auto margins
   - `flex`: Flexible container
   - `grid`: Grid container

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```

To update these links:
1. For internal section links, keep the `#` prefix
2. For external links, use the full URL:
```html
<a href="https://example.com/page" class="text-gray-600 hover:text-gray-900">
```

### Email Links
Update all email links:
```html
<a href="mailto:john@lanaexteriors.ca">
```
Replace with your email address:
```html
<a href="mailto:your.email@domain.com">
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links to the footer's Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same styling as the main page:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Lana Exteriors</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="font-sans antialiased text-gray-900 bg-white">
    <!-- Copy header from index.html -->
    
    <!-- Add your policy content here -->
    
    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues

1. Broken Internal Links
- Ensure section IDs match the href attributes
- Example: `href="#services"` must match `id="services"`

2. Responsive Design Issues
- Check media query classes (md:, lg:)
- Test on different screen sizes
- Use browser developer tools to inspect elements

3. Missing Styles
- Verify Tailwind CSS is properly loaded
- Check for typos in class names
- Ensure classes are space-separated

### Need Help?
- Use browser developer tools (F12) to inspect elements
- Check the Tailwind CSS documentation for class references
- Verify all files are in the correct directory structure

Remember to test all changes across different devices and browsers before deploying to production.