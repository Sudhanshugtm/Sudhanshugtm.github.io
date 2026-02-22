# Portfolio Improvement Agent

This agent is responsible for making small, meaningful improvements to the portfolio website on a daily basis.

## Objective

Make ONE focused improvement per day to enhance the portfolio's quality, accessibility, performance, or user experience.

## Types of Improvements

### 1. Content Enhancements
- Improve clarity and conciseness of copy
- Fix typos or grammatical errors
- Update project descriptions with more specific metrics or outcomes
- Enhance meta descriptions for better SEO
- Add or improve alt text for semantic elements

### 2. Design & UX Refinements
- Improve color contrast for better accessibility (WCAG AA compliance)
- Fine-tune spacing and typography for better readability
- Enhance hover states and interactive feedback
- Improve responsive design breakpoints
- Optimize visual hierarchy

### 3. Performance Optimizations
- Reduce CSS redundancy
- Optimize asset loading
- Improve semantic HTML structure
- Add performance hints (preconnect, dns-prefetch)

### 4. Code Quality
- Improve code organization and maintainability
- Add meaningful comments where helpful
- Ensure consistent code style
- Remove unused CSS or HTML

### 5. Accessibility Improvements
- Enhance keyboard navigation
- Improve screen reader compatibility
- Add ARIA labels where appropriate
- Ensure proper heading hierarchy
- Improve focus indicators

### 6. Documentation
- Update README with new features
- Improve inline documentation
- Add helpful code comments

## Guidelines

1. **One Change at a Time**: Make only ONE improvement per run to keep changes focused and reviewable
2. **Meaningful Impact**: Each change should have clear value for users or maintainability
3. **No Breaking Changes**: Never remove or modify working features
4. **Test Compatibility**: Ensure changes work across different screen sizes
5. **Maintain Design Language**: Keep the existing minimal, professional aesthetic
6. **Document Changes**: Include clear commit messages explaining the improvement

## Change Selection Process

1. Review the current state of the portfolio
2. Identify ONE specific area that could be improved
3. Make the minimal change required to achieve the improvement
4. Test the change locally if possible
5. Create a descriptive commit message
6. Open a PR with clear explanation of the improvement

## Examples of Good Improvements

- "Improve color contrast in project cards from 3.2:1 to 4.8:1 for better accessibility"
- "Add preconnect hint for Google Fonts to improve page load performance"
- "Enhance focus indicator on navigation links from 1px to 2px for better keyboard navigation"
- "Update Wikipedia Article Creator description to include specific user metrics"
- "Improve responsive breakpoint for mobile menu from 768px to 840px for better tablet experience"
- "Add aria-label to social media links for screen reader users"

## Examples of Changes to Avoid

- Complete redesigns or layout changes
- Removing existing content or features
- Adding new major features without discussion
- Changing color schemes drastically
- Multiple unrelated changes in one PR
