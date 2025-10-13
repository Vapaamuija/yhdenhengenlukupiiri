# Yhdenhengen lukupiiri

_A personal book blog documenting all the books I've read, when and where, with brief reviews._

This is a Jekyll-based blog hosted on GitHub Pages, featuring book reviews and reading experiences.

## 📚 About This Blog

This blog serves as a personal reading journal where I document:
- Books I've read
- When and where I read them
- Brief reviews and ratings
- Personal thoughts and reflections

## 🛠️ Making Changes to the Blog

### Adding a New Blog Post

1. **Create a new post file** in the `_posts/` directory
2. **Follow the naming convention**: `YYYY-MM-DD-Title-of-Post.md`
3. **Include front matter** at the top of your post:

```markdown
---
title: "Your Book Title"
date: YYYY-MM-DD
---

Your review content here...
```

4. **Write your review** in Markdown format
5. **Commit and push** your changes to the `main` branch

### Editing Existing Posts

1. **Navigate to the `_posts/` directory**
2. **Open the post file** you want to edit
3. **Make your changes** using Markdown syntax
4. **Save and commit** your changes

### Updating Site Configuration

- **Edit `_config.yml`** to change site title, author, description, or theme
- **Edit `index.md`** to update the homepage content
- **Modify `Gemfile`** to update Jekyll version or add plugins

## 🚀 How to Release Updates

### Automatic Deployment

This blog uses **GitHub Actions** for automatic deployment:

1. **Push changes to `main` branch**:
   ```bash
   git add .
   git commit -m "Add new book review"
   git push origin main
   ```

2. **GitHub Actions automatically**:
   - Builds the Jekyll site
   - Deploys to GitHub Pages
   - Updates the live site

### Manual Deployment

If you need to trigger a manual deployment:

1. **Go to the Actions tab** in your GitHub repository
2. **Select "Deploy to GitHub Pages"** workflow
3. **Click "Run workflow"** button
4. **Wait for deployment** to complete

### Local Development

To preview changes locally before deploying:

#### Prerequisites: Ruby Setup on macOS

**Important**: This project requires Ruby 3.1+ and cannot use the system Ruby due to permission restrictions and missing dependencies.

1. **Install Homebrew** (if not already installed):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install Ruby via Homebrew**:
   ```bash
   brew install ruby
   ```

3. **Add Homebrew Ruby to your PATH**:
   ```bash
   echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```

4. **Verify Ruby installation**:
   ```bash
   ruby --version
   # Should show Ruby 3.4.7 or similar
   ```

#### Running the Local Development Server

1. **Install dependencies**:
   ```bash
   bundle install
   ```

2. **Start local server**:
   ```bash
   bundle exec jekyll serve
   ```

3. **View at** `http://localhost:4000`

#### Troubleshooting Ruby Issues

If you encounter permission errors or missing dependencies:

- **Don't use system Ruby**: macOS system Ruby (2.6.x) has permission restrictions
- **Use Homebrew Ruby**: Always use `brew install ruby` for local development
- **Missing gems**: The Gemfile includes `csv` and `logger` gems required for Ruby 3.4+
- **Native extensions**: Ensure Xcode command line tools are installed: `xcode-select --install`

## 📁 Project Structure

```
├── _config.yml          # Site configuration
├── _posts/              # Blog posts directory
│   └── YYYY-MM-DD-*.md  # Individual blog posts
├── index.md             # Homepage content
├── Gemfile              # Ruby dependencies
├── .github/workflows/   # GitHub Actions configuration
│   └── deploy.yml       # Deployment workflow
└── README.md            # This file
```

## 🔧 Technical Details

- **Framework**: Jekyll 4.3.4
- **Theme**: Minima 2.5.2
- **Hosting**: GitHub Pages
- **Deployment**: GitHub Actions
- **Ruby Version**: 3.4.7 (local development), 3.1.4 (GitHub Actions)

## 📝 Writing Guidelines

### Post Format
- Use clear, descriptive titles
- Include date in YYYY-MM-DD format
- Write reviews in a personal, conversational tone
- Include rating (e.g., 5/5) and location where you read the book

### Content Tips
- Keep reviews concise but meaningful
- Share personal connections to the book
- Mention what made the book special or memorable
- Include any relevant context about when/where you read it

---

## 📞 Support

If you encounter any issues:

1. **Check GitHub Actions** for deployment errors
2. **Review Jekyll documentation** for syntax issues
3. **Test locally** before pushing changes

---

&copy; 2025 Vilhelmiina m. aka vapaaamuija &bull; [MIT License](LICENSE)
