# GitHub Copilot Instructions

## Purpose & Goal
**Document curiosities and challenge conventional thinking** through:
- Exploring unconventional approaches to design and development
- Questioning standard patterns and accepted norms
- Sharing experiments and thought-provoking insights
- Creating a space for intellectual exploration rather than optimization

## Repository Overview

This is Sudhanshu Gautam's personal portfolio website built with Jekyll and deployed to GitHub Pages. The site showcases AI-assisted development projects, work experience at Wikimedia Foundation, and includes a blog section focusing on UX design and AI collaboration.

## Technology Stack

- **Static Site Generator**: Jekyll 4.3
- **Language**: Ruby (Jekyll), HTML/CSS, Liquid templating
- **Deployment**: GitHub Pages via GitHub Actions
- **Content**: Markdown for blog posts, HTML for main pages
- **Styling**: Custom CSS with a focus on clean, minimal design

## Project Structure

```
.
├── _config.yml          # Jekyll configuration
├── _layouts/            # HTML templates
│   ├── default.html     # Main layout with header/footer
│   └── post.html        # Blog post layout
├── _posts/              # Blog posts (Markdown)
├── .github/
│   ├── workflows/       # GitHub Actions for deployment
│   └── copilot-instructions.md # This file
├── index.html           # Main portfolio page
├── landing-variations.html # Design variations showcase
├── landing-concepts/    # Alternative design prototypes
│   ├── variant-a.html   # Design variation A
│   ├── variant-b.html   # Design variation B
│   ├── variant-c.html   # Design variation C
│   ├── variant-d.html   # Design variation D
│   └── *.css           # Individual stylesheets per variant
├── style.css           # Main site stylesheet
├── writing/            # Blog section
│   └── index.md        # Blog index page
├── Gemfile             # Ruby dependencies
└── .gitignore          # Git ignore rules
```

## Development Environment

### Prerequisites
- Ruby 3.1+ with Bundler
- Jekyll 4.3+
- Git

### Setup
```bash
# Install dependencies
bundle install

# Run development server
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

### Local Development
- Development server runs on `http://localhost:4000`
- Auto-regeneration enabled by default
- Livereload available with `--livereload` flag

## Coding Guidelines

### Content Creation

#### Blog Posts
- Place new posts in `_posts/` directory
- Use filename format: `YYYY-MM-DD-title.md`
- Include front matter:
```yaml
---
title: "Post Title"
date: YYYY-MM-DD
description: "Brief description for SEO"
---
```

#### Portfolio Content
- Main portfolio content is in `index.html`
- Update work experience in the timeline section
- Add new projects to the "Featured Work" section
- Design variations are in `landing-concepts/` directory for experimentation
- Alternative layouts accessible via `landing-variations.html`
- Maintain the existing card-based layout structure

### Styling Guidelines
- Use semantic HTML elements
- Follow the existing CSS architecture in `style.css`
- Maintain responsive design principles
- Use CSS Grid and Flexbox for layouts
- Prefer CSS custom properties for theming

### Design Principles
- **Minimalism**: Clean, uncluttered design
- **Typography-first**: Strong emphasis on readable content
- **Professional**: Suitable for a product builder/designer portfolio
- **AI-forward**: Highlight AI-assisted development workflow

## Content Guidelines

### Voice & Tone
- Professional yet approachable
- Focus on practical insights about AI-assisted development
- Share specific examples and case studies
- Maintain authenticity about AI collaboration experiences

### Blog Content Focus
- AI-assisted development workflows
- UX design insights
- Product building experiences
- Technical tutorials and reflections

## Deployment

### Automatic Deployment
- Pushes to `main` branch trigger GitHub Actions
- Site builds and deploys automatically to GitHub Pages
- Build process includes Jekyll compilation and artifact upload

### Manual Deployment
Not typically needed due to GitHub Actions, but can be done via:
```bash
bundle exec jekyll build
# Upload _site/ contents to hosting provider
```

## Best Practices

### Performance
- Optimize images before adding to repository
- Use appropriate image formats (WebP when possible)
- Keep CSS and JavaScript minimal
- Leverage Jekyll's built-in asset optimization

### SEO & Accessibility
- Include proper meta descriptions
- Use semantic HTML structure
- Maintain heading hierarchy
- Ensure color contrast meets accessibility standards
- Add alt text for images

### Content Strategy
- Regular blog posts about AI development experiences
- Update portfolio projects with new work
- Keep technology stack current
- Share practical insights and learnings

## Priority Focus Areas (in order)
1. **Clarity of Thought** - Ideas should be expressed clearly and provocatively
2. **Experimentation** - Embrace unconventional approaches and challenge norms
3. **Authenticity** - Raw, honest documentation of process and thinking
4. **Depth over Polish** - Prioritize substantive content over perfect presentation
5. **Intellectual Curiosity** - Make space for questions, doubts, and exploration

## Content Philosophy
When making changes, consider:
- Does this challenge conventional thinking or present a fresh perspective?
- Will this provoke thought or spark curiosity?
- Is this authentic documentation of my actual process and questions?
- Does this prioritize substance over surface-level polish?
- Am I questioning the status quo rather than following best practices blindly?

## GitHub Copilot Usage

When working on this repository, GitHub Copilot should:

1. **Understand Context**: This is a space for intellectual exploration and questioning conventional wisdom
2. **Maintain Style**: Follow the existing minimal design, but don't be afraid to experiment
3. **Content Awareness**: Suggest content that challenges norms and provokes thought
4. **Technical Alignment**: Generate Jekyll-compatible code and proper Liquid syntax
5. **Authenticity Over Optimization**: Prioritize genuine expression over SEO or conversion metrics
6. **Curiosity Driven**: Encourage experimentation, questioning, and unconventional approaches

### Common Tasks
- Adding new blog posts with proper front matter
- Updating portfolio sections with new projects
- Maintaining responsive CSS layouts
- Optimizing for GitHub Pages deployment

## Contribution Notes

- This is a personal portfolio, but contributions should maintain the professional, minimal aesthetic
- All changes should be tested locally before pushing
- New content should align with the AI-assisted development theme
- Maintain the existing file organization and naming conventions

## Troubleshooting

### Common Issues
- **Bundle install fails**: Ensure Ruby version compatibility
- **Build errors**: Check Jekyll syntax and front matter formatting
- **Deployment fails**: Verify GitHub Actions workflow and permissions
- **Styling issues**: Test across different viewport sizes

For technical issues, refer to Jekyll documentation and GitHub Pages troubleshooting guides.