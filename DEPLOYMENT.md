# GitHub Deployment Instructions

Your Bhoota Gappa website is ready to be pushed to GitHub!

## 📦 What's Ready

✅ Git repository initialized
✅ All files committed (18 files)
✅ Branch renamed to 'main'
✅ All assets included:
   - index.html (main website)
   - 4 book cover images
   - 7 folklore creature images
   - 4 book sample files
   - README.md
   - .gitignore

## 🚀 Steps to Push to GitHub

### Option 1: Create New Repository on GitHub

1. **Go to GitHub** and create a new repository:
   - Go to https://github.com/new
   - Name it: `bhoota-gappa-website` (or your preferred name)
   - Make it **Public** (so GitHub Pages works for free)
   - **DON'T** initialize with README, .gitignore, or license
   - Click "Create repository"

2. **Copy the repository URL** (it will look like):
   ```
   https://github.com/YOUR_USERNAME/bhoota-gappa-website.git
   ```

3. **Run these commands** in your terminal (from the project folder):
   ```bash
   cd /home/claude/bhoota-gappa-website
   git remote add origin https://github.com/YOUR_USERNAME/bhoota-gappa-website.git
   git push -u origin main
   ```

### Option 2: Using GitHub CLI (if installed)

```bash
cd /home/claude/bhoota-gappa-website
gh repo create bhoota-gappa-website --public --source=. --remote=origin --push
```

### Option 3: Using SSH (if you have SSH keys set up)

```bash
cd /home/claude/bhoota-gappa-website
git remote add origin git@github.com:YOUR_USERNAME/bhoota-gappa-website.git
git push -u origin main
```

## 🌐 Enable GitHub Pages

After pushing to GitHub:

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **main** branch
4. Click **Save**
5. Your site will be live at:
   ```
   https://YOUR_USERNAME.github.io/bhoota-gappa-website/
   ```
   (It may take 1-2 minutes to deploy)

## 🔐 Authentication

If you encounter authentication issues:

### Using Personal Access Token (Recommended)

1. Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token with `repo` scope
3. Use the token as your password when pushing

### Using GitHub Desktop (Easiest for beginners)

1. Download GitHub Desktop: https://desktop.github.com/
2. Open GitHub Desktop
3. File → Add Local Repository
4. Select the `/home/claude/bhoota-gappa-website` folder
5. Click "Publish repository"

## 📝 Future Updates

To push updates later:

```bash
cd /home/claude/bhoota-gappa-website
git add .
git commit -m "Updated website content"
git push
```

## 🔧 Custom Domain (Optional)

To use your own domain (e.g., bhootagappa.com):

1. In your repository, create a file named `CNAME`
2. Add your domain name in it: `bhootagappa.com`
3. In your domain registrar, add these DNS records:
   - Type: A, Host: @, Value: 185.199.108.153
   - Type: A, Host: @, Value: 185.199.109.153
   - Type: A, Host: @, Value: 185.199.110.153
   - Type: A, Host: @, Value: 185.199.111.153
   - Type: CNAME, Host: www, Value: YOUR_USERNAME.github.io

## 📧 Need Help?

Contact: pratiksha@justutter.com

---

**Repository Location**: `/home/claude/bhoota-gappa-website`

**Next Step**: Create a repository on GitHub and run the push commands above!
