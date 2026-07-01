# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for 곽준철 (Kwak Junched), a UX/UI Designer. Single-file HTML application with embedded CSS and JavaScript.

## Technology Stack

- **HTML5**: Single-file structure (`index.html`)
- **Tailwind CSS**: CDN-based styling (no build process)
- **Vanilla JavaScript**: Scroll animations, mobile menu toggle, smooth scrolling
- **Google Fonts**: Inter + Noto Sans KR

## Project Structure

```
my-profile-site/
└── index.html          # Complete portfolio (HTML + CSS + JS)
```

### Architecture

The entire site is contained in `index.html` with three main parts:

1. **HTML Sections** (lines 140-230)
   - Navigation bar (fixed, with mobile hamburger menu)
   - Hero section with profile photo placeholder
   - About section with experience stats
   - Skills section (categorized tags)
   - Experience timeline (6 companies)
   - Education section
   - Contact/footer

2. **CSS** (lines 18-130)
   - Custom CSS variables for colors and spacing
   - Tailwind utility classes for layout
   - Custom animations: fade-in, hover effects, hamburger menu
   - Mobile-first responsive design with `@media (max-width: 768px)`

3. **JavaScript** (lines 232-267)
   - Hamburger menu toggle for mobile
   - Smooth scroll behavior for anchor links
   - Intersection Observer for fade-in animations on scroll

### Design System

**Color Palette** (CSS variables):
- `--bg-primary: #0d0d12` (main background)
- `--bg-secondary: #1a1a23` (card/secondary background)
- `--text-primary: #ffffff` (primary text)
- `--text-secondary: #b0b0b0` (secondary text)
- `--accent: #3b82f6` (blue accent for buttons/links)

**Key Components**:
- `.section-label`: Small uppercase section markers (`/ SECTION NAME`)
- `.fade-in`: Elements that animate in on scroll
- `.skill-tag`: Styled tag buttons for skills
- `.experience-card`: Timeline card with left border accent
- `.cta-button`: Primary call-to-action button

## Development

### Viewing the Site
Simply open `index.html` in a browser:
```bash
open index.html
```

### Making Changes
1. Edit `index.html` directly
2. Refresh browser to see changes
3. No build process required

### Customization Points

- **Hero Profile Image**: Replace emoji placeholder (line 181) with actual image or different emoji
- **Content**: All text is directly in HTML sections—no external content files
- **Colors**: Modify CSS variables at the top of `<style>` tag (lines 23-32)
- **Typography**: Google Fonts can be swapped in the `<link>` tag (line 12)
- **Social Links**: Add/edit icon links in hero section and contact section
- **Mobile Breakpoint**: Currently at 768px (line 115)—adjust if needed

## Mobile Responsiveness

Site is fully responsive. Key breakpoints:
- Desktop: Full layout with 2-column hero section
- Mobile (< 768px): Stacked layout, hamburger menu for nav, reduced image sizes

## No Build Tools

This project intentionally uses no build tools, preprocessors, or npm. Everything is vanilla HTML/CSS/JS + CDN links. Advantages:
- No dependencies or lock files
- Single file to manage
- Works immediately in any browser
- Easy to share/deploy

## Future Enhancements to Consider

- Replace emoji placeholder with actual profile image (JPG/PNG)
- Add dark/light theme toggle
- Consider adding a simple blog or project showcase section
- Add form handling for contact section (requires backend service)
- Preload profile image or add lazy loading if adding media
