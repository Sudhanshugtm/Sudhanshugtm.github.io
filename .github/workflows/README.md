# GitHub Actions Workflows

This directory contains the GitHub Actions workflows for the portfolio project.

## Workflows

### 1. Deploy to GitHub Pages (`deploy.yml`)

Automatically builds and deploys the Jekyll site to GitHub Pages whenever changes are pushed to the `main` branch.

**Triggers:**
- Push to `main` branch
- Pull requests to `main` branch

**Jobs:**
1. **Build**: Builds the Jekyll site
2. **Deploy**: Deploys the built site to GitHub Pages

### 2. Daily Portfolio Improvement (`daily-improvement.yml`)

Automatically creates daily improvement tasks assigned to GitHub Copilot agent.

**Schedule:**
- Runs every day at **7:00 AM IST** (1:30 AM UTC)
- Can also be triggered manually via workflow_dispatch

**How it works:**

1. **Issue Creation**: The workflow creates a new GitHub issue each day with:
   - A specific improvement task from a rotating list
   - Clear objectives and success criteria
   - Labels: `daily-improvement`, `copilot-agent`, `enhancement`

2. **Copilot Assignment**: The workflow automatically:
   - Tags `@copilot` in a comment on the issue
   - References the agent guidelines in `.github/agents/portfolio-improver.md`
   - Requests the agent to create a focused pull request

3. **Improvement Categories**: Tasks rotate through 7 categories:
   - Accessibility improvements (color contrast)
   - Content enhancements (project descriptions)
   - Performance optimizations (CSS cleanup)
   - UX refinements (interactive feedback)
   - SEO improvements (meta descriptions)
   - Responsive design (breakpoint optimization)
   - Accessibility enhancements (ARIA labels)

**Benefits:**
- **Continuous improvement**: Small, incremental enhancements over time
- **Automated workflow**: No manual task creation needed
- **Quality focus**: Each change is focused and reviewable
- **AI-powered**: Leverages GitHub Copilot's capabilities for code improvements

**Manual Trigger:**

You can manually trigger this workflow from the Actions tab:
1. Go to Actions → Daily Portfolio Improvement
2. Click "Run workflow"
3. Select the branch and click "Run workflow"

This is useful for testing or creating an ad-hoc improvement task.

## Configuration

### Permissions

Both workflows require specific permissions:
- `contents: read/write` - For checking out code and creating commits
- `pages: write` - For deploying to GitHub Pages
- `issues: write` - For creating improvement issues
- `pull-requests: write` - For the Copilot agent to create PRs

### Secrets

The workflows use `GITHUB_TOKEN` which is automatically provided by GitHub Actions.

## Agent Guidelines

The Copilot agent follows guidelines defined in `.github/agents/portfolio-improver.md`. These guidelines ensure:
- One focused change per improvement
- No breaking changes
- Maintained design aesthetic
- Clear documentation of changes

## Monitoring

To monitor the workflows:
1. Go to the **Actions** tab in the repository
2. Select the workflow you want to monitor
3. View run history, logs, and any errors

## Troubleshooting

### Workflow not running on schedule

- Check that the workflow file is on the `main` branch
- Verify the repository settings allow Actions to run
- Note: Scheduled workflows may be delayed during high GitHub Actions load

### Copilot agent not responding

- Ensure the issue was created with the correct labels
- Verify the `@copilot` mention is in a comment
- Check that Copilot is enabled for the repository

### Duplicate issues created

The workflow checks for existing issues created on the same day to prevent duplicates. If you see duplicates, check the workflow logs for errors in the duplicate detection logic.
