# RevenuePath Landing Page Maintenance Guide

This guide will help you maintain and customize the RevenuePath landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="#" class="text-xl font-bold text-white">RevenuePath</a>
```
Simply replace "RevenuePath" with your desired company name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    We Build Hands-Off Sales Systems for B2B Leaders
</h1>
```
- Replace the heading text while maintaining the existing classes
- The classes control responsive text sizing (`text-4xl md:text-5xl lg:text-6xl`)

### Modifying Tailwind Classes

**Common Class Patterns:**
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-300`, `bg-blue-600`, etc.
- Spacing: `px-6` (padding), `my-8` (margin), etc.

**Example: Changing Button Colors**
```html
<!-- Original -->
<button class="bg-blue-600 hover:bg-blue-700 text-white">

<!-- Modified for green -->
<button class="bg-green-600 hover:bg-green-700 text-white">
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an internal section link
2. Ensure the href matches the `id` of the target section
3. For external links, replace with full URL:
```html
<a href="https://example.com/features">Features</a>
```

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Blog</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Contact</a></li>
</ul>
```

To update:
1. Replace `#` with your actual page URLs
2. For internal pages: `href="about.html"`
3. For external links: `href="https://blog.example.com"`

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
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

Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section `id` attributes match the href values
   - Example: `href="#features"` should match `<section id="features">`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes

3. **Button Styling**
   - Keep the `transition-all` and `duration-300` classes for smooth animations
   - Maintain the `hover:` classes for interactive effects

4. **Text Not Visible**
   - Ensure text colors contrast with background colors
   - The page uses dark mode styling; maintain light text on dark backgrounds

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test all links after making changes
- View the page on different devices to ensure responsive design

Remember to always back up your files before making changes, and test the page thoroughly after any modifications.