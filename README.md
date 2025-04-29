# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your web agency landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">WebAgency</a>
```
Simply replace "WebAgency" with your company name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```
Keep the classes intact to maintain styling and responsive behavior.

### Hero Section
The main headline and subheading are located in:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Best Web Agency In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks
</p>
```

**Important Tailwind Classes Explained:**
- `text-4xl md:text-5xl lg:text-6xl`: Responsive text sizing
- `bg-gradient-to-r`: Creates right-flowing gradient
- `mb-8`: Adds margin bottom spacing

### Features & Benefits Sections
To modify feature cards:
```html
<div class="bg-gray-900 rounded-2xl p-8 hover:shadow-2xl transition duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-400">Your feature description here</p>
</div>
```

## Managing Links

### Navigation Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Add a matching ID to that section: `<section id="your-section-name">`
3. Update the href to match: `<a href="#your-section-name">`

### Call-to-Action Links
The main CTA buttons currently point to "https://fixrr.online":
```html
<a href="https://fixrr.online" class="inline-flex items-center px-8 py-3 rounded-full bg-gradient-to-r from-blue-600 to-teal-500">
    Get Started Now
</a>
```

To update:
1. Replace `https://fixrr.online` with your desired URL
2. Test the link after updating

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add new links:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <div>
        <h4 class="text-lg font-semibold mb-4">Legal</h4>
        <ul class="space-y-2">
            <!-- Add these new items -->
            <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Step 2: Create Policy Pages
1. Create new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradient Text:**
If gradient text disappears, ensure these classes are present:
```html
bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent
```

2. **Responsive Issues:**
- Check that `md:` and `lg:` prefixes are preserved
- Don't remove the `hidden md:flex` class from the navigation menu
- Maintain the responsive grid classes in sections

3. **Animation Problems:**
If animations stop working, verify:
```html
data-aos="fade-up"
```
is present and the AOS script is loaded at the bottom of the page.

### Need Help?
- Double-check class names against Tailwind documentation
- Use browser inspector to identify styling issues
- Keep original class structure when making changes
- Test all links after updating

Remember to always make a backup before making significant changes to your code.