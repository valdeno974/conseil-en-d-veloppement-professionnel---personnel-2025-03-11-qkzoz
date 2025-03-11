# Landing Page Maintenance Guide

This guide will help you maintain and customize the Valdeno Consulting landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
    <nav class="container mx-auto px-6 py-4">
        <!-- Change company name here -->
        <a href="/" class="text-2xl font-bold text-gray-800">
            Valdeno
        </a>
```

To modify:
1. Change "Valdeno" to your company name
2. Adjust text size by changing `text-2xl` to `text-3xl` for larger text
3. Modify colors by changing `text-gray-800` to other Tailwind colors (e.g., `text-blue-800`)

### Hero Section
The main headline and subtitle are in the hero section:

```html
<section class="pt-32 pb-24 bg-gradient-to-br from-purple-50 via-white to-blue-50">
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
        Conseil en développement professionnel & personnel
    </h1>
    <p class="text-xl md:text-2xl text-gray-600">
        Accompagnement personnalisé pour révéler votre potentiel
    </p>
```

To modify:
1. Update the h1 text for your main headline
2. Change the subtitle in the p tag
3. Adjust responsive text sizes using the `md:` and `lg:` prefixes

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-xl`, `px-6`) indicate size
- Color classes follow pattern: `{property}-{color}-{shade}`
  - Example: `text-purple-600`, `bg-blue-100`
- Responsive prefixes: 
  - `md:` (medium screens)
  - `lg:` (large screens)
  - Always keep these to maintain mobile responsiveness

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Avantages</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```

To update links:
1. Change `href="#services"` to your desired section ID or URL
2. Ensure section IDs match exactly (case-sensitive)
3. For external links, use complete URLs (e.g., `href="https://example.com"`)

### External Links
Current external links needing attention:
```html
<a href="www.valdeno-consulting.com">
<!-- Change to: -->
<a href="https://www.valdeno-consulting.com">
```

Remember:
- Always include `https://` for external links
- Verify all URLs work before publishing
- Update email addresses in contact sections

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Légal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
    </ul>
</div>
```

To add proper links:
1. Create new files: `privacy.html` and `terms.html`
2. Update the href attributes:
```html
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly
   - Example: `href="#Services"` won't link to `id="services"`

2. **Responsive Design Issues**
   - Keep all responsive classes (`md:`, `lg:`)
   - Test on different screen sizes
   - Don't remove `container` classes

3. **Styling Problems**
   - Maintain the class order in Tailwind
   - Don't remove `transition` classes
   - Keep `hover:` classes for interactive elements

4. **Link Issues**
   - Always include `https://` for external links
   - Check for typos in URLs
   - Verify email addresses in `mailto:` links

For additional help:
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers

Remember to back up your files before making significant changes, and always test your updates in a development environment first.