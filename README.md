<div align="center">

[![Pair Extraordinaire Automator Banner](https://raw.githubusercontent.com/Shineii86/PairExtraordinaire/main/images/PairExtraordinaire.png)](https://github.com/Shineii86/PairExtraordinaire)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Shineii86/PairExtraordinaire/blob/main/notebooks/PairExtraordinaire_Automator.ipynb)
[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[![GitHub Stars](https://img.shields.io/github/stars/Shineii86/PairExtraordinaire?style=for-the-badge)](https://github.com/Shineii86/PairExtraordinaire/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Shineii86/PairExtraordinaire?style=for-the-badge)](https://github.com/Shineii86/PairExtraordinaire/fork)

A **fully automated** Python script that runs in **Google Colab** to create a co-authored commit and merge the pull request — unlocking the **Pair Extraordinaire** achievement in minutes.

</div>

---

> [!WARNING]
> **This script creates a real co-authored commit and merges a pull request on your GitHub account.**
> - **Never share your Personal Access Token** – treat it like a password.
> - **Your co-author must have write access** to the repository (add them as a collaborator).
> - Use a **dedicated repository** to avoid cluttering important projects.

---

## 🎯 What is Pair Extraordinaire?

**Pair Extraordinaire** is a GitHub achievement awarded when you have a **co-authored commit merged** into the default branch of any repository. The commit must include a `Co-authored-by:` line with the name and email of your collaborator.

This script automates the creation of a co-authored commit, opens a pull request, and merges it — all from your browser.

| Base | Bronze | Silver | Gold |
| :--: | :----: | :----: | :--: |
| [![Base](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-default.png)](https://github.com/Shineii86/PairExtraordinaire) | [![Bronze](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-bronze.png)](https://github.com/Shineii86/PairExtraordinaire) | [![Silver](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-silver.png)](https://github.com/Shineii86/PairExtraordinaire) | [![Gold](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-gold.png)](https://github.com/Shineii86/PairExtraordinaire) |

---

## ✅ Why Use This Method?

| Feature                      | Benefit                                                                 |
|------------------------------|-------------------------------------------------------------------------|
| ☁️ **No PC Required**         | Runs entirely in Google Colab (cloud‑based). Works on any device.        |
| 👥 **Co‑author Support**       | Automatically formats the commit message with the `Co-authored-by:` tag. |
| 🔁 **Fully Automated**        | Creates branch, commits change, opens PR, and merges it automatically.   |
| ⚙️ **Customizable**           | Choose repository, branch, co-author info, and delay.                    |
| 📦 **Minimal Dependencies**   | Only uses the official `PyGithub` library.                               |

---

## 🧰 Prerequisites

Before you begin:

1. **A GitHub account**.
2. **A repository** where you have **write access** (you can create a new one).
3. **A GitHub Personal Access Token (Classic)** with `repo` scope.
4. **A co-author** who has a GitHub account and has **write access** to the repository (add them as a collaborator: `Settings → Collaborators → Add People`).

### 🔐 How to Get a Personal Access Token

1. Go to **Settings → Developer settings → Personal access tokens → Tokens (classic)**.
2. Click **Generate new token (classic)**.
3. Give it a name (e.g., `Pair Extraordinaire Bot`).
4. Under **Select scopes**, check **`repo`**.
5. Click **Generate token** and **copy the token immediately**.

---

## 📥 How to Deploy

### 1️⃣ One‑Click Colab

<a href="https://colab.research.google.com/github/Shineii86/PairExtraordinaire/blob/main/notebooks/PairExtraordinaire_Automator.ipynb">
  <img src="https://user-images.githubusercontent.com/125879861/255389999-a0d261cf-893a-46a7-9a3d-2bb52811b997.png" alt="Open In Colab" width="200px">
</a>

### 2️⃣ Fill in the Configuration Form

Inside the Colab notebook, you'll find a configuration cell with form fields:

| Variable            | Description                                      | Example Value               |
|---------------------|--------------------------------------------------|-----------------------------|
| `GITHUB_USERNAME`   | Your GitHub handle                               | `"Shineii86"`               |
| `GITHUB_TOKEN`      | Personal Access Token (keep secret!)             | `"ghp_abc123..."`           |
| `REPO_NAME`         | Target repository (must exist under your account)| `"PairExtraordinaire"`      |
| `BASE_BRANCH`       | Branch to target (default: `main`)               | `"main"`                    |
| `COAUTHOR_USERNAME` | Co-author's GitHub username                      | `"collaborator"`            |
| `COAUTHOR_EMAIL`    | Co-author's email (associated with GitHub)       | `"collaborator@example.com"`|
| `COAUTHOR_NAME`     | Co-author's full name (for commit message)       | `"Collaborator Name"`       |
| `DELAY_SECONDS`     | Pause before merging (default: 10)               | `10`                        |

### 3️⃣ Run the Notebook

Click **Runtime → Run all** (or press `Ctrl+F9`). The notebook will:
- Install `PyGithub`
- Create a co-authored commit
- Open a pull request
- Merge it automatically

You'll see output like:

```
📌 Latest main commit: a1b2c3d
✅ Created branch: pair-extraordinaire-xyz123-1234567890
📝 Updated README.md with co-authored commit
👥 Co-authored-by: Collaborator Name <collaborator@example.com>
🔗 Created PR: https://github.com/Shineii86/PairExtraordinaire/pull/1
⏳ Waiting for GitHub to calculate mergeability...
⏸️ Waiting 10 seconds before merging...
🎉 Merged PR #1
👥 Congratulations! You've met the requirements for Pair Extraordinaire!
```

### 4️⃣ Verify the Achievement

1. Go to your GitHub profile (`https://github.com/YOUR_USERNAME`).
2. Look for the **Pair Extraordinaire** badge in the achievements section.
   *Note: It may take a few minutes for GitHub to update.*

---

## ⚙️ Customization

All parameters are adjustable directly in the Colab form:

| Parameter        | Default  | Description                                                                 |
|------------------|----------|-----------------------------------------------------------------------------|
| `COAUTHOR_USERNAME` | `"collaborator"` | GitHub username of the co-author. |
| `COAUTHOR_EMAIL` | `"collaborator@example.com"` | Email associated with the co-author's GitHub account. |
| `COAUTHOR_NAME`  | `"Collaborator Name"` | Full name displayed in the commit message. |
| `BASE_BRANCH`    | `"main"` | Target branch for the PR (e.g., `master`, `develop`). |
| `DELAY_SECONDS`  | `10`     | Wait time before merging (seconds). |

---

## 🔬 How It Works

1. **Fetches the latest commit SHA** from the base branch.
2. **Creates a new branch**.
3. **Creates/updates a file** (e.g., `README.md`) with a commit message that includes the `Co-authored-by:` line.
4. **Opens a pull request** from the new branch to the base branch.
5. **Waits for GitHub's mergeability check**.
6. **Merges the pull request**.

The commit message follows GitHub's required format:
```
feat: add pair extraordinaire demo

Co-authored-by: Collaborator Name <collaborator@example.com>
```

---

## 🆘 Troubleshooting

| Issue                                             | Solution                                                                                     |
|---------------------------------------------------|----------------------------------------------------------------------------------------------|
| `github.GithubException.BadCredentialsException`  | Your Personal Access Token is incorrect or expired. Generate a new one.                       |
| `Pull Request is not mergeable: 405`              | Enable **Allow auto‑merge** in repo Settings → General → Pull Requests.                       |
| Co-author not showing on commit                   | Ensure the email matches the co-author's GitHub account email.                                |
| No achievement after successful run               | Wait a few minutes and refresh your profile. Achievement updates are not instant.             |

---

## 📄 License & Disclaimer

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

> [!WARNING]
> This script is intended for educational purposes and to help users unlock a harmless GitHub achievement. Please use responsibly and do not abuse automation to spam repositories. The author is not responsible for any consequences arising from misuse of this tool.

---

## 💕 Loved My Work?

🚨 [Follow me on GitHub](https://github.com/Shineii86)

⭐ [Give a star to this project](https://github.com/Shineii86/PairExtraordinaire)

<div align="center">

<a href="https://github.com/Shineii86/PairExtraordinaire">
<img src="https://github.com/Shineii86/AniPay/blob/main/Source/Banner6.png" alt="Banner">
</a>
  
  *For inquiries or collaborations*
     
[![Telegram Badge](https://img.shields.io/badge/-Telegram-2CA5E0?style=flat&logo=Telegram&logoColor=white)](https://telegram.me/Shineii86 "Contact on Telegram")
[![Instagram Badge](https://img.shields.io/badge/-Instagram-C13584?style=flat&logo=Instagram&logoColor=white)](https://instagram.com/ikx7.a "Follow on Instagram")
[![Pinterest Badge](https://img.shields.io/badge/-Pinterest-E60023?style=flat&logo=Pinterest&logoColor=white)](https://pinterest.com/ikx7a "Follow on Pinterest")
[![Gmail Badge](https://img.shields.io/badge/-Gmail-D14836?style=flat&logo=Gmail&logoColor=white)](mailto:ikx7a@hotmail.com "Send an Email")

  <sup><b>Copyright © 2026 <a href="https://telegram.me/Shineii86">Shinei Nouzen</a> All Rights Reserved</b></sup>

![Last Commit](https://img.shields.io/github/last-commit/Shineii86/PairExtraordinaire?style=for-the-badge)

</div>
