# ListingAI Landing Page Maintenance Guide

This guide will help you maintain and customize the ListingAI landing page. Whether you're new to HTML and CSS or just getting started with web development, we'll walk through common maintenance tasks step by step.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-white">ListingAI</a>
```
Simply replace "ListingAI" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
</div>
```
- To add new menu items, copy an existing `<a>` tag and modify the text and href
- The `hidden md:flex` class means the menu is hidden on mobile and visible on medium screens
- `space-x-8` adds horizontal spacing between items

### Hero Section
To update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-blue-600">
    Quickly Create Unlimited FB Marketplace Listings!
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Turn Pictures into FB Marketplace Listings w/AI
</p>
```
- The headline uses responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)
- The gradient effect is created by `bg-gradient-to-r from-blue-400 to-blue-600`

## Fixing Broken Links

### Current Link Inventory
1. Get Started Button (appears multiple times):
```html
<!-- Replace mm.mm.com with your actual URL -->
<a href="mm.mm.com" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full">
```

2. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
These are internal links to page sections. The `#` indicates they link to elements with matching IDs.

### Updating Links
1. For external links (like the "Get Started" button):
```html
<!-- Old -->
<a href="mm.mm.com">

<!-- New (example) -->
<a href="https://your-actual-domain.com/signup">
```

2. For internal section links, ensure the href matches the section ID:
```html
<!-- Link in navigation -->
<a href="#features">

<!-- Corresponding section -->
<section id="features" class="py-24 px-6 bg-gray-800">
```

## Linking Privacy and Terms Pages

### Footer Links Section
Locate this section in the footer:
```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to your policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working:**
- Check that href values exactly match file names or section IDs
- Section IDs are case-sensitive
- External links should include `https://` or `http://`

2. **Responsive Design Issues:**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `container` and `mx-auto` classes on parent elements
- Maintain the existing responsive class structure:
  ```html
  class="text-4xl md:text-5xl lg:text-6xl"
  ```

3. **Gradient Text Not Showing:**
- Ensure these classes remain together:
  ```html
  class="bg-clip-text text-transparent bg-gradient-to-r"
  ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always make a backup of your files before making changes, and test all modifications across different devices and browsers.