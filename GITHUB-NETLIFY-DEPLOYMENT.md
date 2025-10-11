# GitHub & Netlify Deployment Guide

## ✅ Git Repository Created Successfully!

Your local Git repository has been initialized and committed with:
- 547 files
- 104,074 insertions
- All HTML pages, assets, and configurations

---

## 📤 Step 1: Push to GitHub

### A. Create GitHub Repository

1. **Go to GitHub**: https://github.com/new

2. **Repository Settings**:
   - **Repository name**: `netvin-naturals` (or your preferred name)
   - **Description**: Professional Accounting & Financial Services Website
   - **Visibility**: Public or Private (your choice)
   - **DO NOT** check:
     - ❌ Add a README file
     - ❌ Add .gitignore
     - ❌ Choose a license
   
3. **Click**: "Create repository"

4. **Copy the Repository URL** from the page that appears
   - Example: `https://github.com/YOUR_USERNAME/netvin-naturals.git`

### B. Connect and Push to GitHub

Run these commands in your terminal:

```bash
# Add GitHub as remote origin
git remote add origin YOUR_GITHUB_REPO_URL

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

**Replace** `YOUR_GITHUB_REPO_URL` with the actual URL you copied.

**Example**:
```bash
git remote add origin https://github.com/yourusername/netvin-naturals.git
git branch -M main
git push -u origin main
```

You may be prompted to:
- Enter GitHub username
- Enter personal access token (not password)

**Note**: If you don't have a personal access token:
1. Go to: https://github.com/settings/tokens
2. Click "Generate new token (classic)"
3. Select: `repo` scope
4. Copy the token and use it as password

---

## 🚀 Step 2: Deploy on Netlify from GitHub

### A. Connect Netlify to GitHub

1. **Go to Netlify**: https://app.netlify.com

2. **Sign In/Sign Up**:
   - Use GitHub account (recommended for easy integration)
   - Or use email

3. **Add New Site**:
   - Click **"Add new site"**
   - Select **"Import an existing project"**

4. **Connect to Git Provider**:
   - Click **"GitHub"**
   - Authorize Netlify to access your GitHub account
   - Select your repository: `netvin-naturals`

### B. Configure Build Settings

Netlify will detect it's a static site. Use these settings:

- **Build command**: (leave empty)
- **Publish directory**: `.` (root directory)
- **Branch to deploy**: `main`

### C. Deploy!

1. Click **"Deploy site"**
2. Wait 1-2 minutes for deployment
3. Your site will be live!

---

## ⚙️ Post-Deployment Configuration

### 1. Change Site Name

- Go to **Site settings** → **Site details**
- Click **"Change site name"**
- Enter: `netvin-naturals`
- Your URL becomes: `https://netvin-naturals.netlify.app`

### 2. Add Custom Domain (Optional)

1. Go to **Domain settings**
2. Click **"Add custom domain"**
3. Enter your domain (e.g., `netvin.co.ke`)
4. Follow DNS configuration instructions
5. Netlify will provide:
   - A record for apex domain
   - CNAME for www subdomain

### 3. Enable HTTPS

- Automatic with Netlify!
- Go to **Domain settings** → **HTTPS**
- Enable **"Force HTTPS"** to redirect all HTTP traffic

### 4. Configure Forms

Your contact forms will work automatically with Netlify Forms:
- View submissions in **Forms** tab
- Set up email notifications
- Enable anti-spam protection

### 5. Set Up Continuous Deployment

Already configured! Every push to GitHub main branch will:
1. Automatically trigger a new deployment
2. Build and publish changes
3. Clear cache
4. Update your live site

---

## 🔄 Making Updates

### To Update Your Website:

1. **Make Changes Locally**:
   - Edit HTML, CSS, or images
   - Test locally

2. **Commit Changes**:
   ```bash
   git add .
   git commit -m "Description of changes"
   ```

3. **Push to GitHub**:
   ```bash
   git push origin main
   ```

4. **Automatic Deployment**:
   - Netlify detects the push
   - Automatically builds and deploys
   - Changes are live in 1-2 minutes!

---

## 📊 Monitoring & Analytics

### Netlify Dashboard:

- **Deploys**: View deployment history
- **Forms**: See form submissions
- **Analytics**: Track site traffic (requires upgrade)
- **Logs**: View build and function logs

---

## 🆘 Troubleshooting

### Issue: Git push failed

**Solution**:
```bash
# Check remote
git remote -v

# If wrong, remove and re-add
git remote remove origin
git remote add origin YOUR_CORRECT_URL
git push -u origin main
```

### Issue: Authentication failed

**Solution**:
- Use personal access token instead of password
- Generate at: https://github.com/settings/tokens
- Select `repo` scope

### Issue: Netlify build failed

**Solution**:
- Check deploy logs in Netlify dashboard
- Ensure all files are committed
- Verify .gitignore didn't exclude necessary files

---

## ✅ Deployment Checklist

Before going live:

- [ ] Push to GitHub successfully
- [ ] Deploy on Netlify successfully
- [ ] Change site name
- [ ] Test all pages load
- [ ] Test forms work
- [ ] Test mobile responsiveness
- [ ] Add custom domain (if applicable)
- [ ] Enable HTTPS
- [ ] Set up form notifications
- [ ] Test contact information is correct

---

## 📞 Support Resources

### GitHub:
- Documentation: https://docs.github.com
- Support: https://support.github.com

### Netlify:
- Documentation: https://docs.netlify.com
- Community: https://answers.netlify.com
- Status: https://netlifystatus.com

---

## 🎉 You're All Set!

Your Netvin Naturals website is ready to go live. Follow the steps above to push to GitHub and deploy on Netlify.

**Contact Information on Site**:
- Email: info@netvin.co.ke
- Phone: +254 712 345 678
- Location: Kasarani, Nairobi, Kenya

Good luck with your deployment! 🚀

