# Image Usage Guide for Jekyll Blog Posts

This guide explains how to add and manage images in your Jekyll blog posts.

## Directory Structure

```
yhdenhengenlukupiiri/
├── assets/
│   └── images/          # Store all blog post images here
│       ├── book-covers/
│       ├── author-photos/
│       └── illustrations/
├── _posts/
└── _site/
```

## Adding Images to Blog Posts

### 1. Basic Markdown Image Syntax

```markdown
![Alt text describing the image](/assets/images/filename.jpg)
```

**Example:**
```markdown
![Book cover of Jhumpa Lahiri's collection](/assets/images/book-cover-placeholder.svg)
```

### 2. Image with Title (Tooltip)

```markdown
![Alt text](/assets/images/filename.jpg "Title that appears on hover")
```

### 3. Image as a Link

```markdown
[![Alt text](/assets/images/filename.jpg)](https://example.com)
```

### 4. HTML Image Tag (More Control)

```html
<img src="/assets/images/filename.jpg" alt="Alt text" width="400" height="300">
```

### 5. Responsive Image

```html
<img src="/assets/images/filename.jpg" alt="Alt text" style="max-width: 100%; height: auto;">
```

### 6. Centered Image

```html
<div style="text-align: center;">
  <img src="/assets/images/filename.jpg" alt="Alt text" style="max-width: 100%; height: auto;">
</div>
```

## Image Organization Best Practices

### File Naming Convention
- Use lowercase letters and hyphens: `book-cover-jhumpa-lahiri.jpg`
- Include relevant keywords: `author-photo-murakami.jpg`
- Add dimensions if needed: `book-cover-large-800x600.jpg`

### Directory Organization
```
assets/images/
├── book-covers/         # Book cover images
├── author-photos/       # Author photographs
├── illustrations/       # Custom illustrations
├── screenshots/         # Screenshots or diagrams
└── thumbnails/          # Smaller versions of images
```

### Image Optimization

1. **Compress images** before uploading
   - Use tools like TinyPNG, ImageOptim, or online compressors
   - Aim for file sizes under 500KB for web

2. **Choose appropriate formats:**
   - **JPG**: Photos and complex images
   - **PNG**: Graphics with transparency
   - **SVG**: Scalable vector graphics (logos, icons)
   - **WebP**: Modern format with better compression (if supported)

3. **Responsive images:**
   - Create multiple sizes for different screen sizes
   - Use `srcset` attribute for responsive images

## Advanced Image Techniques

### Image with Caption

```html
<figure>
  <img src="/assets/images/filename.jpg" alt="Alt text" style="max-width: 100%; height: auto;">
  <figcaption>Caption describing the image</figcaption>
</figure>
```

### Multiple Images in a Row

```html
<div style="display: flex; gap: 10px; flex-wrap: wrap;">
  <img src="/assets/images/image1.jpg" alt="Image 1" style="flex: 1; min-width: 200px;">
  <img src="/assets/images/image2.jpg" alt="Image 2" style="flex: 1; min-width: 200px;">
</div>
```

### Image Gallery

```html
<div class="image-gallery">
  <img src="/assets/images/image1.jpg" alt="Image 1">
  <img src="/assets/images/image2.jpg" alt="Image 2">
  <img src="/assets/images/image3.jpg" alt="Image 3">
</div>
```

## Troubleshooting

### Image Not Displaying
1. Check the file path is correct (starts with `/assets/images/`)
2. Verify the image file exists in the correct directory
3. Ensure the image file is not corrupted
4. Check file permissions

### Image Too Large/Small
- Use HTML `<img>` tag with `width` and `height` attributes
- Add CSS styling for responsive behavior
- Consider creating multiple image sizes

### Performance Issues
- Compress images before uploading
- Use appropriate image formats
- Consider lazy loading for multiple images

## Example Blog Post Structure

```markdown
---
layout: post
title: "Book Review: Example Title"
date: 2025-01-15
---

![Book cover](/assets/images/book-covers/example-book.jpg)

## Introduction

Your review content here...

![Author photo](/assets/images/author-photos/author-name.jpg)

## Review Content

More content with images...

<div style="text-align: center;">
  <img src="/assets/images/illustrations/reading-nook.jpg" alt="Cozy reading nook" style="max-width: 100%; height: auto;">
  <p><em>The perfect reading environment</em></p>
</div>
```

## Tools and Resources

- **Image Compression**: [TinyPNG](https://tinypng.com/), [ImageOptim](https://imageoptim.com/)
- **Image Editing**: GIMP, Photoshop, Canva
- **Online Converters**: Convertio, CloudConvert
- **SVG Creation**: Inkscape, Adobe Illustrator, Figma

Remember to always include meaningful alt text for accessibility!
