# Wedding Website Image Upload Guide

## Overview
This guide provides specifications and instructions for uploading images to your wedding website. All images should be placed in the `/images/` directory of your repository.

---

## Hero Background Images (Slideshow)

### Specifications
- **Dimensions:** 1920 x 1080px (16:9 aspect ratio) - minimum
- **Recommended:** 2560 x 1440px or higher for best quality
- **File Format:** PNG or JPG
- **File Size:** 500KB - 3MB per image (optimize for web)
- **Naming Convention:** `hero1.png`, `hero2.png`, `hero3.png`, etc.

### What Works Best
- High-quality engagement/portrait photos
- Images with clear subject focus (you and your partner)
- Consistent lighting and color tone across multiple images
- Minimal text overlay (images will have text on top)
- Slight movement/dynamic poses work well with the fade animation

### Current Setup
Your website currently displays **2 hero images** in a rotating slideshow:
- `images/hero2.png`
- `images/hero3.png`

The slideshow cycles every 12 seconds (6 seconds per image with smooth fade transition).

---

## Gallery Images

### Specifications
- **Dimensions:** Square format (1:1 aspect ratio) recommended, or 3:2
- **Recommended Size:** 1200 x 1200px (square) or 1800 x 1200px (3:2)
- **File Format:** PNG or JPG
- **File Size:** 300KB - 2MB per image
- **Naming Convention:** `photo1.jpg`, `photo2.jpg`, etc. OR `gallery-1.png`, `gallery-2.png`

### What Works Best
- Variety of angles and moments
- Clear, well-lit photos
- Consistent editing style
- Mix of close-ups and wide shots
- Square format displays best in the grid layout

### Current Setup
Your gallery section displays images referenced in the code. You can add as many images as desired - they'll automatically arrange in a responsive grid.

---

## How to Upload Images to GitHub

### Method 1: GitHub Web Interface (Easiest)
1. Go to your repository: `github.com/amanda-andrew/wedding`
2. Navigate to or create the `/images/` folder
3. Click "Add file" → "Upload files"
4. Drag and drop your images or click "choose your files"
5. Name them according to the naming conventions above
6. Commit with a message like "Add wedding hero images"

### Method 2: Git Command Line
```bash
# Navigate to your repo directory
cd wedding

# Create images folder if it doesn't exist
mkdir -p images

# Add your images to the images folder
# Copy/paste your files into: /images/

# Stage the images
git add images/

# Commit
git commit -m "Add wedding photos"

# Push to GitHub
git push origin main
```

### Method 3: GitHub Desktop
1. Open GitHub Desktop
2. Open your wedding repository
3. Click "Show in Explorer" (Windows) or "Show in Finder" (Mac)
4. Drag images into the `/images/` folder
5. Return to GitHub Desktop
6. Stage changes and commit

---

## Image Optimization Tips

### Before Uploading
1. **Resize to specifications** - Use Photoshop, GIMP, or online tools
2. **Compress for web** - Use TinyPNG, ImageOptim, or similar
3. **Maintain aspect ratios** - Don't distort images
4. **Color consistency** - Edit similarly if using multiple photos
5. **Remove unnecessary metadata** - Keep file sizes down

### Recommended Tools
- **Compression:** TinyPNG.com, ImageOptim
- **Resizing:** Photoshop, GIMP, Pixlr, Canva
- **Batch Processing:** ImageMagick (command line)
- **Quick Optimization:** Adobe Lightroom, Capture One

### File Format Choice
| Format | Best For | Pros | Cons |
|--------|----------|------|------|
| **JPG** | Photos | Smaller file size | Slight quality loss |
| **PNG** | Graphics, logos | Lossless quality | Larger file size |
| **WebP** | Modern web | Best compression | Limited browser support |

---

## Updating Images

### To Replace an Existing Image
1. Upload a new image with the same filename
2. This will overwrite the old image
3. Wait 5-10 minutes for cache to clear in browsers

### To Add More Hero Images
1. Upload new images as `hero4.png`, `hero5.png`, etc.
2. Update the CSS in `index.html` to reference new images:
```css
.slide:nth-child(3) {
    background-image: url("images/hero4.png");
    animation-delay: 12s;
}
```

### To Add More Gallery Images
1. Simply upload images to `/images/` folder with appropriate naming
2. Add HTML to the gallery section in `index.html`:
```html
<div class="gallery-item">
    <img src="images/photo3.jpg" alt="Amanda & Andrew moment 3">
</div>
```

---

## Troubleshooting

### Images Not Showing
- **Check file path:** Ensure images are in `/images/` folder with exact filename match
- **Check file format:** Verify file extension (.png, .jpg) is correct
- **Cache issue:** Hard refresh browser (Ctrl+F5 or Cmd+Shift+R)
- **File size:** Verify image file exists and isn't corrupted

### Images Loading Slowly
- **Compress images** - Reduce file size using TinyPNG or similar
- **Reduce dimensions** - Don't use images larger than recommended
- **Use JPG for photos** - Generally smaller than PNG

### Images Look Blurry
- **Upload higher resolution** - Try 2560 x 1440px or larger
- **Check compression** - Don't over-compress images
- **Verify original quality** - Ensure source image is high-quality

---

## Current Image Setup

### Hero Slideshow
- **Location:** `/images/` folder
- **Files:** `hero2.png`, `hero3.png`
- **Cycle Time:** 12 seconds (6 sec per image)
- **Animation:** Smooth fade with 35% overlay

### Gallery Section
- **Location:** `/images/` folder
- **Current Display:** 2 images in grid
- **Grid Type:** Responsive (2-3 columns on desktop, 1 on mobile)

---

## Best Practices

✅ **Do:**
- Use high-quality source images
- Compress before uploading
- Keep consistent editing style
- Name files clearly and descriptively
- Use landscape (16:9) for hero, square (1:1) for gallery
- Test on multiple devices after uploading

❌ **Don't:**
- Upload huge uncompressed files
- Use blurry or low-quality photos
- Mix very different editing styles
- Upload too many images (impacts load time)
- Use images with watermarks
- Forget to commit changes to GitHub

---

## Questions?

Refer to the main `README.md` for general website documentation.
For technical issues, check the `index.html` file for image path references.

---

**Last Updated:** August 4, 2026
**Website:** Amanda & Andrew Wedding
