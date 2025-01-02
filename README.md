# Landing Page Maintenance Guide

This guide will help you maintain and customize your AI Website Builder landing page. Follow these instructions carefully to make updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. Change the brand name:
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent">
    BAI Builder  <!-- Replace this text -->
</div>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Replace text as needed -->
    <a href="#benefits">Benefits</a>  <!-- Replace text as needed -->
    <!-- etc. -->
</div>
```

### Hero Section
The main headline and subheading can be updated here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
    Best AI Website Builder  <!-- Replace this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    The ultimate AI website builder for non-coders  <!-- Replace this text -->
</p>
```

### Working with Tailwind Classes

Common class patterns used in this page:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-400`, `bg-blue-600`, etc.
- Spacing: `px-6`, `py-4`, `mb-6`, etc.
- Hover effects: `hover:scale-105`, `hover:text-blue-400`

To modify styles:
1. Find the element you want to change
2. Look up the class you want to modify on [Tailwind CSS documentation](https://tailwindcss.com/docs)
3. Replace or add classes maintaining the existing responsive classes (those with `md:` or `lg:` prefixes)

Example:
```html
<!-- Original -->
<div class="bg-gray-800 rounded-xl p-8">

<!-- Modified with different background and padding -->
<div class="bg-gray-900 rounded-xl p-6">
```

## Managing Links

### Navigation Links
Update the href attributes in the header navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Call-to-Action Buttons
Replace the placeholder URLs:
```html
<!-- Find all instances of -->
<a href="https://bai.com" class="...">
<!-- Replace with your actual URL -->
<a href="https://your-actual-domain.com" class="...">
```

### Social Media Links
Update social media links in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-blue-400">
        <i class="fab fa-twitter text-xl"></i>
    </a>
    <!-- Replace '#' with actual social media URLs -->
</div>
```

## Adding Privacy and Terms Pages

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update footer links:
```html
<!-- Find this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

3. Ensure your new pages maintain consistent styling by copying the header and footer from index.html

## Troubleshooting

Common Issues:
1. **Broken Links**: Ensure all href attributes start with either:
   - `#` for page sections
   - `./` for local pages
   - `https://` for external links

2. **Responsive Issues**: Check that you maintain responsive classes:
```html
<!-- Example of responsive classes -->
text-4xl md:text-5xl lg:text-6xl  <!-- Don't remove the md: and lg: prefixes -->
```

3. **Icon Problems**: If icons aren't showing:
```html
<!-- Verify this line is in your head section -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```

For additional help:
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all files are in the correct directory
- Test all links after making changes
- Use browser developer tools (F12) to inspect elements

Remember to always backup your files before making significant changes!