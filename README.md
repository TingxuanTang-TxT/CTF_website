# CTF Research Project Website

A modern, responsive website for the research paper: "An Empirical Study of Human–AI Collaboration and Autonomous Agents in Capture-the-Flag Competitions"

## Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Six Main Sections**:
  - Introduction
  - Agent Architecture
  - Experiment Leaderboard (interactive)
  - Experiment Results
  - Survey Materials
  - BibTeX Citation
- **Interactive Leaderboard**: Filter results by challenge category (All, Web, Crypto, Pwn, Reverse)
- **Smooth Navigation**: Sticky navigation bar with smooth scrolling
- **Anonymous Authors**: All author information is anonymized for review
- **One-Click BibTeX Copy**: Easy citation copying

## Quick Start

### Local Development

Simply open `index.html` in your web browser:

```bash
open index.html
```

Or use a local development server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (if you have http-server installed)
npx http-server
```

Then visit `http://localhost:8000` in your browser.

## Customization Guide

### Update Content

1. **Introduction Section**: Edit the content in the `#introduction` section in `index.html`
2. **Agent Architecture**: Modify the architecture components and capabilities in the `#architecture` section
3. **Results**: Update statistics in the `stat-card` divs and key findings list

### Update Leaderboard Data

Edit the `leaderboardData` array in `script.js`:

```javascript
const leaderboardData = [
    {
        rank: 1,
        name: "Your Agent Name",
        category: "all",  // or "web", "crypto", "pwn", "reverse"
        solved: 87,
        successRate: 87,
        avgTime: 23
    },
    // Add more entries...
];
```

### Update BibTeX Citation

Modify the citation in the `#bibtex-code` element in `index.html`:

```html
<pre id="bibtex-code"><code>@article{yourkey2025,
  title={Your Paper Title},
  author={Your Authors},
  journal={Your Journal},
  year={2025}
}</code></pre>
```

### Customize Colors

Edit CSS variables in `styles.css`:

```css
:root {
    --primary-color: #2563eb;     /* Main brand color */
    --secondary-color: #1e40af;   /* Secondary brand color */
    --text-color: #1f2937;        /* Main text color */
    --text-light: #6b7280;        /* Secondary text color */
}
```

### Add Survey Materials

1. Place your PDF files in a `materials/` directory
2. Update the download links in the `#survey` section:

```html
<a href="materials/survey-questions.pdf" class="download-link">Download Survey Questions (PDF)</a>
```

## Deployment

### GitHub Pages

1. Create a new repository on GitHub
2. Push your code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/your-repo.git
   git push -u origin main
   ```
3. Go to repository Settings → Pages
4. Select "main" branch as source
5. Your site will be available at `https://yourusername.github.io/your-repo/`

### Other Hosting Options

- **Netlify**: Drag and drop your folder to [Netlify Drop](https://app.netlify.com/drop)
- **Vercel**: Import your GitHub repository at [vercel.com](https://vercel.com)
- **Cloudflare Pages**: Connect your repository at [pages.cloudflare.com](https://pages.cloudflare.com)

## File Structure

```
CTF-Website/
├── index.html      # Main HTML file with all sections
├── styles.css      # All styling and responsive design
├── script.js       # Interactive features and leaderboard logic
└── README.md       # This file
```

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Tips

- The leaderboard filters work automatically - just update the data in `script.js`
- All placeholder content can be replaced with your actual research data
- The design is mobile-first and fully responsive
- Charts can be replaced with actual visualization libraries (Chart.js, D3.js, etc.)
- Survey download links currently point to `#` - update them with actual file paths

## License

This template is provided as-is for academic use.
