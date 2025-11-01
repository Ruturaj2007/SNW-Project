# PetCare Guide

A comprehensive website providing pet care tips and advice for dogs, cats, and birds.

## Description

PetCare Guide is a responsive, multi-page website that offers detailed care information for three types of pets: dogs, cats, and birds. The site features a consistent design system with unified styling, proper navigation, and optimized image assets.

## How to Run Locally

To run the site locally, use Python's built-in HTTP server:

```bash
python -m http.server 8000
```

Then open your browser and navigate to:
- Home: `http://localhost:8000/index.html`
- Dogs: `http://localhost:8000/dog.html`
- Cats: `http://localhost:8000/cat.html`
- Birds: `http://localhost:8000/birds.html`

## Project Structure

```
Project Copy 2/
├── assets/
│   └── images/
│       ├── golden-retriever-tongue-out.jpg
│       ├── istockphoto-1443562748-612x612.jpg
│       └── mybird_sun_conure_on_perch-900x651.jpg
├── index.html
├── dog.html
├── cat.html
├── birds.html
├── style.css
├── dog.css
├── cat.css
├── birds.css
└── README.md
```

## Files Changed

### CSS Files
- **style.css**: Enhanced with Google Fonts (Inter for display, Merriweather for body), consolidated all CSS variables in `:root` as single source of truth. Added missing variables (`--primary-darker`, `--subtext-light`, `--accent-light`) referenced by page-specific styles.

### HTML Files
- **index.html**: Fixed navigation links (`dogs.html` → `dog.html`, `cats.html` → `cat.html`), updated card links, ensured proper head structure.
- **dog.html**: Added `dog.css` link, fixed navigation links, updated image path to `assets/images/golden-retriever-tongue-out.jpg`.
- **cat.html**: Added `cat.css` link, fixed navigation links, updated image path to `assets/images/istockphoto-1443562748-612x612.jpg`.
- **birds.html**: Added `birds.css` link, fixed navigation links, updated image path to `assets/images/mybird_sun_conure_on_perch-900x651.jpg`.

### Page-Specific CSS Files
- **dog.css**, **cat.css**, **birds.css**: Verified no duplicate `:root` variable declarations. These files only contain page-specific overrides and component styles.

### Assets
- Created `assets/images/` directory structure.
- Moved all images from root to `assets/images/` folder for better organization.

## Commit History

The following commits were made to implement these changes:

1. **chore: add image assets** - Created `assets/images/` directory and moved three images (golden-retriever-tongue-out.jpg, istockphoto-1443562748-612x612.jpg, mybird_sun_conure_on_perch-900x651.jpg) from root to assets folder.

2. **refactor: unify styles into style.css** - Enhanced `style.css` with Google Fonts import and added missing CSS variables (`--primary-darker`, `--subtext-light`, `--accent-light`) to ensure all page-specific styles can reference global variables.

3. **feat: link style.css & update HTML heads** - Updated all HTML files to include page-specific CSS links (`dog.css`, `cat.css`, `birds.css`) after `style.css`. Standardized `<head>` sections and fixed navigation links across all pages (Home → index.html, Dogs → dog.html, Cats → cat.html, Birds → birds.html).

4. **fix: update image paths and minor layout tweaks** - Updated all image references in HTML files to use the new `assets/images/` path structure. All images now load from the centralized assets folder.

5. **docs: add README with run instructions** - Added comprehensive README.md documenting project structure, how to run locally, files changed, and commit history.

## Acceptance Criteria

✅ All pages use `style.css` as the global stylesheet and rely on variables in `:root` for fonts/colors.  
✅ Per-page CSS (`dog.css`, `cat.css`, `birds.css`) only contains overrides and does not redefine variables.  
✅ Images are in `assets/images/` and page references are updated to that folder.  
✅ Navigation works correctly - all links point to the correct pages (`index.html`, `dog.html`, `cat.html`, `birds.html`).  
✅ Pages load with no 404s for CSS or images when tested locally.  
✅ A brief README.md is added describing how to run the site and what changed.  
✅ The repo has the commits described in the commit plan.

## Design System

The site uses CSS variables defined in `style.css` for consistent theming:

- **Colors**: Primary green (#17cf17), background variants, text colors
- **Fonts**: Inter (display) and Merriweather (body) from Google Fonts
- **Spacing**: Consistent radius, shadow, and transition values
- **Responsive**: Mobile-first design with breakpoints for tablets and desktops

All page-specific styles extend these global variables, ensuring visual consistency across the entire site.

