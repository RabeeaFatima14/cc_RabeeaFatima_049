# Cloud Computing - Assignment 1

**Submitted by:**  
**Name:** Rabeea Fatima  
**Registration No:** 2023-BSE-049  
**Section:** B  
**Subject:** Cloud Computing  

---

## Task 1: Run Gitea in Codespace and Create an Initial Repo

1. **Set up Gitea**
   - Run a Gitea server inside your Codespace.
   - Use **HTTPS** for communication (SSH is not supported in Codespace).

2. **Create a Repository**
   - Create a new repository on your Gitea server.
   - Add a `README.md` file listing each student’s name and roll number.

3. **Add Remote Repo**
   - Add your Gitea repository as a remote:
     ```bash
     git remote add gitea <repository-url>
     ```
   - Push your initial commit containing the `README.md` to Gitea.

---

## Task 2: Mirror README.md from Gitea to GitHub

1. **Continue Working with Your Existing Repository**
   - Use the same repository created and pushed to your Gitea server in Task 1.

2. **Create GitHub Repository**
   - Create a new GitHub repository named **assignment-1**.

3. **Add GitHub as a Second Remote**
   ```bash
   git remote add github <github-repository-url>
   ```

4. **Push README.md File to GitHub**
   - Push the contents (including the `README.md`) from your local repository to GitHub.

5. **Verify Remotes**
   ```bash
   git remote -v
   ```
   - Ensure both remotes (`gitea` and `github`) are listed.

---

## Task 3: Use Git LFS for Large Files

1. **Install Git LFS**
   - Set up Git LFS in your local repository.

2. **Add Large Files**
   - Add three files larger than **100 MB** each to your repository.
   - Track them using Git LFS:
     ```bash
     git lfs track "*.ext"
     ```
     Replace `.ext` with the appropriate file extension.

3. **Reference in Assignment Repo**
   - Commit and push these large files to your GitHub **assignment-1** repository.
   - Ensure the files are referenced correctly in your repository history.

---

## Task 4: Create a Portfolio/CV with GitHub Pages

1. **Create a New Repository for GitHub Pages**
   - Create a new repository named `<username>.github.io`
     (e.g., `johnsmith.github.io`).

2. **Design Your Portfolio/CV**
   - Create your portfolio or CV using **HTML/CSS** (or a static site generator).

3. **Publish with GitHub Pages**
   - Push your portfolio/CV files to the `.github.io` repository.
   - Enable GitHub Pages in your repository settings (if not automatically enabled).
   - Publish your site and share the link.

---

### 🌐 Link to Portfolio Website

[https://rabeeafatima14.github.io/](https://rabeeafatima14.github.io/)
