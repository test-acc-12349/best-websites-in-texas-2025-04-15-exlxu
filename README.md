# Texas Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "Texas Web":
```html
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web</a>
```

2. **Navigation Items**: Located in the `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Other navigation items -->
</div>
```

### Hero Section
The main headline and introduction are in the first `<section>` after `<main>`:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Texas
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">{hero_statement}</p>
```

Replace `{hero_statement}` with your actual hero text.

### Tailwind CSS Class Guide
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-6` (margin bottom)
- Responsive design: `md:text-5xl` (applies at medium screens and up)

To modify styles:
1. Find the element you want to change
2. Look at its existing classes
3. Add or replace classes maintaining the same format

Example:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4">Easy to Use</h3>

<!-- Modified for larger text and different color -->
<h3 class="text-2xl font-semibold mb-4 text-blue-700">Easy to Use</h3>
```

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an in-page section
2. Match the href value to the `id` of the target section
3. Example: `<a href="#new-section">` links to `<section id="new-section">`

### External Links
The template contains these external links:
```html
<!-- Header CTA button -->
<a href="https://sigmaseo.io" class="hidden md:inline-block px-6 py-3 bg-blue-600">Get Started</a>

<!-- Hero CTA button -->
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```

To update external links:
1. Locate the `<a>` tag
2. Replace the `href` value with your desired URL
3. Always include `https://` for external links

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section `id` attributes match their corresponding links
   - Ensure the `#` symbol is included in the href
   - Verify there are no spaces in IDs

2. **Responsive Design Problems**
   - Look for classes starting with `md:` or `lg:`
   - Don't remove these classes as they control mobile responsiveness
   - Test on different screen sizes using browser dev tools

3. **Styling Issues**
   - Keep the existing class structure
   - Add new classes at the end of the class list
   - Don't remove `transition`, `duration`, or `hover` classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before publishing changes

Remember to always make a backup of your files before making changes!