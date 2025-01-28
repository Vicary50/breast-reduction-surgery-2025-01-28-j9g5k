# Landing Page Maintenance Guide
A comprehensive guide for maintaining and customizing the Karri Clinic landing page.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm shadow-sm z-50">
    <nav class="container mx-auto px-6 py-4">
        <a href="/" class="text-2xl font-bold text-blue-600">Karri Clinic</a>
```
To modify:
1. Change clinic name: Replace "Karri Clinic" with your clinic name
2. Adjust header color: Change `text-blue-600` to other colors (e.g., `text-red-600`)
3. Modify background opacity: Change `bg-white/95` to adjust transparency

### Hero Section
```html
<section class="pt-32 pb-24 bg-gradient-to-b from-blue-50 to-white">
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 text-gray-900">
        Breast Reduction Surgery
    </h1>
```
To customize:
1. Update heading: Replace text between `<h1>` tags
2. Modify gradient: Change `from-blue-50` to other colors
3. Adjust text size:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Benefits Cards
Each benefit card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Benefit Title</h3>
    <p class="text-gray-600">Benefit description text.</p>
</div>
```
To modify:
1. Change title: Update text in `<h3>` tags
2. Update description: Modify text in `<p>` tags
3. Adjust spacing: Modify `p-8` padding value
4. Change hover effect: Modify `hover:shadow-xl`

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#benefits">Benefits</a>
    <a href="#features">Features</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Internal links (same page):
   - Keep `#` followed by section ID
   - Example: `href="#benefits"`
2. External links:
   - Replace with full URL
   - Example: `href="https://yourwebsite.com/page"`

### Consultation Button
```html
<a href="https://thekarriclinic.co.uk/" class="inline-block px-8 py-4 bg-blue-600">
```
To update:
1. Replace URL with your booking system link
2. Ensure URL includes `https://`
3. Test link functionality after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To add proper links:
1. Create privacy.html and terms.html files
2. Update href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. Broken Navigation
- Verify section IDs match href attributes
- Example: `href="#benefits"` needs matching `id="benefits"` in section

2. Responsive Design Issues
- Check media query classes:
  - Mobile (default): No prefix
  - Tablet: `md:` prefix
  - Desktop: `lg:` prefix

3. Color Inconsistencies
- Main blue color classes used:
  - `text-blue-600`
  - `bg-blue-600`
  - `from-blue-50`
- Ensure consistent color usage throughout

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify all links start with `https://` for external URLs
- Test responsiveness using browser developer tools
- Maintain consistent spacing with provided padding/margin classes

Remember to always test changes across different devices and browsers before publishing updates.