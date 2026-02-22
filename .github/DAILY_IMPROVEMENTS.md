# Daily Portfolio Improvements

This repository includes an automated system for continuous portfolio improvement using GitHub Copilot agent.

## How It Works

Every day at **7:00 AM IST**, a GitHub Action automatically:

1. Creates a new issue with a specific improvement task
2. Tags the GitHub Copilot agent (`@copilot`) to work on it
3. The agent creates a focused pull request with the improvement

## Improvement Categories

The system rotates through 7 types of improvements on a weekly cycle:

1. **Monday**: Accessibility - Color contrast improvements
2. **Tuesday**: Content - Enhanced project descriptions
3. **Wednesday**: Performance - CSS optimization
4. **Thursday**: UX - Interactive feedback enhancements
5. **Friday**: SEO - Meta description improvements
6. **Saturday**: Responsive Design - Breakpoint optimization
7. **Sunday**: Accessibility - ARIA labels

## Manual Trigger

You can manually trigger an improvement task at any time:

1. Go to **Actions** tab
2. Select **Daily Portfolio Improvement** workflow
3. Click **Run workflow**
4. Select the branch and click **Run workflow**

This will immediately create a new improvement issue.

## Review Process

When the Copilot agent creates a pull request:

1. Review the changes carefully
2. Test the changes locally if needed
3. Check that the improvement aligns with the guidelines
4. Merge if satisfied, or request changes if needed

## Guidelines for Improvements

All improvements follow strict guidelines defined in `.github/agents/portfolio-improver.md`:

### ✅ Good Improvements
- Small, focused changes
- Clear, measurable impact
- Maintains existing design aesthetic
- No breaking changes
- Well-documented

### ❌ Avoid
- Large refactors
- Removing existing features
- Multiple unrelated changes
- Breaking changes
- Undocumented changes

## Monitoring

### View Improvement History
```bash
# List all daily improvement issues
gh issue list --label "daily-improvement"

# View closed improvements (completed)
gh issue list --label "daily-improvement" --state closed
```

### View Active Tasks
```bash
# See current open improvement tasks
gh issue list --label "daily-improvement" --state open
```

## Customization

### Modify Schedule

To change the schedule, edit `.github/workflows/daily-improvement.yml`:

```yaml
on:
  schedule:
    - cron: '30 1 * * *'  # Change this cron expression
```

Cron time calculator: https://crontab.guru/

### Add New Improvement Types

To add new improvement categories, edit the `improvements` array in `.github/workflows/daily-improvement.yml`.

### Modify Agent Guidelines

Update `.github/agents/portfolio-improver.md` to change how the Copilot agent should approach improvements.

## Benefits

- **Continuous improvement**: Regular, incremental enhancements
- **Automated workflow**: No manual task management
- **Consistent quality**: Follows strict guidelines
- **AI-powered**: Leverages Copilot's code understanding
- **Reviewable**: Each change is in a separate PR
- **Documented**: Clear history of all improvements

## Troubleshooting

### Workflow not running on schedule
- Ensure the workflow file is on the `main` branch
- Check repository Actions settings are enabled
- Note: Scheduled workflows may be delayed during high GitHub Actions load

### Copilot not responding
- Verify Copilot is enabled for the repository
- Check the issue has correct labels
- Ensure `@copilot` mention is present in a comment

### Multiple issues created
- The workflow checks for existing issues on the same day
- If duplicates occur, close extras manually
- Check workflow logs for debugging information

## Disabling

To temporarily disable the automated improvements:

1. Go to **Actions** tab
2. Select **Daily Portfolio Improvement** workflow
3. Click the **•••** menu → **Disable workflow**

To re-enable, follow the same steps and click **Enable workflow**.

## Example Issue

Here's what an automated improvement issue looks like:

```markdown
Title: [2024-09-30] Improve accessibility: Enhance color contrast

**Daily Improvement Task - 2024-09-30**

### Objective
Review and improve color contrast ratios across the portfolio to ensure WCAG AA compliance.

### Scope
- Check text/background contrast ratios
- Focus on interactive elements (links, buttons)
- Ensure minimum 4.5:1 contrast for normal text
- Ensure minimum 3:1 contrast for large text

### Success Criteria
- At least one color contrast issue identified and fixed
- Changes maintain the existing design aesthetic
- No breaking changes to layout or functionality

### Reference
See `.github/agents/portfolio-improver.md` for detailed guidelines.
```

## Support

For issues or questions about the daily improvement system:
1. Check the workflow logs in the Actions tab
2. Review the guidelines in `.github/agents/portfolio-improver.md`
3. Open a discussion or issue with the `question` label
