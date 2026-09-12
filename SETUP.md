# 🌍 World Time Zone Clock - Setup Guide

## Quick Start

### Option 1: Open Locally
Simply download or clone the repository and open `index.html` in your web browser.

```bash
git clone https://github.com/hariompatidar04/seattle-day-planner.git
cd seattle-day-planner
open index.html
```

### Option 2: Use GitHub Pages
Visit the live site at: **https://hariompatidar04.github.io/seattle-day-planner/**

## Features Overview

### 🕐 Clock Display
- **Digital Clock**: Shows time in HH:MM:SS format
- **Analog Clock**: Visual representation with hour, minute, and second hands
- **Time Details**: Displays current date, hour, and minute values

### 🌍 Timezone Management
- **Default Timezones**: 10 major cities loaded by default
- **Add Timezone**: Click "+ Add Timezone" to select from 33+ global timezones
- **Remove Timezone**: Click "Remove" button to delete any timezone

### 🎨 Design Features
- **Gradient UI**: Beautiful purple gradient background
- **Responsive Layout**: Works on all screen sizes
- **Smooth Animations**: Real-time hand movements and transitions
- **Hover Effects**: Interactive cards with elevation on hover

## Supported Timezones

### Americas
- Los Angeles (PST/PDT)
- Chicago (CST/CDT)
- New York (EST/EDT)
- Mexico City (CST/CDT)
- Toronto (EST/EDT)
- Vancouver (PST/PDT)
- Anchorage (AKST/AKDT)

### Europe
- London (GMT/BST)
- Paris (CET/CEST)
- Berlin (CET/CEST)
- Rome (CET/CEST)
- Istanbul (EET/EEST)
- Moscow (MSK)
- Azores (AZOT/AZOST)

### Asia
- Tokyo (JST)
- Shanghai (CST)
- Hong Kong (HKT)
- Dubai (GST)
- Bangkok (ICT)
- Kolkata (IST)
- Manila (PHT)
- Seoul (KST)
- Singapore (SGT)
- Jakarta (WIB)

### Africa
- Cairo (EET/EEST)
- Lagos (WAT)
- Johannesburg (SAST)
- Nairobi (EAT)

### Oceania
- Sydney (AEDT/AEST)
- Melbourne (AEDT/AEST)
- Auckland (NZDT/NZST)
- Fiji (FJT/FJST)

## Technical Stack

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with gradients and animations
- **JavaScript (ES6+)**: Vanilla JS with no dependencies
- **Intl API**: Browser's native internationalization for timezone handling

## Browser Compatibility

Works in all modern browsers:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## File Structure

```
seattle-day-planner/
├── index.html          # Main application file
├── README.md           # Project documentation
├── DEPLOYMENT.md       # Deployment guide
├── SETUP.md           # This file
├── .gitignore         # Git ignore rules
└── deploy.yml         # GitHub Actions workflow
```

## Customization

### Changing Default Timezones

Edit the `DEFAULT_TIMEZONES` array in `index.html`:

```javascript
const DEFAULT_TIMEZONES = [
    'America/Los_Angeles',
    'America/Chicago',
    'America/New_York',
    // Add or remove timezones here
];
```

### Modifying Colors

Update the gradient color in the CSS:

```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    /* Change these hex colors to customize */
}
```

### Adjusting Card Styling

Edit the `.clock-card` CSS class:

```css
.clock-card {
    border-radius: 20px;  /* Change border radius */
    padding: 30px;        /* Change padding */
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);  /* Change shadow */
}
```

## Performance Notes

- **Zero Dependencies**: Loads instantly with no external libraries
- **Real-time Updates**: Updates every second using `setInterval`
- **Optimized Animations**: Uses CSS transforms for smooth 60fps performance
- **Responsive**: Automatically adjusts layout based on screen size

## Accessibility

- Semantic HTML structure
- Readable font sizes and contrast ratios
- Color indicators beyond just color for timezone identification
- Keyboard navigation support

## FAQ

**Q: Can I add more than the default timezones?**
A: Yes! Click "+ Add Timezone" to add any of the 33+ supported timezones.

**Q: Does it work offline?**
A: Yes! This is a pure HTML/CSS/JS application with no server dependencies.

**Q: Can I customize the colors?**
A: Absolutely! Edit the CSS in the `<style>` section of `index.html`.

**Q: How often does the clock update?**
A: Every second automatically.

**Q: Does it sync with the system time?**
A: Yes, it uses your device's clock and converts to each timezone.

## Troubleshooting

### Clock not updating
- Refresh the page
- Ensure JavaScript is enabled in your browser
- Check browser console for errors (F12)

### Timezones showing incorrect time
- Verify your system clock is correct
- Check that you've selected the right timezone

### Page looks broken on mobile
- Ensure viewport meta tag is present (it is in index.html)
- Try clearing browser cache
- Rotate your device to landscape for better view

## Contributing

To contribute improvements:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Push to your branch
5. Open a Pull Request

## License

MIT License - Free for personal and commercial use

## Support

For issues or questions:
1. Check the [README.md](README.md)
2. Review the [DEPLOYMENT.md](DEPLOYMENT.md)
3. Check GitHub Issues
4. Create a new issue with detailed information

---

**Enjoy tracking time zones across the world! 🌍⏰**
