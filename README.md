# GIS Portfolio Template

A template repository for creating a professional GIS portfolio hosted on GitHub Pages.

## First Steps (Start Here!)

Your goal today: Get a live portfolio website with at least one project documented.

1. **Create a GitHub account (if you don't have one)** - Choose a professional username like `firstname-lastname`, `firstnamelastname`, or `firstname-lastinitial`. If your name is taken, try `firstname-middleinitial-lastname` or `firstinitial-lastname`. Avoid numbers, birth years, or old gamer tags - this username will be part of your portfolio URL: `yourusername.github.io`
2. **Create your portfolio repository** - Click "Use this template" and name it `GIS Portfolio` ([see detailed instructions](#1-create-your-portfolio-repository))
4. **Enable GitHub Pages** - Turn on Pages in repository Settings ([see detailed instructions](#2-enable-github-pages))
5. **Edit your Configuaration YML file** - Find the file called '_config.yml' and edit the contents, clicking Commit Changes when you're done. This will adjust the name on your Portfolio pages.
6. **Edit your homepage** - Update `index.md` with your name, education, and contact info ([see Homepage Guide](homepage-guide.md) for what to include, and [detailed how-to instructions](#3-customize-your-portfolio))
7. **Add your first project** - Copy `project-template.md`, fill it out for one completed project, and link it from your homepage ([see detailed instructions](#4-adding-new-projects))
8. **Check your live site** - Visit `https://yourusername.github.io/gis-portfolio` and see your portfolio live!

**Don't worry about making it perfect.** Start simple and build from there.

## Next Steps (Build Over Time)

Once you have the basics working, grow your portfolio as you complete coursework:

- **After each major project**: Document it using the project template (5-10 minutes while methods are fresh)
- **Add content types as you create them**: Writing samples, posters, database designs, web applications (see File Structure below)
- **Customize your design**: Explore HTML/CSS if you want more control (see Learning Resources below)
- **Review each semester**: Update skills, remove weak projects, ensure everything is current
- **Read about paper portfolios**: See the [Paper Portfolio Guide](paper-portfolio-guide.md) for preparing print versions for interviews
- **Prepare for job hunting**: Review the [Portfolio Design Guide](portfolio-design-guide.md) for creating effective portfolio content
- **Consider a custom domain**: When you're ready for a more professional URL ([optional, see instructions below](#using-a-custom-domain-optional))

**The key**: Update regularly, not all at once before job applications.

## Paper Portfolios for Interviews

While your online portfolio is essential for applications and networking, you should also prepare a **paper portfolio** to bring to in-person interviews. A physical portfolio:
- Gives you and the interviewer something tangible to discuss
- Demonstrates preparation and professionalism
- Works without technology or internet connections
- Can be left with interviewers for further review
- Helps you control the conversation and highlight your best work

Your paper portfolio should be selective (5-8 projects), professionally printed, and organized in a presentation folder or binder. See the complete [Paper Portfolio Guide](paper-portfolio-guide.md) for detailed instructions on:
- Selecting content from your online portfolio
- Including writing samples and posters
- Formatting for print
- Assembly and organization
- Using your portfolio effectively in interviews

**Start with your online portfolio, then create a print version when you're ready to interview.**

## Table of Contents
- [Getting Started](#getting-started)
  - [1. Create Your Portfolio Repository](#1-create-your-portfolio-repository)
  - [2. Enable GitHub Pages](#2-enable-github-pages)
  - [3. Customize Your Portfolio](#3-customize-your-portfolio)
  - [4. Adding New Projects](#4-adding-new-projects)
- [Portfolio Maintenance Tips](#portfolio-maintenance-tips)
- [File Structure](#file-structure)
- [Using a Custom Domain (Optional)](#using-a-custom-domain-optional)
- [Questions?](#questions)
- [Learning Resources](#learning-resources)

## Getting Started

### 1. Create Your Portfolio Repository

1. Click the green "Use this template" button at the top of this repository
2. Name your new repository `GIS Portfolio`
4. - You can set it to private for now, if you'd like, but be aware you can't look at or create web pages with a private repository.
5. Click "Create repository"

### 2. Enable GitHub Pages

1. Go to your new repository's **Settings**
2. Scroll down to **Pages** (in the left sidebar under "Code and automation")
3. Under **Source**, select **Deploy from a branch** (not GitHub Actions - that's for advanced workflows)
4. Under **Branch**, select `main` branch
5. Click **Save**
6. Your portfolio will be live at `https://yourusername.github.io/gis-portfolio` (may take a few minutes)

### 3. Customize Your Portfolio

**Note:** You'll edit files directly in GitHub's web interface. To see your changes live, commit them and wait a few minutes for GitHub Pages to rebuild your site (usually 1-2 minutes). You can't preview changes before committing when working in the web interface.

#### Edit the Homepage

By default, the template uses `index.md` (markdown), which is easier for beginners. GitHub Pages will automatically style it for you.

**Option A: Use Markdown (Default - Recommended for Beginners)**
- Edit `index.md` with your information
- Replace all `[placeholder text]` with your actual information
- GitHub Pages will automatically style it

**Option B: Use HTML (More Control)**
- Rename `index.html.example` to `index.html`
- Delete `index.md`
- Edit `index.html` with your information
- Add custom CSS/styling as desired

**Important:** Only keep ONE index file (`index.md` OR `index.html`), not both.

#### Add Your First Project

1. Go to the `projects/` folder
2. Copy `project-template.md` and rename it (e.g., `watershed-analysis.md`)
3. Fill in your project details following the template structure
4. Add any images to the `images/` folder
5. Link to your new project from `index.md` or `index.html`

#### What About Empty Folders?

The template repository includes folders for `writing/`, `posters/`, and `webapps/` with template files. **You only need ONE repository** - this is both your template and your live portfolio.

**If you don't have content for a section yet:**
- Keep the folders and template files in your repository (they won't affect your live site)
- Comment out or remove those sections from your homepage until you have content
- GitHub Pages only displays what you link to from `index.md` or `index.html`

**Example - commenting out sections in `index.md`:**
```markdown
## Projects
- [Project 1](projects/project1.md) - Description

<!-- Uncomment these sections when you have content to add:

## Web Applications
- [Web Apps](webapps/webapps.md)

## Writing & Posters
- [Writing Samples](writing/writing-samples.md)
- [Posters](posters/posters.md)

-->
```

As you create dashboards, posters, or writing samples, uncomment the relevant sections and add your content to the template files.

### 4. Adding New Projects

For each project you complete:

1. Copy `projects/project-template.md`
2. Rename it descriptively (e.g., `census-mapping.md`)
3. Fill in all sections:
   - Project title and metadata
   - Overview
   - Methods (be specific!)
   - Skills demonstrated
   - Outputs (include images)
   - Challenges/solutions (optional)
   - Links to code/data (optional)
4. Add images to the `images/` folder
5. Update your homepage to link to the new project
6. Commit and push changes

## Portfolio Maintenance Tips

- **Update regularly**: Add projects as you complete them, not months later
- **Be specific in methods**: Future you (and employers) need to understand what you actually did
- **Include visuals**: Maps, charts, workflow diagrams, code screenshots
- **Link to code**: If you have analysis code in another repo, link to it
- **Proofread**: This is a professional document

### Growing Your Portfolio Beyond the Basics

GitHub Pages is more flexible than you might think. While this template uses simple markdown and HTML, you can add:

**Advanced Features (all free on GitHub Pages):**
- Interactive elements and animations (CSS, JavaScript)
- Responsive design and mobile optimization
- Interactive web maps (Leaflet, Mapbox GL JS)
- Data visualizations (D3.js, Chart.js)
- Custom styling and themes
- Multi-page layouts
- Client-side interactivity (buttons, modals, image galleries)

**What GitHub Pages Cannot Do:**
- Server-side processing (PHP, Python backends, databases)
- Contact forms that send email (you'll need a third-party service)
- Content management systems (no WordPress, Drupal)

**When to Consider Other Hosting:**
If you need a blog with CMS, complex backend functionality, or prefer drag-and-drop editing, consider platforms like Squarespace, Wix, or self-hosted WordPress. However, for most GIS/technical portfolios, GitHub Pages provides everything you need with the added benefits of version control and free hosting.

Start here, and only upgrade if you hit specific limitations.

## File Structure

```
yourusername.github.io/
├── README.md          (this file - you can keep or delete)
├── index.md           (your portfolio homepage - markdown version, DEFAULT)
├── index.html.example (your portfolio homepage - HTML version, rename to use)
├── projects/
│   ├── project-template.md
│   └── [your-project-files.md]
├── writing/
│   ├── [research-papers.pdf]
│   ├── [lab-reports.pdf]
│   └── writing-samples.md (optional landing page)
├── posters/
│   ├── [conference-posters.pdf]
│   └── posters.md (optional landing page with thumbnails)
├── webapps/
│   └── webapps.md (links to Dashboards, Experience Builder, StoryMaps, etc.)
├── database/
│   ├── [ERD-diagrams.pdf or .png]
│   ├── [schema-documentation.pdf]
│   └── database-projects.md (optional landing page)
└── images/
    ├── README.md      (guide for organizing and optimizing images)
    └── [your-images]
```

**Note:** Each folder contains a README guide explaining what to include and how to organize that type of content. Start with the guides, then use the templates.

### Expanding Your Portfolio

As you progress through your program, you can add additional content types:

**Writing Samples** (`writing/` folder)
- Upload PDFs of lab reports, research papers, technical memos
- Create a `writing-samples.md` page that links to and describes each document

**Posters** (`posters/` folder)  
- Upload PDFs of scientific or conference posters
- Create thumbnail images for preview
- Link from a `posters.md` landing page

**Web Applications** (`webapps/` folder)
- Create a page linking to your ArcGIS Online content:
  - Dashboards
  - Experience Builder applications
  - StoryMaps
  - Web maps
  - Survey123 forms
- Include screenshots, descriptions, and links to live applications
- Note: Your AGOL account persists after graduation specifically so you can maintain these portfolio pieces

**Database Design** (`database/` folder)
- Upload ERD (Entity-Relationship Diagram) images or PDFs
- Include database schema documentation
- Document spatial database design projects
- Show geodatabase design, data modeling, and optimization work
- Create a `database-projects.md` landing page describing your database work

## Using a Custom Domain (Optional)

You can use a custom domain (e.g., `yourname.com`) instead of `yourusername.github.io`. This is completely optional - the free GitHub URL works great for a professional portfolio.

**Why use a custom domain?**
- More memorable and professional URL
- Your portfolio URL won't change if you change your GitHub username
- Demonstrates additional technical skills

**Cost:** Typically $10-15 per year

**How to set it up:**

1. **Purchase a domain** from a domain registrar like:
   - [Squarespace Domains](https://domains.squarespace.com/)
   - [Cloudflare](https://www.cloudflare.com/products/registrar/)

2. **Add the domain to GitHub Pages:**
   - Go to your repository **Settings** → **Pages**
   - Under **Custom domain**, enter your domain (e.g., `yourname.com`)
   - Click **Save**

3. **Configure DNS settings:**
   - Follow [GitHub's documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) for your specific registrar
   - This connects your purchased domain to your GitHub Pages site

## Questions?

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Homepage Guide](homepage-guide.md) - Tips for creating an effective portfolio homepage
- [Portfolio Design Guide](portfolio-design-guide.md) - Tips for creating effective portfolio content
- [Paper Portfolio Guide](paper-portfolio-guide.md) - Creating a print portfolio for interviews
- Ask your instructor!

## Learning Resources

### HTML Tutorials
- [W3Schools HTML Tutorial](https://www.w3schools.com/html/) - beginner-friendly with examples
- [MDN Web Docs: HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) - comprehensive guide
- [freeCodeCamp](https://www.freecodecamp.org/) - interactive lessons and projects
- [HTML Cheat Sheet](https://htmlcheatsheet.com/) - quick reference

### Markdown
- [Markdown Guide](https://www.markdownguide.org/) - complete markdown reference

### Portfolio Design
- [How to Build a Science Portfolio That Gets You Hired](https://www.linkedin.com/pulse/how-build-science-portfolio-gets-you-hired-just-one-weekend-0hwhc/) - practical advice for science portfolios
