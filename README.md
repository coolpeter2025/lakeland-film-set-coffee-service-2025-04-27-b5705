# Delightful Bean Landing Page - Maintenance Guide

This guide will help you maintain and customize the Delightful Bean landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

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
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Delightful Bean  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-6">
    Lakeland Film Set Coffee Service  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Keeping Lakeland production crews fueled and focused  <!-- Update subheading -->
</p>
```

### Tailwind CSS Tips for Beginners
- `text-4xl`: Controls text size (4xl is larger than 3xl)
- `md:text-6xl`: Applies different text size on medium screens
- `mb-6`: Adds margin bottom (spacing)
- `text-gray-300`: Sets text color
- `font-bold`: Makes text bold

## Managing Links

### Current Link Locations

1. **Navigation Menu Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Links:**
```html
<a href="https://www.delightfulbean.com/" class="inline-flex items-center...">
    Get Started  <!-- Replace URL with your booking page -->
</a>
```

3. **Contact Email:**
```html
<a href="mailto:info@delightfulbean.com">
    info@delightfulbean.com  <!-- Update with your email -->
</a>
```

### Updating Links Step-by-Step

1. Internal Links (Same Page):
   - Keep the `#` symbol
   - Match the ID of the section you're linking to
   ```html
   <a href="#services">Services</a>
   <section id="services">  <!-- These must match -->
   ```

2. External Links:
   - Replace placeholder URLs
   - Include full URL with https://
   ```html
   <a href="https://your-actual-website.com">Book Now</a>
   ```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h4 class="font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <li><a href="#services" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Services</a></li>
        <!-- Add these new links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Privacy and Terms Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling:
   ```html
   <main class="container mx-auto px-6 py-24">
       <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
       <!-- Add your policy content here -->
   </main>
   ```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working:**
   - Check that IDs match exactly (case-sensitive)
   - Ensure external URLs include `https://`
   - Verify file names match exactly

2. **Styling Problems:**
   - Check for missing class names
   - Verify Tailwind CSS is loading (check network tab)
   - Maintain responsive classes (md:, lg: prefixes)

3. **Layout Issues:**
   - Keep container classes intact
   - Maintain the grid structure in sections
   - Don't remove responsive utility classes

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12)
2. Verify all files are in the correct location
3. Ensure all HTML tags are properly closed
4. Maintain the existing class structure when making changes

Remember to test all changes across different screen sizes using your browser's developer tools.