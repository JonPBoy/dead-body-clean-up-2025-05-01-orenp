# CleanScene Landing Page Maintenance Guide

This guide will help you maintain and customize the CleanScene landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo**
```html
<a href="#" class="text-2xl font-bold text-red-500">CleanScene</a>
```
- Replace "CleanScene" with your company name
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- Change color using `text-red-500` (options: text-blue-500, text-green-500, etc.)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold mb-6">Dead Body Clean-Up</h1>
<p class="text-xl md:text-2xl lg:text-3xl text-gray-400 mb-12">Specializing in Blood Stain Removal</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Size classes explanation:
  - `text-4xl`: Default size on mobile
  - `md:text-5xl`: Size on medium screens
  - `lg:text-7xl`: Size on large screens

### Feature Cards
Located in the features section:
```html
<div class="bg-gray-800 p-8 rounded-xl hover:bg-gray-700">
    <h3 class="text-xl font-semibold mb-4 text-red-500">Fast Response</h3>
    <p class="text-gray-400">24/7 emergency response team ready to assist you immediately</p>
</div>
```
To modify:
1. Change heading text between `<h3>` tags
2. Update description between `<p>` tags
3. Adjust colors:
   - Background: `bg-gray-800`
   - Hover: `hover:bg-gray-700`
   - Text: `text-gray-400`

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="hover:text-red-500 transition-colors duration-300">Services</a>
    <a href="#features" class="hover:text-red-500 transition-colors duration-300">Features</a>
    <a href="#faq" class="hover:text-red-500 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-red-500 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute
2. For internal links (same page):
   - Use `#section-id` format
   - Ensure section IDs match exactly
3. For external links:
   - Replace with full URL (e.g., `href="https://example.com"`)

### Contact Email
Located in two places:
```html
<!-- Contact section -->
<a href="mailto:joe@cleanjoe.com">joe@cleanjoe.com</a>

<!-- Footer section -->
<p class="text-gray-400">joe@cleanjoe.com</p>
```
To update:
1. Replace `joe@cleanjoe.com` with your email address
2. Update both instances for consistency

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-red-500 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-red-500 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check for typos in `href` attributes
   - Verify section IDs match exactly (case-sensitive)
   - Ensure files exist in the correct directory

2. **Responsive Design Issues**
   - Check screen-size classes:
    - `md:` for medium screens (768px+)
    - `lg:` for large screens (1024px+)
   - Test on different devices or using browser dev tools

3. **Styling Problems**
   - Verify Tailwind CSS is properly loaded
   - Check for missing or incorrect class names
   - Ensure classes are space-separated

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before publishing updates to your live site.