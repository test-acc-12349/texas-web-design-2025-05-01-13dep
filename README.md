# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions to make updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- Modify color using `text-blue-600` (options: text-[color]-[shade])

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `hidden md:flex` class for mobile responsiveness
- Keep `space-x-8` for consistent spacing

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- Update heading and subheading text
- Maintain responsive text sizes (text-4xl, md:text-5xl, lg:text-6xl)
- Keep margin classes (mb-6, mb-12) for spacing

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
- Update heading and description text
- Maintain the shadow classes for hover effects
- Keep padding (p-8) and margin (mb-4) classes

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure corresponding section IDs exist
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://example.com/features"`

### Call-to-Action Buttons
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white">Start Your Project</a>
```
- Update `href` with your actual URL
- Maintain button styling classes
- Test links before deploying

### Footer Links
Located in the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Web Design</a></li>
    <!-- Additional links -->
</ul>
```
- Replace `#` with actual URLs
- Keep hover effects and spacing classes
- Update link text as needed

## Adding Privacy and Terms Pages

### Footer Legal Section
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Verify file paths are correct
   - Test all links after updating

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Maintain the mobile menu button for small screens
   - Test on multiple device sizes

3. **Styling Problems**
   - Keep the Tailwind CDN link in the header
   - Maintain existing class structure
   - Use browser inspector to debug style issues

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all changes in a development environment first
- Keep a backup of the original file before making changes

Remember to test all changes thoroughly before deploying to a live environment. If you're unsure about any modifications, consult with a web developer or create a backup first.