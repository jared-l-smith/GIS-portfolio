# Images Folder

This folder stores all images, maps, screenshots, and visual content for your portfolio.

## What to Store Here

**Maps and cartographic outputs:**
- Finished maps from projects
- Map layouts and compositions
- Cartographic products

**Screenshots:**
- Web application interfaces
- Dashboard views
- Software workflows
- Analysis outputs

**Charts and graphs:**
- Data visualizations
- Statistical graphics
- Infographics

**Diagrams:**
- Workflow diagrams
- ERD diagrams (can also be PDFs in database folder)
- Poster thumbnails
- Process flowcharts

**Photos (if relevant):**
- Field work photos (equipment, sites)
- Professional headshot (if you choose to include one)

## File Formats

**Recommended formats:**
- **PNG** - Best for maps, screenshots, diagrams (supports transparency)
- **JPG/JPEG** - Good for photos, smaller file sizes
- **SVG** - Vector graphics (if needed)

**Avoid:**
- TIFF or other large uncompressed formats
- BMP files
- Unnecessarily large file sizes

## File Naming Best Practices

**Use descriptive, consistent names:**
- `wildfire-risk-map.png`
- `urban-heat-dashboard-screenshot.png`
- `parks-database-erd.png`
- `poster-thumbnail-water-quality.png`

**Avoid:**
- Generic names: `image1.png`, `map.png`, `screenshot.png`
- Spaces: `my map.png` (use hyphens instead)
- Special characters: `map@project#1.png`

## Image Quality Guidelines

**For maps and technical content:**
- Export at 300 DPI for print quality
- Use at least 150 DPI for web (higher is better)
- Ensure text is readable when viewed at normal size
- Test that colors display correctly

**For screenshots:**
- Capture at actual display resolution
- Crop to remove unnecessary content
- Ensure interface elements are clear and readable

**File size considerations:**
- Optimize images to balance quality and file size
- Very large images (>5MB) may slow page loading
- Use PNG compression or reduce dimensions if needed
- GitHub has file size limits (100MB per file, 1GB per repo recommended max)

## Organization Tips

**Keep it simple:**
- All images in this one folder (don't create subfolders unless you have 50+ images)
- Use clear naming to identify which project each image belongs to
- Delete unused images periodically

**Reference in markdown:**
Images are referenced in your project files like this:
```markdown
![Description of image](../images/your-image-name.png)
```

The `../` means "go up one folder level" from the projects folder to access images.

## Privacy and Content

**Before uploading images:**
- Remove any personal information from map layouts (your name, if privacy is a concern)
- Check metadata - some image formats store location data, author info, etc.
- Ensure you have permission to share any data shown in maps
- Don't include confidential or proprietary information
- Verify that project locations don't reveal personal addresses

**Editing metadata:**
- Use image editing software to remove EXIF data if needed
- Many PDF editors allow removing author/creator information
- Screenshot tools typically don't embed personal metadata

## Getting Started

1. **Export your first map or screenshot**
2. **Name it descriptively** (e.g., `census-mapping-final.png`)
3. **Upload to this folder** via GitHub web interface or git commands
4. **Reference it in your project markdown** using the syntax above
5. **Verify it displays correctly** on your live GitHub Pages site

---

[Back to Main README](../README.md)
