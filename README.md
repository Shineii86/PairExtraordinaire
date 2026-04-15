<div align="center">

[![Pair Extraordinaire Automator Banner](https://raw.githubusercontent.com/Shineii86/PairExtraordinaire/main/images/PairExtraordinaire.png)](https://github.com/Shineii86/PairExtraordinaire)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Shineii86/PairExtraordinaire/blob/main/notebooks/PairExtraordinaire.ipynb)
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

# 👥 Pair Extraordinaire Automator – Beginner's Guide

Welcome! This guide will walk you through **every single step** to earn the **Pair Extraordinaire** achievement on GitHub using our automated Google Colab notebook.

> **No coding experience required.** All you need is a browser, a GitHub account, and a friend (or a second account) to collaborate with.

---

## 📚 Table of Contents

1. [What is Pair Extraordinaire?](#1-what-is-pair-extraordinaire)
2. [What You'll Need](#2-what-youll-need)
3. [Step 1: Create a GitHub Repository](#3-step-1-create-a-github-repository)
4. [Step 2: Add Your Collaborator](#4-step-2-add-your-collaborator)
5. [Step 3: Get Your Personal Access Token](#5-step-3-get-your-personal-access-token)
6. [Step 4: Find Your Collaborator's Email](#6-step-4-find-your-collaborators-email)
7. [Step 5: Open the Colab Notebook](#7-step-5-open-the-colab-notebook)
8. [Step 6: Fill in the Configuration](#8-step-6-fill-in-the-configuration)
9. [Step 7: Run the Automation](#9-step-7-run-the-automation)
10. [Step 8: Verify the Achievement](#10-step-8-verify-the-achievement)
11. [Troubleshooting](#11-troubleshooting)
12. [FAQ](#12-faq)

---

## 1. What is Pair Extraordinaire?

**Pair Extraordinaire** is a GitHub achievement awarded when you have a **co-authored commit merged** into the default branch of any repository. The commit must include a `Co-authored-by:` line with the name and email of your collaborator.

This script automates the creation of a co-authored commit, opens a pull request, and merges it — all from your browser.

| Base | Bronze | Silver | Gold |
| :--: | :----: | :----: | :--: |
| [![Base](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-default.png)](https://github.com/Shineii86/PairExtraordinaire) | [![Bronze](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-bronze.png)](https://github.com/Shineii86/PairExtraordinaire) | [![Silver](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-silver.png)](https://github.com/Shineii86/PairExtraordinaire) | [![Gold](https://github.com/Shineii86/PairExtraordinaire/blob/main/images/pair-extraordinaire-gold.png)](https://github.com/Shineii86/PairExtraordinaire) |

---

## 2. What You'll Need

| Item | Description |
|------|-------------|
| **Your GitHub Account** | The account that will own the repository and run the automation. |
| **A Collaborator** | Another GitHub user (friend, classmate, or your second account). They must have **write access** to your repository. |
| **Personal Access Token** | A special key from your GitHub account that lets the script act on your behalf. |
| **Collaborator's Email** | The email address associated with their GitHub account. |
| **A Browser** | Google Chrome, Firefox, Edge, Safari, etc. |
| **Google Account** | To use Google Colab (free). |

> 💡 **Don't have a friend or second account?**  
> You can add **me (@Shineii86)** as a collaborator! I'm happy to help you earn the achievement.  
> Use these details in the configuration:
> - **Co-author Username:** `Shineii86`  
> - **Co-author Email:** `shineii86@users.noreply.github.com`  
> - **Co-author Name:** `Shinei Nouzen`  
> 
> Just send me a collaborator invite (Step 2) and I'll accept it as soon as I can.

---

## 3. Step 1: Create a GitHub Repository

We'll create a **new, empty repository** just for this purpose. This keeps your main projects clean.

1. Go to [GitHub](https://github.com) and sign in.
2. Click the **+** icon in the top‑right corner and select **New repository**.
3. Fill in the details:
   - **Repository name:** `pair-extraordinaire-demo` (or any name you like).
   - **Description:** (optional) e.g., "Repo for Pair Extraordinaire achievement".
   - **Visibility:** Choose **Public** (recommended) or **Private**.
   - **Initialize this repository with:** Check **Add a README file**.
4. Click **Create repository**.

> ⚠️ **Important:** Make sure you check **"Add a README file"**. This creates an initial commit and a default branch (usually `main`).

---

## 4. Step 2: Add Your Collaborator

Your collaborator needs **write access** to the repository so the co‑authored commit can be attributed to them.

1. Go to your new repository on GitHub.
2. Click the **Settings** tab (near the top).
3. In the left sidebar, click **Collaborators**.
4. Click the green **Add people** button.
5. Type your collaborator's **GitHub username** and select them from the list.
6. Click **Add [username] to this repository**.

Your collaborator will receive an email invitation. They **must accept** the invitation. (If you're using your own second account, log into that account and accept the invite.)

> ✅ After they accept, their name will appear in the Collaborators list.

---

## 5. Step 3: Get Your Personal Access Token

A **Personal Access Token (PAT)** is like a password that lets the script create and merge pull requests on your behalf.

1. Go to GitHub **Settings** (click your profile picture → **Settings**).
2. Scroll down and click **Developer settings** (bottom of left sidebar).
3. Click **Personal access tokens** → **Tokens (classic)**.
4. Click **Generate new token (classic)**.
5. Give it a name, e.g., `Pair Extraordinaire Bot`.
6. Under **Select scopes**, check the box for **`repo`** (this grants full control of your repositories).
7. Scroll down and click **Generate token**.
8. **Copy the token immediately!** It looks like `ghp_xxxxxxxxxxxxxxxxxxxx`. You won't be able to see it again.

> 🔒 **Keep this token secret.** Never share it with anyone or upload it to a public place.

---

## 6. Step 4: Find Your Collaborator's Email

The co‑author line requires the exact email address associated with your collaborator's GitHub account.

**Ask your collaborator to follow these steps:**

1. Go to GitHub **Settings** → **Emails**.
2. Look for the email marked as **Primary**.
3. They can use either:
   - Their real email address (e.g., `collaborator@gmail.com`), OR
   - The GitHub‑provided `no‑reply` email (e.g., `12345678+collaborator@users.noreply.github.com`). **This is recommended for privacy.**

Copy that email address carefully. You'll need it in the next step.

---

## 7. Step 5: Open the Colab Notebook

Click the button below to open the notebook in Google Colab:

<div align="center">

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Shineii86/PairExtraordinaire/blob/main/notebooks/PairExtraordinaire.ipynb)

</div>

Alternatively, you can manually upload the notebook if you have the `.ipynb` file.

Colab will open in your browser. If you're not already signed into Google, you'll be prompted to sign in.

---

## 8. Step 6: Fill in the Configuration

Inside the notebook, you'll see two main cells:

- **Cell 1:** 📦 Install Dependencies (just run it).
- **Cell 2:** ⚙️ Configuration & Run (this is where you enter your info).

Click on **Cell 2** and fill in the form fields:

| Field | What to Enter | Example |
|-------|---------------|---------|
| `GITHUB_USERNAME` | Your GitHub username | `"Shineii86"` |
| `GITHUB_TOKEN` | Your Personal Access Token (from Step 5) | `"ghp_abc123..."` |
| `REPO_NAME` | The repository name you created (Step 3) | `"pair-extraordinaire-demo"` |
| `BASE_BRANCH` | Default branch (usually `"main"`) | `"main"` |
| `COAUTHOR_USERNAME` | Your collaborator's GitHub username | `"collaborator"` |
| `COAUTHOR_EMAIL` | Your collaborator's email (from Step 6) | `"collaborator@users.noreply.github.com"` |
| `COAUTHOR_NAME` | Full name of your collaborator (for display) | `"Collaborator Name"` |
| `DELAY_SECONDS` | Wait time before merging (keep default) | `10` |

> 💡 **Tip:** The form fields are interactive. Just click inside the text box and type/paste your values.

---

## 9. Step 7: Run the Automation

Now it's time to run the notebook.

1. First, run **Cell 1** by clicking the **▶️ Play** button on its left side. This installs the required library.
2. Wait for it to finish (you'll see `✅ All dependencies installed and imported.`).
3. Now run **Cell 2** (the configuration cell). Click its ▶️ Play button.

The script will start working. You'll see output like this:

```
Configuration loaded for user 'Shineii86' on repo 'pair-extraordinaire-demo'
Base branch: main
Co-author: collaborator <collaborator@users.noreply.github.com>

📌 Latest main commit: a1b2c3d
✅ Created branch: pair-extraordinaire-xyz123-1234567890
📝 Updated README.md with co-authored commit
👥 Co-authored-by: Collaborator Name <collaborator@users.noreply.github.com>
🔗 Created PR: https://github.com/Shineii86/pair-extraordinaire-demo/pull/1
⏳ Waiting for GitHub to calculate mergeability...
⏸️  Waiting 10 seconds before merging...
🎉 Merged PR #1

🏁 Finished. Co-authored commit merged successfully!
👥 Congratulations! You've met the requirements for Pair Extraordinaire!
```

That's it! The script created a branch, made a co‑authored commit, opened a pull request, and merged it automatically.

---

## 10. Step 8: Verify the Achievement

1. Go to your GitHub profile: `https://github.com/YOUR_USERNAME`
2. Look at the **Achievements** section on the left sidebar (or under the "Achievements" tab).
3. You should see the **Pair Extraordinaire** badge.

> ⏳ **Note:** It can take up to **24 hours** for the achievement to appear. Usually it's within a few minutes. Try refreshing the page after 5–10 minutes.

---

## 11. Troubleshooting

| Problem | Solution |
|---------|----------|
| `github.GithubException.BadCredentialsException` | Your **Personal Access Token** is wrong or expired. Go back to Step 5 and generate a new one. Make sure you copied the entire token. |
| `Pull Request is not mergeable: 405` | Go to your repository **Settings → General → Pull Requests** and enable **"Allow auto-merge"**. Then re‑run the notebook. |
| Co-author not showing on the commit | Double‑check the email in `COAUTHOR_EMAIL`. It must exactly match the email in your collaborator's GitHub **Settings → Emails**. Also ensure they accepted the collaborator invitation. |
| The script says "PR not mergeable" and stops | Wait a minute and run Cell 2 again. Sometimes GitHub's mergeability check is slow. |
| No achievement after 24 hours | Confirm that the commit message contains `Co-authored-by: Name <email>`. You can check the commit on GitHub. Also ensure the commit was merged into the **default branch** (usually `main`). |

---

## 12. FAQ

### Q: Can I use my second GitHub account as the collaborator?
**A:** While it is technically possible, it is **against GitHub's Terms of Service** to maintain multiple free accounts for a single person. We recommend using a real friend's account or adding **@Shineii86** as described above. See [GitHub's Terms](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#account-requirements).

### Q: Do I need to keep the repository after I get the badge?
**A:** No, you can delete the repository once the achievement appears. Go to repository **Settings → Danger Zone → Delete this repository**.

### Q: Can I run this on my phone?
**A:** Yes! Google Colab works on mobile browsers. Just use the "Desktop site" option for easier navigation.

### Q: Will this cost me anything?
**A:** No. GitHub, Google Colab, and the PyGithub library are all free.

### Q: Is this script safe?
**A:** Yes. The script only uses your token to create and merge a single pull request in the repository you specify. Your token is never stored or sent anywhere else. However, always keep your token private.

---

## 🎉 Congratulations!

You've successfully automated the Pair Extraordinaire achievement! Enjoy your new badge and happy collaborating.

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
