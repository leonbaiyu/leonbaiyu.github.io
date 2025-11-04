# Leon Williams Personal Website

This repository contains the source code for Leon Williams' personal academic website, built with [Quarto](https://quarto.org/). The website is automatically published to GitHub Pages when changes are pushed to the repository.

## 🌐 Live Website

The website is live at: [https://leonbaiyu.github.io/](https://leonbaiyu.github.io/)

## 📁 Repository Structure

```
leonbaiyu.github.io/
├── _quarto.yml          # Main configuration file
├── index.qmd            # Homepage with blog post listing
├── about.qmd            # About page
├── styles.css           # Custom CSS styles
├── custom.scss          # SCSS customizations
├── posts/               # Blog posts directory
│   ├── _metadata.yml    # Post-wide settings
│   └── [post-folders]/  # Individual post directories
├── docs/                # Generated website files (published to GitHub Pages)
├── _site/               # Local build output
└── _extensions/         # Quarto extensions
```

## 🚀 Quick Start for Editing

### Prerequisites

1. **Install Quarto**: Download from [quarto.org](https://quarto.org/docs/get-started/). 
2. **Git**: Ensure you have Git installed for version control
3. **Text Editor**: VS Code, RStudio, or any markdown-capable editor

For Quarto install, make sure that if you're using VSCode, you install the extension then restart VSCode. After which quarto commands should be available in the terminal.

### Making Your First Edit

1. **Clone the repository** (if not already done):
   ```bash
   git clone https://github.com/leonbaiyu/leonbaiyu.github.io.git
   cd leonbaiyu.github.io
   ```

2. **Make your changes** (see sections below for specific edits)

3. **Preview locally**:
   ```bash
   quarto preview
   ```

4. **Build the site**:
   ```bash
   quarto render
   ```

5. **Commit and push**:
   ```bash
   git add .
   git commit -m "Description of your changes"
   git push origin main
   ```

## ✏️ Common Editing Tasks

### Adding a New Blog Post

1. **Create a new folder** in the `posts/` directory:
   ```bash
   mkdir posts/my-new-post
   ```

2. **Create an `index.qmd` file** in the new folder:
   ```bash
   touch posts/my-new-post/index.qmd
   ```

3. **Add frontmatter and content** to `index.qmd`:
   ```yaml
   ---
   title: "My New Post Title"
   author: "Leon Williams"
   date: "2024-11-04"
   categories: [research, tutorial]
   tags: [tag1, tag2]
   description: "Brief description of the post"
   image: "preview-image.jpg"  # optional
   ---

   # Your Post Content Here

   Write your post content using Markdown syntax...
   ```

4. **Add any images or files** to the same folder

5. **Preview and publish** following the Quick Start steps above

### Editing Existing Posts

1. **Navigate** to the post folder: `posts/[post-name]/`
2. **Edit** the `index.qmd` file
3. **Update the date** in the frontmatter if making significant changes
4. **Preview and publish** your changes

### Updating the About Page

1. **Edit** `about.qmd` in the root directory
2. **Use standard Markdown syntax** for content
3. **Modify the YAML frontmatter** to change page settings

### Changing Website Configuration

Edit `_quarto.yml` to modify:
- **Site title and description**
- **Navigation menu items**
- **Theme and styling**
- **Social media links**

Example navigation change:
```yaml
website:
  title: "Your Name"
  navbar:
    right:
      - about.qmd
      - text: "CV"
        href: "cv.pdf"
      - icon: github
        href: https://github.com/yourusername/
```
