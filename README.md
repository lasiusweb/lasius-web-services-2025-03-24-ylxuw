# Lasius Web Services Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Lasius Web Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu.

```html
<!-- Original header text -->
<a href="/" class="text-2xl font-bold tracking-tight hover:text-gray-300 transition-colors">
    Lasius Web
</a>
```

To update the company name:
1. Locate this code in the header section
2. Replace "Lasius Web" with your desired text
3. Maintain the existing classes to preserve styling

### Hero Section
The hero section contains the main headline and subheading.

```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-8 bg-clip-text text-transparent bg-gradient-to-r from-purple-400 to-blue-400">
    Transform your online presence.<br>Dominate your market.
</h1>
```

To modify the hero text:
1. Find the `<h1>` tag within the hero section
2. Update the text between the tags
3. Keep the `<br>` tag for line breaks
4. Preserve the Tailwind classes for proper styling

#### Understanding Key Tailwind Classes:
- `text-4xl`: Large text on mobile
- `md:text-6xl`: Larger text on medium screens
- `bg-gradient-to-r`: Creates right-flowing gradient
- `from-purple-400 to-blue-400`: Gradient colors

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-gray-300 transition-colors">Features</a>
    <a href="#benefits" class="hover:text-gray-300 transition-colors">Benefits</a>
    <a href="#faq" class="hover:text-gray-300 transition-colors">FAQ</a>
    <a href="#contact" class="hover:text-gray-300 transition-colors">Contact</a>
</div>
```

To update navigation links:
1. Locate the `href` attribute in each `<a>` tag
2. Replace the "#section-name" with:
   - Internal links: Use "#new-section-id"
   - External links: Use complete URL (e.g., "https://example.com")

### Call-to-Action Links
Current CTA links that need attention:

```html
<a href="https://lasiuswebservices.com" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 rounded-full">
    Get Started Now
</a>
```

To update CTA links:
1. Find all instances of "https://lasiuswebservices.com"
2. Replace with your actual service URL
3. Test all CTA buttons to ensure proper linking

## Linking Privacy and Terms Pages

### Footer Legal Links
Current footer legal section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:

```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - Verify that all referenced sections exist

2. **Responsive Design Issues**
   - Keep all responsive Tailwind classes (starting with `md:`, `lg:`, etc.)
   - Test on multiple screen sizes
   - Don't remove the viewport meta tag

3. **Gradient Text Not Showing**
   - Ensure these classes remain together:
     ```html
     bg-clip-text text-transparent bg-gradient-to-r
     ```

4. **Navigation Menu Hidden on Mobile**
   - The `hidden md:flex` class combination controls mobile visibility
   - Don't remove unless implementing mobile menu alternative

### Best Practices
- Always backup before making changes
- Test all links after updates
- Maintain consistent styling across new pages
- Keep the responsive design intact
- Test on multiple browsers and devices

For additional support or questions, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.