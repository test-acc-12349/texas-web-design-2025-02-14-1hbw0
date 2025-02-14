# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo Text**
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep the `href` attributes matching section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```
- Update heading and subheading text
- Maintain responsive text sizes (md: for tablet, lg: for desktop)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-server text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package...</p>
</div>
```
To modify:
1. Change icon: Update `fa-server` to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Modify text in `<h3>` tag
3. Update description: Change text in `<p>` tag

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">Get Started</a>
```

To update links:
1. Internal links (starting with #):
   - Ensure the href matches the section ID
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace "https://twd.com" with your actual website URL
   - Always include "https://" or "http://"

## Linking Privacy and Terms Pages

### Footer Legal Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These ensure proper display on different screen sizes
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Icons Not Displaying**
- Verify Font Awesome CDN link in header is present
- Check icon class names match exactly
- Example: `class="fas fa-server"`

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Check Tailwind CSS documentation for class references
- Ensure all files are in the correct directory
- Test all links after making changes

Remember to always backup your files before making changes, and test the page across different devices and browsers after updates.