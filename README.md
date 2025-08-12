# Geotab Holiday Tool

A free, public web-based tool for managing work holidays in Geotab databases. Connect to your MyGeotab instance to view, add, and remove work holidays with an intuitive interface.

## ⚠️ Important Disclaimer

This is an **unofficial, community-created tool** that uses Geotab's public API. It is **not affiliated with or endorsed by Geotab Inc.**

- **Use at your own risk** - This tool directly modifies your Geotab database
- **No warranty or support** - The tool is provided "as-is" 
- **Breaking changes** - Geotab may update their API which could break this tool
- **Test first** - Always test in a non-production environment before using in production

## 🎯 What This Tool Does

The Geotab Holiday Tool provides a simple web interface to:

- **Connect** to your MyGeotab database using your credentials
- **View** existing work holidays in a sortable table
- **Add** federal holidays (US) for multiple years at once
- **Add** other common holidays (Halloween, Black Friday, etc.)
- **Create** custom holidays with fixed or variable dates
- **Remove** individual holidays from your database
- **Bulk process** holidays with progress tracking and rate limiting

## ✨ Key Features

- **No Installation Required** - Runs entirely in your web browser
- **Secure** - Credentials are only used for direct API connection (not stored)
- **Smart Duplicate Detection** - Prevents adding holidays that already exist
- **Rate Limiting** - Automatically manages API call limits
- **Progress Tracking** - Real-time feedback during bulk operations
- **Responsive Design** - Works on desktop and mobile devices
- **Federal Holiday Support** - Pre-configured US federal holidays with correct calculation logic
- **Custom Holiday Builder** - Create holidays with variable dates (e.g., "3rd Monday in February")

## 🚀 Quick Start

### Option 1: Use Online (Recommended)
Visit the live tool: **https://logvin.github.io/geotab-holiday-tool/**

### Option 2: Run Locally
1. Download or clone this repository
2. Open `index.html` in any modern web browser
3. No setup required!

## 📋 How to Use

### 1. Connect to Your Database
- Enter your MyGeotab database name (e.g., "my_company")
- Enter your username and password
- Click "Connect"
<img width="654" height="621" alt="image" src="https://github.com/user-attachments/assets/c8115b2c-8342-4a20-89e9-f6fa75846150" />


### 2. View Existing Holidays
- Click "Load Holidays" to see current work holidays
- Sort by name, date, or year by clicking column headers
- Remove individual holidays using the "Remove" button
<img width="654" height="784" alt="image" src="https://github.com/user-attachments/assets/ccd12e50-688a-4155-a11a-300861417641" />

### 3. Add New Holidays
- Select from pre-configured federal holidays
- Choose other common holidays
- Create custom holidays with the "Add New" button
- Set the year range (start and end year)
- Click "Add Selected Holidays" to process
<img width="654" height="784" alt="image" src="https://github.com/user-attachments/assets/45900778-9fe6-4755-a329-2fb5bbfa0368" />

### 4. Monitor Progress
- Watch real-time progress in the output window
- See success/skip/failure counts in the summary
- API rate limiting is automatically handled
<img width="654" height="784" alt="image" src="https://github.com/user-attachments/assets/77809846-61fe-4fcc-8568-464c0c5068bf" />

## 🏛️ Supported Federal Holidays

- New Year's Day (January 1)
- Martin Luther King Jr. Day (3rd Monday in January)
- Presidents' Day (3rd Monday in February) 
- Memorial Day (Last Monday in May)
- Juneteenth (June 19)
- Independence Day (July 4)
- Labor Day (1st Monday in September)
- Columbus Day (2nd Monday in October)
- Veterans Day (November 11)
- Thanksgiving Day (4th Thursday in November)
- Christmas Day (December 25)

## 🎃 Other Holidays

- Halloween (October 31)
- Black Friday (Day after Thanksgiving)
- Christmas Eve (December 24)
- New Year's Eve (December 31)
- Customer Holidays by fixed date or variable (like Thanksgiving)
<img width="654" height="399" alt="image" src="https://github.com/user-attachments/assets/af2b620a-b408-4dd2-9420-41e77b30e38e" />

