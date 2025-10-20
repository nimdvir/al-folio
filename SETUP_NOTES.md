# Personal Website Setup Notes

This repository has been customized to create a personal website for Nim Dvir using the al-folio Jekyll theme.

## What's Been Done

### 1. Basic Configuration (_config.yml)
- Updated site title, name, and description
- Changed URL to `https://nimdvir.github.io`
- Updated blog name and description
- Changed favicon icon to 🚀
- Updated scholar information for publications
- Disabled external sources (Medium RSS, Twitter plugin) to avoid network issues

### 2. About Page (_pages/about.md)
- Personalized biography and introduction
- Updated subtitle to "Software Developer & Tech Enthusiast"
- Modified profile information section

### 3. Social Media Links (_data/socials.yml)
- Updated email address
- Added GitHub username: nimdvir
- Added LinkedIn username: nimdvir
- Added X/Twitter username: nimdvir
- Removed example InspireHEP and Google Scholar IDs

### 4. News Announcements (_news/)
- Created welcome announcement
- Added website launch announcement with details
- Updated announcement dates to October 2024

### 5. Resume (assets/json/resume.json)
- Updated name to Nim Dvir
- Changed label to "Software Developer & Tech Enthusiast"
- Updated email and contact information
- Added GitHub and LinkedIn profiles

### 6. Repositories (_data/repositories.yml)
- Set GitHub user to nimdvir
- Updated repository list to show relevant repos

### 7. Projects (_projects/1_project.md)
- Created a project entry for the personal website itself
- Documented technologies used (Jekyll, GitHub Pages, Bootstrap)

## Building the Site

The site has been successfully built using Docker. To build it yourself:

```bash
docker compose run --rm jekyll bundle exec jekyll build
```

To serve it locally for development:

```bash
docker compose run --rm jekyll bundle exec jekyll serve --host 0.0.0.0
```

Then visit http://localhost:8080 in your browser.

## Deployment

This site is configured to be deployed on GitHub Pages. The recommended workflow is:

1. Push changes to the `main` branch
2. GitHub Actions will automatically build and deploy the site
3. The site will be available at https://nimdvir.github.io/al-folio/

## Next Steps (Optional Customizations)

1. **Add Profile Picture**: Replace `assets/img/prof_pic.jpg` with your own photo
2. **Add More Projects**: Create new `.md` files in `_projects/` directory
3. **Write Blog Posts**: Add new posts in `_posts/` directory following the `YYYY-MM-DD-title.md` format
4. **Update CV**: Edit `_data/cv.yml` or `assets/json/resume.json` with full CV details
5. **Add Publications**: Edit `_bibliography/papers.bib` if you have academic publications
6. **Customize Theme Colors**: Edit `_sass/_themes.scss` to change the color scheme
7. **Remove Unused Pages**: Delete or disable pages you don't need (teaching, publications, etc.)

## Notes

- The CV data in `_data/cv.yml` already contains detailed information for Nim Dvir
- Some plugins (Twitter, external RSS) have been disabled to ensure the site builds in restricted network environments
- The site builds successfully with only warnings about citation fetching (Google Scholar, InspireHEP) due to network restrictions

## File Structure

```
.
├── _config.yml              # Main configuration file
├── _pages/                  # Website pages
│   ├── about.md            # Home page
│   ├── blog.md             # Blog listing
│   ├── projects.md         # Projects showcase
│   └── cv.md               # CV/Resume page
├── _data/                   # Data files
│   ├── socials.yml         # Social media links
│   ├── cv.yml              # CV data (YAML format)
│   └── repositories.yml    # GitHub repositories
├── _news/                   # News announcements
├── _projects/              # Project descriptions
├── _posts/                 # Blog posts
├── assets/
│   └── json/
│       └── resume.json     # CV data (JSON format)
└── _site/                  # Generated static site (after build)
```

## Support

For questions about the al-folio theme, visit:
- GitHub: https://github.com/alshedivat/al-folio
- Documentation: See CUSTOMIZE.md, FAQ.md, and INSTALL.md in this repository
