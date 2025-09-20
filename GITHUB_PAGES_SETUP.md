# GitHub Pages Setup

This repository is now configured with a GitHub Actions workflow that automatically builds and deploys your Jekyll site to GitHub Pages.

## How to Enable GitHub Pages

1. **Go to your repository settings**:
   - Navigate to your GitHub repository
   - Click on "Settings" tab
   - Scroll down to "Pages" in the left sidebar

2. **Configure Pages source**:
   - Under "Source", select "GitHub Actions"
   - This will allow the workflow to deploy to Pages

3. **Workflow Overview**:
   - The workflow file is located at `.github/workflows/build.yml`
   - It runs automatically on every push to the `main` branch
   - It also runs on pull requests for testing (but doesn't deploy)

## What the Workflow Does

### On Pull Requests:
- ✅ Builds the Jekyll site
- ✅ Runs HTML validation with html-proofer
- ❌ Does NOT deploy (testing only)

### On Main Branch Pushes:
- ✅ Builds the Jekyll site
- ✅ Runs HTML validation with html-proofer  
- ✅ Configures GitHub Pages
- ✅ Uploads the `_site` directory as an artifact
- ✅ Deploys to GitHub Pages using `actions/deploy-pages`

## Workflow Features

- **Ruby 3.3**: Uses the latest stable Ruby version
- **Bundler caching**: Speeds up builds by caching gems
- **HTML validation**: Ensures your site has valid HTML
- **Secure deployment**: Uses GitHub's official Pages deployment action
- **Concurrent deployment protection**: Prevents conflicts during deployment

## Your Site URL

Once enabled, your site will be available at:
- `https://<username>.github.io/<repository-name>/` (for user repositories)
- `https://<organization>.github.io/<repository-name>/` (for organization repositories)

## Troubleshooting

If deployment fails:
1. Check the "Actions" tab in your repository for error details
2. Ensure GitHub Pages is enabled with "GitHub Actions" as the source
3. Verify your `_config.yml` settings (especially `baseurl` if using a project site)

## Customization

You can modify the workflow by editing `.github/workflows/build.yml`:
- Change Ruby version in the `ruby-version` field
- Add additional build steps or tests
- Modify the HTML proofer settings
- Add environment-specific configurations