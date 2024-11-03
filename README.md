# Weather-Based Movie Recommendation App

This mini-app provides personalized movie recommendations based on the current weather forecast. It combines real-time weather data and popular movies to suggest a curated list of films that match the mood of the day. The app demonstrates integration with third-party APIs and uses a large language model (LLM) to generate context-aware recommendations.

## Features

- **Fetches Popular Movies**: Retrieves a list of fan-favorite movies from IMDb.
- **Gets Real-Time Weather**: Fetches current weather conditions from AccuWeather.
- **Generates Recommendations**: Uses a large language model to recommend movies based on weather conditions, with creative descriptions tailored to the weather.

## Getting Started

### Prerequisites

- Python 3.x
- Required Python packages:
  - `requests` for API calls.
  - `groq` for interacting with the language model API.
- API keys for IMDb, AccuWeather, and the Groq LLM.

### Installation

1. Clone this repository or download the files.
   ```bash
   git clone https://github.com/your-username/weather-movie-recommendation.git
   cd weather-movie-recommendation
   ```
2. Install required packages.
   ```bash
   pip install requests groq
   ```

### Setting Up API Keys

Replace the placeholders in the code with your API keys:
- `IMDB_API_KEY`: Your IMDb API key.
- `ACCUWEATHER_API_KEY`: Your AccuWeather API key.
- `GROQ_API_KEY`: Your Groq API key.

Example:
```python
headers = {
    "x-rapidapi-key": "YOUR_IMDB_API_KEY",
    "x-rapidapi-host": "imdb188.p.rapidapi.com"
}

url = f"http://dataservice.accuweather.com/forecasts/v1/daily/1day/{location_id}?apikey=YOUR_ACCUWEATHER_API_KEY"
client = Groq(api_key="YOUR_GROQ_API_KEY")
```

### Usage

To run the app, execute the main function:
```python
python main.py
```

The app will:
1. Fetch a list of IMDb fan-favorite movies.
2. Fetch the weather forecast for a specified location.
3. Generate and print a movie recommendation list based on the weather.

### Example Output

```
Generating movie recommendations based on the weather...

Based on the rainy weather forecast, I'd recommend a few relaxing movies from your list. Here are some suggestions:

1. **Shawshank Redemption** (Rating: 9.3) - A highly-rated film about hope, redemption, and friendship, perfect for a cozy evening on a rainy day.
2. **The Lord of the Rings: The Fellowship of the Ring** (Rating: 8.9) - A classic fantasy film that will transport you to a different world, providing an escape from the gloomy weather outside.
3. **Forrest Gump** (Rating: 8.8) - A heartwarming, feel-good movie with a simple yet inspiring story that's easy to get lost in on a rainy day.
```

## Project Structure

- `main.py`: The main script containing functions to fetch movie data, get weather information, and generate recommendations.
- `get_imdb_fan_favorites()`: Fetches fan-favorite movies from IMDb.
- `get_weather_forecast()`: Retrieves the weather forecast for a specific location.
- `generate_movie_recommendation()`: Uses the Groq API to generate movie recommendations based on the weather.

## API References

- **IMDb API**: Used to fetch popular movie data.
- **AccuWeather API**: Provides real-time weather forecasts.
- **Groq LLM API**: Processes the weather data and generates a movie recommendation list.

## Notes

- API calls are rate-limited; ensure you do not exceed the free API limits.
- Make sure to handle any errors related to API calls for a smooth user experience.

## Future Improvements

- Enhance the UI within the notebook for a more interactive experience.
- Integrate support for multiple locations or more complex weather-based suggestions.
- Allow user customization of the movie recommendation criteria.

## License

This project is open-source and free to use under the MIT License.

## Contributing

Feel free to fork this project, submit issues, or contribute by opening a pull request.

## Contact

For any questions, feel free to reach out or open an issue in the repository.
