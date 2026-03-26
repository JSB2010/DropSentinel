# Required Labels for Dependabot

This file documents the labels that need to be created in the GitHub repository for Dependabot to function properly.

## Labels to Create

The following labels are referenced in `.github/dependabot.yml` and need to be created in the repository:

### 1. `dependencies`
- **Name**: `dependencies`
- **Description**: Pull requests that update a dependency file
- **Color**: `#0366d6` (blue)

### 2. `automated`
- **Name**: `automated`
- **Description**: Automated pull requests from bots
- **Color**: `#7057ff` (purple)

## How to Create Labels

### Via GitHub Web Interface
1. Go to the repository on GitHub
2. Click on "Issues" tab
3. Click on "Labels"
4. Click "New label"
5. Fill in the name, description, and color
6. Click "Create label"

### Via GitHub CLI (if available)
```bash
gh label create "dependencies" --description "Pull requests that update a dependency file" --color "0366d6"
gh label create "automated" --description "Automated pull requests from bots" --color "7057ff"
```

### Via GitHub API (if available)
```bash
# Create dependencies label
curl -X POST \
  https://api.github.com/repos/JSB2010/DropSentinel/labels \
  -H "Authorization: token YOUR_TOKEN" \
  -d '{"name":"dependencies","description":"Pull requests that update a dependency file","color":"0366d6"}'

# Create automated label
curl -X POST \
  https://api.github.com/repos/JSB2010/DropSentinel/labels \
  -H "Authorization: token YOUR_TOKEN" \
  -d '{"name":"automated","description":"Automated pull requests from bots","color":"7057ff"}'
```

## Verification

After creating the labels, Dependabot will automatically apply them to dependency update pull requests.