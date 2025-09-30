# 🚀 GitHub Profile Analyzer

A simple, beautiful web application that analyzes GitHub profiles and provides personalized suggestions for improvement.

![GitHub Profile Analyzer](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML](https://img.shields.io/badge/HTML-5-orange)
![CSS](https://img.shields.io/badge/CSS-3-blue)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)

## ✨ Features

- **📊 Comprehensive Stats**: View public repos, followers, following, and gists at a glance
- **🎯 Profile Strength Score**: Get an overall score (0-100) based on profile completeness and activity
- **🔤 Language Analysis**: See your top programming languages with color-coded visualization
- **💡 Smart Suggestions**: Receive personalized recommendations to improve your GitHub profile
- **🎨 Beautiful UI**: Modern gradient design with smooth animations
- **📱 Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **⚡ Fast**: Pure vanilla JavaScript with no dependencies

## 🖼️ Screenshots

### Profile Analysis
The analyzer displays comprehensive statistics and a profile strength score.

### Personalized Suggestions
Get actionable recommendations prioritized by importance (high/medium/low).

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (to fetch data from GitHub API)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/frankfurtru/github-profile-analyzer.git
```

2. Navigate to the project directory:
```bash
cd github-profile-analyzer
```

3. Open `index.html` in your browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

Or simply double-click the `index.html` file.

### Live Demo

You can also use GitHub Pages to host this:
1. Go to your repository settings
2. Navigate to "Pages" section
3. Select the main branch as source
4. Your site will be live at `https://frankfurtru.github.io/github-profile-analyzer/`

## 📖 Usage

1. Open the application in your browser
2. Enter a GitHub username in the search box
3. Click "Analyze Profile" button
4. View the results:
   - Profile strength score
   - Basic statistics (repos, followers, etc.)
   - Top programming languages
   - Personalized improvement suggestions

### Example Usernames to Try

- `torvalds` - Linux creator
- `gaearon` - React core team
- `tj` - Express.js creator
- `sindresorhus` - Open source contributor

## 🎯 How Profile Score is Calculated

The profile strength score (0-100) is calculated based on:

| Factor | Points | Details |
|--------|--------|---------|
| Bio | 10 | Having a bio description |
| Location | 5 | Adding your location |
| Website | 5 | Adding a blog/website |
| Social Media | 5 | Twitter/social links |
| Company | 5 | Company affiliation |
| Public Repos | up to 30 | 2 points per repo (max 15 repos) |
| Followers | up to 20 | 1 point per follower |
| Repos with Descriptions | up to 15 | Well-documented repositories |
| Starred Repos | up to 10 | Repositories with community stars |

**Maximum Score**: 100 points

## 💡 Suggestions Categories

Suggestions are prioritized into three categories:

### 🔴 High Priority
- Add a bio
- Add repository descriptions
- Create more public repositories

### 🟡 Medium Priority
- Add location
- Add website/blog
- Pin best repositories
- Engage with the community

### 🟢 Low Priority
- Diversify tech stack
- General improvements

## 🛠️ Technologies Used

- **HTML5** - Structure
- **CSS3** - Styling with gradients and animations
- **JavaScript (ES6+)** - Logic and GitHub API integration
- **GitHub REST API** - Fetching user and repository data

## 📁 Project Structure

```
github-profile-analyzer/
│
├── index.html          # Main HTML file with embedded CSS and JavaScript
└── README.md          # This file
```

## 🔧 Customization

### Changing Colors

Edit the CSS gradient in the `<style>` section:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Adding New Suggestions

Add logic in the `generateSuggestions()` function:

```javascript
if (yourCondition) {
    suggestions.push({
        icon: '🎯',
        title: 'Your Suggestion Title',
        description: 'Your suggestion description',
        priority: 'high' // or 'medium' or 'low'
    });
}
```

### Modifying Score Calculation

Edit the `calculateProfileScore()` function to adjust point values.

## 🚨 API Rate Limiting

GitHub API has rate limits:
- **Unauthenticated requests**: 60 requests per hour
- **Authenticated requests**: 5,000 requests per hour

For heavy usage, consider adding GitHub authentication:

```javascript
const response = await fetch('https://api.github.com/users/${username}', {
    headers: {
        'Authorization': 'token YOUR_GITHUB_TOKEN'
    }
});
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions

- [ ] Add contribution calendar visualization
- [ ] Add repository activity graphs
- [ ] Compare two GitHub profiles
- [ ] Export results as PDF
- [ ] Dark mode toggle
- [ ] Multi-language support
- [ ] Add more detailed language statistics
- [ ] Show recent activity timeline
- [ ] Display organization memberships
- [ ] Add contribution streak counter

## 📝 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2025 frankfurtru

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🙏 Acknowledgments

- GitHub REST API for providing profile data
- Inspired by various GitHub profile analyzers in the community
- Color palette inspired by modern gradient designs

## 📧 Contact

**Your Name** - [@frankfurtru](https://github.com/frankfurtru)

Project Link: [https://github.com/frankfurtru/github-profile-analyzer](https://github.com/frankfurtru/github-profile-analyzer)

---

⭐ If you found this useful, please consider giving it a star!

Made with ❤️ by frankfurtru
