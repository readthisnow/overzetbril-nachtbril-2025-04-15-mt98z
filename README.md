# Landing Page Maintenance Guide

This guide will help you maintain and customize the Nachtbril landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header Section
```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <a href="/" class="text-2xl font-bold text-gray-800">Nachtbril</a>
```
To update the company name:
1. Locate the `<a>` tag with "Nachtbril"
2. Replace "Nachtbril" with your desired text
3. Keep the surrounding classes unchanged

#### Hero Section
```html
<div class="relative z-10 text-center text-white max-w-4xl mx-auto px-4">
    <h1 class="text-4xl md:text-6xl font-bold mb-6">Overzetbril Nachtbril</h1>
    <p class="text-xl md:text-2xl mb-8">Schrijf Alles In Het Nederlands Over Overzetbril Nachtbril</p>
```
To update hero content:
1. Replace the `<h1>` text with your main headline
2. Update the `<p>` text with your subheading
3. Keep the responsive classes (`text-4xl md:text-6xl`) to maintain mobile/desktop sizing

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:`: Applies styles on medium screens (768px) and up
- `lg:`: Applies styles on large screens (1024px) and up
Example:
```html
<h1 class="text-4xl md:text-6xl">
```
- Mobile screens: `text-4xl` (2.25rem)
- Tablets and up: `text-6xl` (4rem)

#### Common Utility Classes
- `container`: Centers content and sets max-width
- `mx-auto`: Centers element horizontally
- `px-4`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `space-x-4`: Adds horizontal spacing between children
- `rounded-lg`: Adds border radius
- `shadow-md`: Adds medium box shadow

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
    <a href="https://nachtbril.com/shop" class="bg-blue-600 text-white px-6 py-2 rounded-full">Koop Nu</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. For internal sections, use `#section-name`
3. For external links, use the full URL (https://...)
4. Update the link text between the opening and closing tags

### Shop Button Links
The shop buttons appear in multiple locations:
```html
<!-- Hero section -->
<a href="https://nachtbril.com/shop" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">

<!-- CTA section -->
<a href="https://nachtbril.com/shop" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-full">
```
Replace all instances of `https://nachtbril.com/shop` with your shop URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Current footer structure:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Beleid</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors">Terms & Conditions</a></li>
    </ul>
</div>
```

To add policy pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links in the footer:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors">Terms & Conditions</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match link hrefs
   - Section IDs should not contain spaces
   - Check for proper lowercase/uppercase matching

2. **Responsive Design Issues**
   - Keep both mobile (`text-base`) and desktop (`md:text-lg`) classes
   - Don't remove `container` class from main sections
   - Maintain the `hidden md:flex` pattern for mobile menu

3. **Image Loading Problems**
   - Verify image URLs are correct and accessible
   - Include proper `alt` text for accessibility
   - Keep the `object-cover` class on full-width images

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before deploying to production.