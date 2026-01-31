# Blitz Ankara v2 - Live Presentations (Static)

A lightweight, static HTML page optimized for old TVs to display live presentations from Blitz Ankara v2.

## Features

- **Zero dependencies** - Pure HTML, CSS, and vanilla JavaScript
- **Old browser compatible** - Uses XMLHttpRequest, ES5 syntax
- **Auto-updating** - Polls API every 3 seconds for presenter updates
- **High contrast** - Black and white theme, large fonts for TV viewing
- **Minimal bandwidth** - Static files, efficient updates

## Deployment to GitHub Pages

### Option 1: Deploy to root of GitHub Pages site

1. Create a new repository or use existing GitHub Pages repo
2. Copy `index.html` to the root or a subdirectory
3. Push to GitHub
4. Enable GitHub Pages in repository settings
5. Access at `https://yourusername.github.io/` or `https://yourusername.github.io/live/`

### Option 2: Deploy as standalone project

```bash
cd live-static
git init
git add index.html README.md
git commit -m "Initial commit: Live presentation display"
git branch -M main
git remote add origin https://github.com/yourusername/blitz-live.git
git push -u origin main
```

Then enable GitHub Pages from Settings → Pages → Source: main branch

## Local Testing

Simply open `index.html` in any browser:

```bash
open index.html
```

Or use a local server:

```bash
python3 -m http.server 8000
# Visit http://localhost:8000
```

## Configuration

Edit these variables in `index.html` if needed:

```javascript
var API_BASE = 'https://blitz.devnads.com';
var EVENT_SLUG = 'blitz-ankara-v2';
var POLL_INTERVAL = 3000; // 3 seconds
```

## Browser Compatibility

Tested to work on:
- Internet Explorer 9+
- Old Smart TVs (10+ years old)
- Any browser supporting XMLHttpRequest and basic ES5

## API Endpoints Used

- `GET /api/events/blitz-ankara-v2/presenter` - Current presenter
- `GET /api/events/blitz-ankara-v2/projects` - All projects

Both endpoints are public and require no authentication.
