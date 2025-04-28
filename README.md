# 101Headshots Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
- [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
- [Fixing Broken Links](#fixing-broken-links)
- [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Located at the top of the page -->
<span class="font-bold text-xl">101Headshots</span>
```
To update the company name, modify the text between the `<span>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Kansas City, Missouri Corporate Headshot Photography Services
</h1>
<p class="max-w-2xl mx-auto text-xl md:text-2xl text-gray-600 mb-12">
    High-impact headshots communicating your professionalism clearly.
</p>
```
To update the main headline and subheading:
1. Locate the `<h1>` tag for the main headline
2. Locate the `<p>` tag for the subheading
3. Replace the text while keeping the tags intact

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Impact Shots</h3>
    <p class="text-gray-600">Professional headshots that make a lasting impression...</p>
</div>
```
To update feature cards:
1. Find the `<div>` with the `bg-white` class
2. Modify the `<h3>` text for the feature title
3. Update the `<p>` text for the feature description

### Tailwind CSS Classes

#### Understanding Responsive Classes
The site uses Tailwind's responsive prefixes:
- `md:` applies styles on medium screens (768px and up)
- `lg:` applies styles on large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Default size: text-4xl (36px)
- Medium screens: text-5xl (48px)
- Large screens: text-6xl (60px)

#### Common Class Modifications

1. Spacing Classes:
   - `p-` for padding (p-4 = 1rem)
   - `m-` for margin (m-4 = 1rem)
   - `space-x-` for horizontal spacing between elements
   - `space-y-` for vertical spacing between elements

2. Color Classes:
   - `text-{color}-{shade}` for text color
   - `bg-{color}-{shade}` for background color
   - Example: `text-gray-600`, `bg-blue-600`

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://www.101headshots.com">Book Now</a>
</div>
```

To update links:
1. Locate the `<a>` tag you want to modify
2. Update the `href` attribute:
   - For internal sections: Use `#section-id`
   - For external links: Use complete URL (https://...)

### Footer Links
Current footer link structure:
```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```

To update footer links:
1. Find the appropriate `<ul>` section
2. Locate the `<a>` tag within the `<li>`
3. Update the `href` attribute

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Current footer legal section:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Replace the `#` in the href with the correct path:
```html
<li><a href="/privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. Broken Internal Links
- Check that section IDs match the href attributes
- Ensure no spaces in IDs
- Verify that the section exists in the HTML

2. Responsive Design Issues
- Check that you're maintaining the responsive classes (md:, lg:)
- Test the page at different screen sizes
- Verify Tailwind CSS is properly loaded in the head section

3. Styling Inconsistencies
- Maintain the existing class structure
- Keep hover states (hover:) when modifying links
- Preserve transition classes for animations

### Need Help?
If you encounter issues:
1. Verify the Tailwind CSS CDN is accessible
2. Check for typos in class names
3. Ensure all HTML tags are properly closed
4. Test the page in multiple browsers

Remember to always back up your files before making changes, and test thoroughly after each modification.