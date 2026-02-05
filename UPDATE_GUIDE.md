# Update Guide

This document explains how to keep the Antigravity Skills Guide up to date with the source skills repository.

## 🔄 Automatic Update Notifications

This repository has a **GitHub Action** that automatically checks for updates every Sunday at 9:00 AM UTC.

When updates are detected in [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills), a GitHub Issue will be created with:
- List of recent commits
- Changed files
- Links to review the changes

## 📋 Manual Update Process

When you receive an update notification:

### 1. Review the Changes
- Check the linked commits in the issue
- Identify which skills were added or modified

### 2. Update Relevant Chapters
For each changed skill, update the corresponding chapter:

| Skill Category | Chapter |
|---------------|---------|
| Architecture | 04-08 |
| DevOps | 15-22 |
| Security | 23-27 |
| Testing | 28-32 |
| Development | 33-40 |
| Data/AI | 41-46 |
| Productivity | 47-50 |
| Specialized | 51-55 |

### 3. Update Format
Each skill section should include:
- Skill introduction
- Contextual prompts
- Expected output
- Best practices

### 4. Commit and Push
```bash
git add -A
git commit -m "Update [chapter] with new skills from [date]"
git push
```

### 5. Close the Issue
Mark the update issue as closed.

## 🔧 Manual Trigger

You can manually trigger the update check:

1. Go to **Actions** tab in GitHub
2. Select **Check Skills Updates**
3. Click **Run workflow**

## 📁 Files

- `.github/workflows/check-skills-updates.yml` - The automation workflow
- `UPDATE_GUIDE.md` - This document
