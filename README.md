# MUCHMAN Landing Page - Maintenance Guide

This guide will help you maintain and customize the MUCHMAN landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and replace "MUCHMAN" with your brand name:
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">MUCHMAN</a>
```

2. **Navigation Links**: Locate the navigation menu:
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors">Features</a>
    <!-- Other navigation items -->
</div>
```
To modify link text, simply change the text between `<a>` tags.

### Hero Section
The main banner section contains:

1. **Main Heading**: Update the headline here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Discover The Secret Weapon Women Can't Resist
</h1>
```

2. **Subheading**: Modify the subtitle text:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Spray once. Instant attraction to women.
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `hover:`: Prefix for hover effects

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Modify existing classes or add new ones
4. Test responsiveness on different screen sizes

## Managing Links

### Internal Navigation Links
Current internal links use anchor tags (#):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you're linking to
2. Ensure the href matches exactly (including case)
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The main CTA button links to:
```html
<a href="https://laptoplifepro.com/pheromones" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500...">
```

To update external links:
1. Replace the href value with your new URL
2. Ensure URLs include `https://` or `http://`
3. Test links after updating

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links in footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Refund Policy</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href values exactly
   - Ensure no spaces in IDs
   - Verify that the # symbol is included

2. **Styling Issues**
   - Check for typos in Tailwind class names
   - Verify class order (responsive classes should come after base classes)
   - Test on multiple screen sizes

3. **External Links Not Working**
   - Verify URL format (including https://)
   - Test links in different browsers
   - Check for typing errors

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers
- Keep a backup of the original code before making changes

Remember to always test your changes thoroughly before pushing to production!