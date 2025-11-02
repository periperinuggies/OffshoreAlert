# OffshoreAlert

**Australian Coastal Weather Tracker**

OffshoreAlert is a comprehensive web application that tracks offshore wind conditions and weather data for 5,838+ Australian coastal locations including beaches, bays, and boat ramps.

## Features

- **Comprehensive Location Database**: 5,838 Australian coastal locations
  - 1,478 Beaches
  - 2,463 Bays
  - 1,897 Boat Ramps
- **Full State Coverage**: NSW, VIC, QLD, WA, SA, TAS, NT
- **Real-time Weather Data**: Wind speed, direction, wave height, swell data
- **Offshore Wind Tracking**: Identifies optimal offshore wind windows
- **7-Day Forecast**: Navigate forward and backward through the week
- **Sunrise/Sunset Times**: Local sunrise and sunset with collapsible night hours
- **Session Quality Rating**: 5-star rating system based on conditions
- **Mobile-Friendly**: Responsive design optimized for mobile devices
- **Google Maps Integration**: Quick access to location maps

## Data Sources

The location database was compiled from multiple Australian government and open data sources:

### Primary Data Sources:
- **OpenStreetMap** (via Overpass API): 6,050 beaches, 2,523 bays, 2,645 boat ramps
- **NSW Transport Open Data**: NSW boat ramps and coastal facilities
- **Victorian Government Data**: Beach facilities, coastal access points
- **Queensland Open Data**: Boat ramps and coastal locations
- **Western Australia Data Catalogue**: WA coastal locations
- **South Australia Open Data**: SA beaches and coastal access

### Data Processing:
- Duplicate removal and coordinate validation
- State and offshore wind direction assignment
- Unified format with consistent naming

## Usage

### Adding Locations:
1. Search for any Australian beach, bay, or boat ramp
2. Select from search results
3. Add to your tracked locations

### Viewing Conditions:
- Scroll through your tracked locations
- Navigate between days using arrow buttons
- Tap sunrise/sunset to show/hide night hours
- View 3-column summary showing previous, current, and next day conditions

### Understanding Colors:
- **Green**: Offshore winds (ideal)
- **Yellow/Orange**: Cross winds (moderate)
- **Red**: Onshore winds (poor)
- **Color intensity**: Wind strength indicator

### Quality Indicators:
- ⭐⭐⭐⭐⭐ Perfect conditions (light offshore, good swell, daylight)
- ⭐⭐⭐ Good conditions
- ⭐ Poor conditions

## Location Types

### Beaches 🏖️
Surf beaches and swimming beaches along the Australian coast

### Bays 🌊
Protected bays and coves suitable for various water activities

### Boat Ramps 🚤
Public boat launching facilities for fishing, boating, and sailing

## Technical Details

### Weather Data API:
- **Open-Meteo Marine API**: Wave height, swell, wave period
- **Open-Meteo Forecast API**: Wind speed/direction, temperature, weather codes
- **Update Frequency**: Hourly data, 7-day forecast

### Offshore Wind Logic:
Offshore wind direction is determined by coastal orientation:
- **East Coast** (NSW, QLD, VIC east): West winds offshore
- **South Coast** (SA, VIC south): North winds offshore
- **West Coast** (WA): East winds offshore
- **North Coast** (NT, QLD north): South winds offshore

### Browser Compatibility:
- Modern browsers with ES6+ support
- Local storage for saved locations
- Fetch API for data loading

## File Structure

```
OffshoreAlert/
├── index.html                           # Main application
├── australian_coastal_locations.json    # 5,838 location database (823KB)
├── surf-spots-australia.json           # Original surf spots (deprecated)
├── README.md                            # This file
└── [data files]                         # Downloaded source data
```

## Example Searches

Try searching for:
- **Famous Surf Spots**: Bondi, Bells Beach, Snapper Rocks, Margaret River
- **Bays**: Byron Bay, Port Phillip Bay, Jervis Bay
- **Boat Ramps**: Sydney Harbour ramps, Gold Coast launches
- **By State**: "NSW Beach", "QLD Bay", "VIC Boat Ramp"
- **By Name**: Cottesloe, Noosa, Torquay, Manly

## Database Statistics

| State | Locations |
|-------|-----------|
| NSW   | 1,439     |
| VIC   | 1,266     |
| WA    | 966       |
| QLD   | 734       |
| TAS   | 603       |
| SA    | 588       |
| NT    | 242       |
| **TOTAL** | **5,838** |

## Future Enhancements

Potential features for future versions:
- [ ] Tide data integration
- [ ] Water temperature
- [ ] Webcam integration (for locations with cameras)
- [ ] Favorite/bookmark locations
- [ ] Notification alerts for ideal conditions
- [ ] Export to calendar
- [ ] Share location links
- [ ] Historical weather patterns
- [ ] Moon phase data
- [ ] Extended 14-day forecast

## Credits

Built using:
- Open-Meteo API for weather data
- OpenStreetMap for location data
- Australian Government Open Data portals

## Version History

**v2.0** (2025-10-31)
- Expanded from 60 surf spots to 5,838 coastal locations
- Added beaches, bays, and boat ramps
- Renamed from "Offshore Window Tracker" to "OffshoreAlert"
- Comprehensive Australian coastal coverage

**v1.0** (2025-10-01)
- Initial release as surf spot tracker
- 60 premium surf locations

## 🔧 Local Development

To run locally:

1. Clone this repository:
```bash
git clone https://github.com/periperinuggies/OffshoreAlert.git
cd OffshoreAlert
```

2. Serve the files with a local web server:
```bash
# Using Python 3
python -m http.server 8000

# Or using Node.js
npx http-server
```

3. Open `http://localhost:8000` in your browser

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📝 Code Quality

The codebase includes:
- Comprehensive error handling for API failures and network issues
- Input validation for all user interactions
- Null safety checks throughout
- Retry functionality for failed API requests
- User-friendly error messages

---

**OffshoreAlert - Track your perfect surf conditions** 🌊🏄‍♂️
