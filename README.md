# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Best Air Purifier landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <div class="flex items-center">
            <!-- Update company name here -->
            <a href="/" class="text-2xl font-bold text-gray-800">Best Air Purifier</a>
        </div>
```

To modify:
1. Locate the text between `<a>` tags
2. Replace "Best Air Purifier" with your desired company name
3. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main banner section contains your primary headline:

```html
<div class="max-w-4xl mx-auto text-center text-white">
    <!-- Update main headline here -->
    <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">Best Air Purifier</h1>
    <!-- Update subheading here -->
    <p class="text-xl md:text-2xl mb-8">Find Best Air Purifier</p>
```

To modify:
1. Update the `<h1>` text for your main headline
2. Modify the `<p>` text for your subheading
3. Adjust responsive text sizes:
   - Before `md:` is mobile size
   - After `md:` is desktop size

### Features Section
Each feature card can be customized:

```html
<div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="text-blue-600 mb-4">
        <!-- Change icon here -->
        <i class="fas fa-fan text-4xl"></i>
    </div>
    <!-- Update feature title -->
    <h3 class="text-xl font-bold mb-4">Dyson Air Purifier</h3>
    <!-- Update feature description -->
    <p class="text-gray-600">Advanced air filtration technology...</p>
</div>
```

To modify:
1. Change icons by updating the `fa-` class (reference [Font Awesome](https://fontawesome.com/icons))
2. Update feature titles in the `<h3>` tags
3. Modify descriptions in the `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <!-- Update purchase link here -->
    <a href="https://stripe.com/buy" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700">Buy Now</a>
</div>
```

To update links:
1. Locate the `href` attribute in any `<a>` tag
2. Replace with your desired URL:
   - Internal links start with `#` (e.g., `#features`)
   - External links need full URLs (e.g., `https://example.com`)
3. Update button text between `<a>` tags as needed

### Purchase Links
The "Buy Now" buttons appear throughout the page:

```html
<a href="https://stripe.com/buy" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">Shop Now</a>
```

To update all purchase links:
1. Search for `https://stripe.com/buy`
2. Replace with your actual checkout or product page URL
3. Test all buttons to ensure they direct to the correct destination

## Adding Policy Pages

### Footer Policy Links
The footer contains placeholder policy links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Policies</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Shipping Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Return Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create your policy HTML files (e.g., `privacy.html`, `terms.html`)
2. Update the `href` attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the correct directory
   - Test all links after updating

2. **Responsive Design Issues**
   - Keep both mobile (`text-xl`) and desktop (`md:text-2xl`) classes when updating text sizes
   - Don't remove `md:` prefixes as they control desktop styling
   - Test on both mobile and desktop views after changes

3. **Icon Problems**
   - Verify Font Awesome is properly loaded
   - Check icon names on Font Awesome website
   - Ensure proper icon prefix (`fas`, `fab`, etc.)

Remember to:
- Always backup before making changes
- Test on multiple devices and browsers
- Keep consistent styling across similar elements
- Maintain the responsive design by preserving Tailwind's responsive classes

Need help? Contact your web developer or reference the [Tailwind CSS documentation](https://tailwindcss.com/docs).