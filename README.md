# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Albert Park  <!-- Replace this text -->
</div>

<!-- Navigation Items -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update navigation text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

**Styling Tip:** The `hidden md:flex` class means the menu is hidden on mobile and appears on medium screens and larger.

### Hero Section
Update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Your financial success is our bottom line  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting services tailored to drive your business forward  <!-- Subheading -->
</p>
```

**Responsive Text Classes Explained:**
- `text-4xl`: Base size for mobile
- `md:text-5xl`: Larger size for medium screens
- `lg:text-6xl`: Largest size for large screens

### Feature Cards
Each feature card follows this structure:

```html
<div class="bg-gray-800 rounded-2xl p-8 hover:scale-105 transition-transform duration-300 shadow-lg">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-xl mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Tax Optimization</h3>  <!-- Feature title -->
    <p class="text-gray-400">Strategic tax planning and optimization...</p>  <!-- Feature description -->
</div>
```

## Managing Links

### Navigation Menu Links
The navigation uses anchor links to scroll to page sections:

```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
```

To update:
1. Find the section ID in the HTML (`id="features"`)
2. Match the href attribute (`href="#features"`)
3. Ensure the ID exists in the target section

### Call-to-Action Links
Update the main CTA buttons:

```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full">
    Transform Your Finances  <!-- Button text -->
</a>
```

**Important:** Replace `https://theaccountants.com` with your actual URL.

### Footer Links
The footer contains multiple link sections:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Tax Optimization</a></li>
</ul>
```

Replace `href="#"` with actual page URLs.

## Adding Privacy and Terms Pages

### Step 1: Locate Footer Links
Find the Legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update Link Paths
Replace the placeholder `#` with paths to your policy pages:

```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Maintain the responsive class patterns:
     ```html
     class="text-base md:text-lg lg:text-xl"
     ```
   - Don't remove `md:` or `lg:` prefixes

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     class="bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent"
     ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different screen sizes and browsers before deploying to production.