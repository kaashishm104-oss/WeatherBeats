# Weather Beats 🎵🌤️

A responsive weather-based music recommendation web app, built from the September 2026 BCA project synopsis.

## Features
- Search for a city using Open-Meteo geocoding.
- Display live temperature, humidity, wind, cloud cover, and conditions.
- Optional browser geolocation (requires permission and HTTPS/localhost).
- Map weather to five moods: sunny/energetic, rainy/calm, cloudy/chill, stormy/atmospheric, and snowy or cold/cozy.
- Recommend curated tracks with genre preferences (pop, indie/acoustic, instrumental, Bollywood).
- Open YouTube search results for each recommended song.
- Responsive layout, accessible labels, loading states, and error handling.

## Run locally
Open `index.html` in a modern browser with an internet connection. For geolocation, use a localhost server, e.g.:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Publish with GitHub Pages
In GitHub repository **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, and save. GitHub will publish the site at `https://kaashishm104-oss.github.io/WeatherBeats/` once deployment completes.

## APIs and privacy
Weather and location lookup use the public [Open-Meteo API](https://open-meteo.com/), which does not require a key for non-commercial use subject to its terms. Music suggestions are a curated catalog; links lead to YouTube search, not in-app streaming. Location coordinates are sent to Open-Meteo only after the user grants location permission. No account or database is required, and no listening history is stored.

## Architecture
City or device location → Open-Meteo geocoding (for city searches) → current weather → rule-based mood classifier → curated music suggestions → user.

## Future enhancements
Music service integration, user accounts, listening history, personalized recommendations, forecast-based playlists, and machine-learning recommendations.

## Manual test checklist
- Search for a valid city (e.g., Moradabad).
- Search for an invalid city and check the error message.
- Change genre and verify the track list changes.
- Open a song and confirm it leads to a YouTube search.
- Try location permission granted and denied (HTTPS/localhost).
- Check the layout on mobile and desktop.
- Try offline mode and confirm the API error is handled.

Built using HTML, CSS and vanilla JavaScript. No build tools or paid credentials required.
