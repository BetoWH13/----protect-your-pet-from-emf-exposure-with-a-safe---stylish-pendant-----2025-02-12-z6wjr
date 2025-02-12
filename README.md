# Pet EMF Protection Landing Page - Maintenance Guide

This guide will help you maintain and customize the Pet EMF Protection landing page. It's written for beginners and provides step-by-step instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and logo. To update:

```html
<!-- Located at the top of the page -->
<div class="flex items-center space-x-2">
    <i class="fas fa-shield-alt text-2xl text-purple-500"></i>
    <span class="text-xl font-bold">PetEMF Shield</span> <!-- Change brand name here -->
</div>
```

### Hero Section
The main headline and subtitle can be updated here:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    🛡️ Protect Your Pet from EMF Exposure with a Safe & Stylish Pendant! 🐾
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Shield your beloved companion from electromagnetic radiation with our premium protective pendant.
</p>
```

#### Tailwind CSS Class Guide
- `text-4xl`: Base text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens
- `mb-8`: Bottom margin spacing
- `text-gray-300`: Text color

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-800 p-8 rounded-2xl hover:bg-gray-700/50 transition-all duration-300 transform hover:scale-105">
    <i class="fas fa-feather text-3xl text-purple-400 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Lightweight & Pet-Friendly</h3>
    <p class="text-gray-400">Designed for comfort, our pendant won't weigh your pet down or cause any discomfort.</p>
</div>
```

To modify a feature card:
1. Change the icon by updating the `fa-feather` class to any [Font Awesome icon](https://fontawesome.com/icons)
2. Update the heading text within the `<h3>` tags
3. Modify the description within the `<p>` tags

## Managing Links

### Current Links in the Page
1. Main CTA Button:
```html
<a href="https://youremfshield.com/pages/pet-emf-defense-pendant-dg-2-0#aff=BetoWH72" class="inline-flex items-center px-8 py-4 text-lg font-semibold text-white bg-purple-600 rounded-full hover:bg-purple-700">
    Protect Your Pet Now
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

2. Footer Links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Shipping Information</a></li>
</ul>
```

To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute to your desired URL
3. Update the text between the opening and closing tags if needed

## Adding Policy Pages

### Step 1: Create Policy Pages
Create two new HTML files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder "#" links with the correct file paths:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    <li><a href="shipping.html" class="hover:text-purple-400 transition-colors duration-300">Shipping Information</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Images or Icons**
   - Ensure Font Awesome is properly loaded in the head section
   - Check that the icon class names are correct
   - Example: `<i class="fas fa-shield-alt">` must use exact Font Awesome class names

2. **Responsive Design Issues**
   - Check the responsive classes (prefixed with `sm:`, `md:`, or `lg:`)
   - Test the page at different screen sizes
   - Example: `text-4xl md:text-5xl lg:text-6xl` ensures proper text scaling

3. **Link Issues**
   - Verify all `href` attributes point to valid URLs or file paths
   - Test all links after updating
   - Ensure relative paths are correct based on your file structure

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all file paths are correct
3. Ensure Tailwind CSS is properly loaded via CDN
4. Confirm all HTML tags are properly closed

Remember to always test your changes across different devices and browsers after making updates.