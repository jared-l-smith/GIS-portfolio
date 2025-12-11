# Projects Guide

This folder contains documentation for your GIS and remote sensing projects. Each project should have its own markdown file that describes what you did, how you did it, and what skills you demonstrated.

## What to Include

**Include projects that:**
- Demonstrate technical skills relevant to your career goals
- Show problem-solving and analytical thinking
- You're proud of and can discuss confidently
- Represent a range of GIS/remote sensing capabilities
- Include clear methods and outputs

**You don't need to include:**
- Every assignment you've ever completed
- Projects you didn't enjoy or connect with
- Work that doesn't represent your current skill level
- Projects where you can't clearly articulate what you did

**Remember**: Your portfolio should showcase your strengths and interests, not just check boxes. If you weren't interested in a particular project area, it's okay to leave it out.

## Project Types to Consider

- **Spatial Analysis**: Buffer analysis, overlay operations, site suitability, network analysis
- **Cartography**: Map design projects, thematic mapping, web map creation
- **Remote Sensing**: Image classification, change detection, NDVI analysis, band math
- **Data Processing**: Coordinate transformations, data cleaning, format conversions
- **Geoprocessing**: Model building, automation, batch processing
- **Field Data Collection**: GPS/GNSS surveys, mobile data collection
- **3D Analysis**: Terrain analysis, viewshed, surface modeling
- **UAV/UAS**: Drone data processing, photogrammetry workflows

## Writing Effective Project Descriptions

### The Methods Section is Critical

This is where you prove you know how to do GIS work. Be specific about:
- What tools/software you used
- What analysis functions or processes you applied
- How you handled data preparation
- What decisions you made and why

**Weak methods description:**
> "Used ArcGIS Pro to analyze population data."

**Strong methods description:**
> "Joined census demographic data to county boundaries using common FIPS codes. Normalized population counts by area to calculate population density. Applied quantile classification with 5 classes to show distribution patterns. Used ColorBrewer to select a colorblind-friendly sequential color scheme. Added appropriate map elements including scale bar, north arrow, legend, and data sources."

### Show Your Work

- Include the map, chart, or output
- Describe challenges you encountered and how you solved them
- Link to code if you wrote scripts
- Mention datasets and their sources
- Note any interesting findings

### Skills List

Be explicit about what skills each project demonstrates. Future you (and employers) need to quickly see what you're capable of.

Examples:
- Spatial join operations
- Raster calculator and band math
- Supervised classification (maximum likelihood)
- Python scripting with arcpy
- Database design and normalization
- Web map publishing and configuration

## Organizing Your Projects

**File naming:**
- Use descriptive, lowercase names with hyphens
- Examples: `watershed-analysis.md`, `urban-heat-island-study.md`, `census-mapping-project.md`

**Images:**
- Store in the main `images/` folder
- Name clearly: `watershed-analysis-map.png`
- Use PNG format for maps and screenshots
- Ensure images are high quality (300 dpi for print, clear for web)

**Linking to your homepage:**
- Add each project to your `index.md` or `index.html`
- Include a one-sentence description with the link
- Order by most recent, most complex, or by category

## Template Usage

Copy `project-template.md` for each new project:
1. Duplicate the template file
2. Rename it descriptively (e.g., `site-suitability-analysis.md`)
3. Fill in all sections with your project details
4. Add your map/output images
5. Link from your homepage

## Tips for Success

- **Document as you go**: Write project descriptions right after completing the work while methods are fresh
- **Update images**: Replace low-quality screenshots with polished versions
- **Proofread**: This is professional work - check spelling and grammar
- **Be honest**: Only include work you actually did (note collaborators if applicable)
- **Show progression**: It's okay to include earlier work that shows how you've improved
- **Get feedback**: Ask peers or instructors to review your descriptions

## Examples of Strong vs. Weak Projects

### Weak Project Entry
Title: GIS Project  
Date: Fall 2024  
Made a map of Colorado.

**Why it's weak**: Vague title, no context, no methods, no skills demonstrated, no visual.

### Strong Project Entry
Title: Colorado Wildfire Risk Assessment  
Date: October 2024  
Course: GIS 2040 - Raster Based GIS

**Overview**: Created a multi-criteria wildfire risk map for Colorado using raster analysis to identify high-risk areas based on vegetation, slope, aspect, and proximity to human development.

**Methods**:
- Acquired and processed 30m DEM for slope and aspect calculation
- Classified NLCD land cover data to identify vegetation types
- Created Euclidean distance rasters from roads and structures
- Reclassified all inputs to common 1-5 risk scale
- Applied weighted overlay analysis with domain expert input
- Generated final risk map with 5 risk categories

**Skills**: Raster analysis, DEM processing, reclassification, weighted overlay, multi-criteria analysis, spatial modeling

**Outputs**: [Includes clear map image]

**Why it's strong**: Clear title, specific methods, demonstrates multiple technical skills, includes context and outputs.

---

[Back to Main README](../README.md)
