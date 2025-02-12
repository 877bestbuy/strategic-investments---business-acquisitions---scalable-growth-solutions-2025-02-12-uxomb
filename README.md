# Alto Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alto landing page. Whether you're new to web development or need a quick reference, follow these steps to make updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-800">Alto</a>
```
- Replace "Alto" with your company name
- Keep the classes unchanged to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `class` attributes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 text-gray-900">
    AI-Driven Acquisitions & Strategic Investments for Growth
</h1>
```
- Update heading text while keeping the responsive sizing classes
- The classes ensure proper display on different screen sizes:
  - `text-4xl`: Base size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features and Benefits Sections
To update feature cards:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-chart-line text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Strategic Acquisitions</h3>
    <p class="text-gray-600 leading-relaxed">Your updated text here</p>
</div>
```
- Update icon: Change `fa-chart-line` to any [Font Awesome](https://fontawesome.com/icons) icon
- Modify heading and paragraph text
- Maintain the card structure and classes for consistent styling

## Managing Links

### Navigation Links
Current links in the header:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://alto.icu">Get Started</a>
```
To update:
1. Internal links (starting with #):
   - Match the `id` of the section you're linking to
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace `https://alto.icu` with your desired URL
   - Always include `https://` for external links

### Footer Links
Update social media and contact links:
```html
<a href="mailto:info@alto.icu">info@alto.icu</a>
<a href="#" class="hover:text-white transition-colors duration-300">
    <i class="fab fa-linkedin text-xl"></i>
</a>
```
- Replace email address in both the `href` and display text
- Update social media links from `#` to actual profile URLs

## Adding Privacy and Terms Pages

### 1. Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### 2. Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section `id` attributes match link `href` values
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Test changes using browser dev tools' responsive mode

3. **Icon Not Displaying**
   - Verify Font Awesome is properly loaded
   - Check icon class names against Font Awesome documentation
   - Ensure you're using the correct icon style prefix (fas, fab, far)

4. **Styling Problems**
   - Keep the original Tailwind classes unless you understand their purpose
   - Test any style changes across different screen sizes
   - Use browser inspector to identify which classes are affecting elements

Remember to:
- Always backup your files before making changes
- Test all links after updating
- View changes on multiple devices or screen sizes
- Validate your HTML using [W3C Validator](https://validator.w3.org/)

Need additional help? Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.