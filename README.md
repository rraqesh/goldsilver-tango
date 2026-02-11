# Gold & Silver Price Tracker 📈

Real-time tracking and comparison of Gold and Silver prices in Indian Rupees (INR) with historical analysis since June 1, 2022.

## 🌟 Features

- **Dual Price Charts**: Track Gold (INR per 10g) and Silver (INR per kg) simultaneously
- **Indexed Performance**: Compare relative performance since reference date (June 1, 2022)
- **Real-time Metrics**: Current prices, percentage changes, and Gold/Silver ratio
- **Time Range Filters**: 1M, 3M, 6M, 1Y, and All-time views
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Interactive Charts**: Hover tooltips, zoom, and pan functionality

## 🚀 Demo

View live demo: (https://rraqesh.github.io/goldsilver-tango/)

## 📊 Data Coverage

- **Reference Date**: June 1, 2022
- **Current Coverage**: Up to February 2026
- **Update Frequency**: Daily
- **Target End Date**: March 31, 2026

## 🛠️ Technology Stack

- Pure HTML5, CSS3, JavaScript (ES6+)
- [Chart.js](https://www.chartjs.org/) for data visualization
- No backend required - runs entirely in browser
- Responsive design with modern CSS

## 📁 Project Structure

```
gold-silver-tracker/
│
├── index.html          # Main application file
├── README.md           # This file
├── LICENSE             # MIT License
├── .gitignore          # Git ignore rules
│
├── data/
│   └── prices.json     # Historical price data (future enhancement)
│
└── docs/
    └── screenshots/    # App screenshots (optional)
```

## 🔧 Installation & Setup

### Option 1: Direct Use
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/gold-silver-tracker.git
   cd gold-silver-tracker
   ```

2. Open `index.html` in your web browser:
   ```bash
   # On macOS
   open index.html
   
   # On Linux
   xdg-open index.html
   
   # On Windows
   start index.html
   ```

### Option 2: Local Server (Recommended)
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js http-server
npx http-server

# Then visit: http://localhost:8000
```

### Option 3: Deploy to GitHub Pages
1. Go to repository Settings → Pages
2. Select branch: `main` and folder: `/ (root)`
3. Save and wait for deployment
4. Access at: `https://YOUR_USERNAME.github.io/gold-silver-tracker/`

## 📈 Data Integration

### Current Implementation
The app currently uses embedded historical data in `index.html`. 

### Future: API Integration
To add real-time updates, integrate with commodity price APIs:

**Option 1: Indian Market APIs**
- [Metals API](https://metals-api.com/) - Gold/Silver rates in INR
- [GoldAPI](https://www.goldapi.io/) - Real-time precious metals
- Custom scraping from Indian commodity exchanges

**Option 2: Add data update script**
```javascript
// Example: Fetch latest prices
async function fetchLatestPrices() {
  const response = await fetch('YOUR_API_ENDPOINT');
  const data = await response.json();
  // Update historicalData array
}
```

### Data Format
```json
{
  "date": "2022-06-01",
  "gold": 51000,
  "silver": 62000
}
```

## 🔄 Daily Update Workflow

### Manual Update
1. Open `index.html`
2. Locate `historicalData` array
3. Add new entry with today's prices:
   ```javascript
   { date: "2026-02-02", gold: 72500, silver: 91000 }
   ```
4. Commit and push changes

### Automated Update (Future Enhancement)
- GitHub Actions workflow to fetch daily prices
- Automatic commit to repository
- See `docs/automation.md` for implementation guide

## 🎨 Customization

### Colors
Edit CSS variables in `<style>` section:
```css
:root {
  --gold-color: #FFD700;
  --silver-color: #C0C0C0;
}
```

### Reference Date
Change in JavaScript:
```javascript
const referenceDate = '2022-06-01'; // Modify as needed
```

## 📝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Ideas for Contribution
- [ ] Add export to CSV functionality
- [ ] Implement price alerts/notifications
- [ ] Add more precious metals (Platinum, Palladium)
- [ ] Create mobile app version
- [ ] Add technical indicators (Moving averages, RSI)
- [ ] Multi-currency support

## 🐛 Known Issues

- Historical data requires manual updates (API integration planned)
- No backend persistence (all data in HTML file)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Price data sourced from Indian commodity markets
- Built with [Chart.js](https://www.chartjs.org/)
- Inspired by financial tracking tools

## 📞 Contact

**Your Name**
- GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/YOUR_PROFILE)
- Email: your.email@example.com

## 🗓️ Roadmap

- [x] Basic price tracking and visualization
- [x] Indexed performance comparison
- [x] Responsive design
- [ ] API integration for automatic updates
- [ ] Price alert system
- [ ] Historical data export
- [ ] Technical analysis indicators
- [ ] Mobile app version

## ⭐ Star History

If you find this project useful, please consider giving it a star!

---

**Built with ❤️ for precious metals investors and traders**
