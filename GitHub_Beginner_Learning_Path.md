# 🚀 GitHub Beginner Learning Path: Hello World Tutorial

Welcome to your **first GitHub project!**  
This guide is based on GitHub’s official [Hello World tutorial](https://docs.github.com/en/get-started/start-your-journey/hello-world), but with **added explanations, command-line equivalents, and learning notes** for complete beginners.

---

## 🧭 Overview

This tutorial will teach you:
1. How to create a repository  
2. How to create and switch branches  
3. How to make and commit changes  
4. How to open a pull request  
5. How to merge branches  

You’ll learn both **the GitHub web UI steps** and **the equivalent Git commands**.

---

## 🧱 Step 1: Create a Repository

**On GitHub UI:**
1. Go to [GitHub](https://github.com/) → Click **New repository**
2. Enter a name (e.g. `hello-world`)
3. Add a short description (optional)
4. Choose **Public**
5. Check ✅ *“Add a README file”*
6. Click **Create repository**

**Command-line equivalent:**
```bash
# Initialize a new local repository
git init hello-world
cd hello-world

# Create a README file
echo "# Hello World" > README.md

# Stage and commit the file
git add README.md
git commit -m "Initial commit"

# Link to remote repository (replace your username)
git remote add origin https://github.com/<your-username>/hello-world.git

# Push to GitHub
git branch -M main
git push -u origin main
```
---

## 🌿 Step 2: Create a Branch

Branches let you work on features separately from the main code.

**On GitHub UI:**
- Click the branch dropdown (near top-left)
- Type a new branch name (e.g. `readme-edits`)
- Click **Create branch: readme-edits from main**

**Command-line equivalent:**
```bash
# Create and switch to a new branch
git checkout -b readme-edits
```
---

## ✍️ Step 3: Make & Commit Changes

Now we’ll edit the README to add a short message.

**On GitHub UI:**
1. In your new branch, click the **README.md** file  
2. Click the ✏️ pencil icon to edit  
3. Add something like:
   ```
   Hi, I’m learning GitHub through this Hello World tutorial!
   ```
4. Scroll down → Add a commit message  
   Example: `"Add introduction message"`
5. Click **Commit changes**

**Command-line equivalent:**
```bash
# Edit the file using any text editor
echo "Hi, I’m learning GitHub through this Hello World tutorial!" >> README.md

# Stage and commit the change
git add README.md
git commit -m "Add introduction message"
```
---

## 🔁 Step 4: Open a Pull Request (PR)

Pull Requests help you propose changes to be reviewed and merged into the main branch.

**On GitHub UI:**
1. Go to the **Pull requests** tab → Click **New pull request**
2. Select `main` (base) and `readme-edits` (compare)
3. Review the diff (changes shown)
4. Click **Create pull request**
5. Add a title and optional description
6. Click **Create pull request**

**Command-line equivalent (via GitHub CLI):**
```bash
# Push your branch first
git push origin readme-edits

# Then open PR (if GitHub CLI is installed)
gh pr create --base main --head readme-edits --title "Add intro message" --body "Updated README with a short introduction."
```
---

## ✅ Step 5: Merge the Pull Request

**On GitHub UI:**
1. Review your PR  
2. Click **Merge pull request** → **Confirm merge**  
3. Optionally, delete the `readme-edits` branch after merging  

**Command-line equivalent:**
```bash
# Switch to main branch
git checkout main

# Merge the branch
git merge readme-edits

# Push the changes
git push origin main

# Delete branch locally (optional)
git branch -d readme-edits
```
---

## 🧩 What You’ve Learned

By completing this, you now understand:
- GitHub’s workflow: *Repository → Branch → Commit → Pull Request → Merge*  
- Basic Git commands (`init`, `branch`, `checkout`, `add`, `commit`, `push`, `merge`)  
- How version control helps track and review changes  

---

## 📚 Next Steps

| Topic | Description | Resource |
|--------|--------------|-----------|
| Markdown Basics | Learn how to format text beautifully in README.md | [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/) |
| Git CLI Commands | Master the command-line tools behind GitHub | [Git Cheat Sheet (PDF)](https://education.github.com/git-cheat-sheet-education.pdf) |
| GitHub Flow | Learn the professional workflow used by teams | [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/) |
| GitHub CLI | Manage GitHub from your terminal | [GitHub CLI Documentation](https://cli.github.com/manual/) |

---

## 🗓️ Learning Progress Checklist

| Step | Task | Status |
|------|-------|--------|
| 1 | Create your first repository | ☐ |
| 2 | Create and switch to a new branch | ☐ |
| 3 | Make and commit your first change | ☐ |
| 4 | Open your first pull request | ☐ |
| 5 | Merge your pull request | ☐ |
| 6 | Explore Markdown and Git basics | ☐ |

---

## 💡 Tips

- Always write **clear commit messages**  
- Use **branches** for every new feature or fix  
- Regularly **pull** updates before making new changes  
- Explore **Issues** and **Discussions** to collaborate with others  

---

⭐ **You’ve completed your first step into GitHub!**  
Keep experimenting, explore open-source projects, and start contributing!
