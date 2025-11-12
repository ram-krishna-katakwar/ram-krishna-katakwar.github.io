# Ram Krishna Katakwar - Portfolio Website

Personal portfolio website showcasing cybersecurity expertise and professional experience.

## 🚀 Tech Stack

- **[Zola](https://www.getzola.org/)** - Fast static site generator
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework
- **GitHub Pages** - Hosting

## 📋 Prerequisites

- [Zola](https://www.getzola.org/documentation/getting-started/installation/) (v0.19.2 or higher)
- [Node.js](https://nodejs.org/) (v18 or higher)
- npm (comes with Node.js)

## 🛠️ Local Development

### 1. Install Dependencies

```bash
# Install Node dependencies
npm install
```

### 2. Build Tailwind CSS

```bash
# Build CSS for development
npm run build:css

# Or for production
npm run build
```

### 3. Run Zola Development Server

```bash
# Start the Zola dev server with live reload
zola serve
```

Visit `http://127.0.0.1:1111` to view your site locally.

## 📦 Building for Production

```bash
# Build Tailwind CSS
npm run build

# Build Zola site
zola build
```

The built site will be in the `public/` directory.

## 🚀 Deployment to GitHub Pages

### Automatic Deployment (Recommended)

The site automatically deploys to GitHub Pages when you push to the `portfolio` branch.

**Setup Steps:**

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **GitHub Actions**
4. Push your changes to the `portfolio` branch

```bash
git add .
git commit -m "Setup GitHub Pages deployment"
git push origin portfolio
```

The GitHub Actions workflow will:
- Install dependencies
- Build Tailwind CSS
- Build the Zola site
- Deploy to GitHub Pages

Your site will be live at: **https://ram-krishna-katakwar.github.io**

### Manual Deployment (Alternative)

If you prefer to build locally and push:

```bash
# Build the site
npm run build
zola build

# The public/ folder contains your site
# You can deploy this folder to any hosting service
```

## 📁 Project Structure

```
.
├── config.toml           # Zola configuration
├── content/              # Markdown content
│   └── _index.md        # Homepage content
├── templates/            # HTML templates
│   ├── index.html       # Main template
│   └── navbar.html      # Navigation template
├── static/               # Static assets (images, icons)
│   └── styles/          # Compiled CSS
├── styles/               # Source CSS files
│   └── style.css        # Tailwind source
├── tailwind.config.js   # Tailwind configuration
└── .github/
    └── workflows/
        └── deploy.yml   # GitHub Actions workflow
```

## 🎨 Customization

### Update Content

Edit `content/_index.md` to update your:
- About section
- Skills
- Projects
- Contact information

### Modify Styles

Edit `styles/style.css` and rebuild with:

```bash
npm run build:css
```

### Change Configuration

Edit `config.toml` for site-wide settings like:
- Base URL
- Language
- Syntax highlighting

## 🔧 Troubleshooting

### CSS not updating

Make sure to rebuild Tailwind CSS after making changes:

```bash
npm run build:css
```

### Zola not found

Install Zola:

```bash
# macOS
brew install zola

# Linux
snap install zola --edge

# Or download from https://github.com/getzola/zola/releases
```

### GitHub Pages not updating

1. Check the Actions tab in your GitHub repository
2. Ensure the workflow completed successfully
3. Verify Pages settings are correct (Settings → Pages)
4. Clear your browser cache

## 📝 License

ISC

## 👤 Author

**Ram Krishna Katakwar**
- LinkedIn: [ram-krishna-katakwar](https://www.linkedin.com/in/ram-krishna-katakwar)
- GitHub: [@ram-krishna-katakwar](https://github.com/ram-krishna-katakwar)
- Email: ramkkatakwar@gmail.com