## 🛠️ Technical Details

- **Built with**: Pure HTML, CSS, and JavaScript (ES6+)
- **API Integration**: Uses [mg-api-js](https://github.com/Geotab/mg-api-js) wrapper
- **Geotab SDK**: Based on [official MyGeotab API documentation](https://developers.geotab.com/myGeotab/introduction/)
- **No Dependencies**: Runs entirely in the browser with CDN resources
- **Rate Limiting**: Respects Geotab's API rate limits (90 calls per minute)

## 📁 Project Structure

```
geotab-holiday-tool/
├── index.html          # Complete single-file application
├── README.md           # This documentation
└── LICENSE             # MIT License
```

## ⚡ Features in Detail

### Smart Date Calculation
- Federal holidays are calculated correctly for any year
- Variable dates (like "3rd Monday") are computed automatically
- Custom holidays support both fixed dates and variable patterns

### Duplicate Prevention
- Checks existing holidays before adding new ones
- Flexible date matching handles timezone differences
- Prevents accidental duplicates across bulk operations

### Rate Limiting & Progress
- Automatic API rate limit detection and waiting
- Real-time progress updates with timestamps
- Detailed success/failure reporting

### Data Safety
- Verification step confirms holidays were added successfully
- Clear error reporting for any failures
- Non-destructive operations (view before modify)

## 🔒 Security & Privacy

- **No data storage** - All processing happens in your browser
- **Direct API connection** - Your credentials go directly to Geotab
- **Open source** - Full code is available for review
- **No external dependencies** - Only uses Geotab's official API wrapper

## 🐛 Known Limitations

- Only supports US federal holidays (contributions welcome for other countries)
- Requires manual credential entry each session
- Limited to work holidays (doesn't handle other Geotab calendar types)

## 🤝 Contributing

This is a community project! Contributions are welcome:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-country-holidays`)
3. Commit your changes (`git commit -m 'Add Canadian holidays'`)
4. Push to the branch (`git push origin feature/new-country-holidays`)
5. Open a Pull Request

### Ideas for Contributions
- Add holidays for other countries
- Improve the UI/UX
- Add more custom holiday patterns
- Enhance error handling
- Add data export features

## 📋 Requirements

- Modern web browser (Chrome 70+, Firefox 65+, Safari 12+, Edge 79+)
- Internet connection
- Valid MyGeotab account with appropriate permissions
- Work holiday management permissions in your Geotab database

## ❓ Troubleshooting

**Connection Issues:**
- Verify your database name, username, and password
- Ensure you have API access permissions
- Check that your account has work holiday management rights

**Rate Limiting:**
- The tool automatically handles rate limits
- Wait for the countdown timer if you see rate limit warnings

**Duplicate Holidays:**
- The tool checks for existing holidays before adding
- "Skipped" results indicate the holiday already exists

## 📄 License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](https://github.com/Logvin/geotab-holiday-tool?tab=GPL-3.0-1-ov-file) file for details.

## 🙏 Acknowledgments

- [Geotab Inc.](https://www.geotab.com/) for their comprehensive API
- [mg-api-js](https://github.com/Geotab/mg-api-js) for the JavaScript wrapper
- The Geotab developer community

## 📞 Support

For questions, issues, or feature requests:

- Create an [Issue](https://github.com/yourusername/geotab-holiday-tool/issues) on GitHub
- This is a community project with no official support
- Check existing issues before creating new ones

---

**⚠️ Remember: This is an unofficial tool. Always test in a safe environment first!**

**🔗 Useful Links:**
- [Geotab Developer Portal](https://developers.geotab.com/)
- [MyGeotab API Documentation](https://developers.geotab.com/myGeotab/introduction/)
- [mg-api-js GitHub Repository](https://github.com/Geotab/mg-api-js)
