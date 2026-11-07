# ✨ Activity Manager

### Want a beautiful GitHub contribution graph? 🌱

Tired of an empty GitHub contribution graph? Want to make your profile look a little more alive?

**Activity Manager** automatically creates commits throughout the day. No manual work, no need to remember to commit. Just a little automation. 🚀

## ⚡ How it works

- ⏰ Runs automatically **4 times a day** (every 6 hours).
- 🎲 Has a **55% chance** of making a commit on scheduled runs.
- ✋ Manual runs via `workflow_dispatch` always create a commit.
- 📝 Updates `activity.txt` with the current UTC date and time.
- 🤖 Automatically commits and pushes changes to your repository.

## 📊 Activity schedule

| Trigger | Commit probability |
|---|---:|
| Scheduled run | 55% |
| Manual run | 100% |

Average expected activity: **2.2 commits per day**.

## 🛠️ Installation

You don't need to fork or copy the workflow. Just reuse it directly in your repository.

1. Create `.github/workflows/activity-manager.yml` in your repository.
2. Add the following configuration:

```yaml
name: Activity Manager

on:
  schedule:
    - cron: '0 */6 * * *'
  workflow_dispatch:

jobs:
  activity-manager:
    uses: sidroded/.github/.github/workflows/github-activity-manager.yaml@v1
```

3. Go to **Settings → Actions → General → Workflow permissions**.
4. Enable **Read and write permissions**.

That's it! Your activity manager is ready. 🚀

## 🌿 Enjoy your green squares!

Let automation take care of your contribution graph while you focus on other things.

**Happy farming!** 💚

---

<sub>Disclaimer: This project is intended for experimentation and personal GitHub profile automation. Automated contributions do not represent actual development work.</sub>