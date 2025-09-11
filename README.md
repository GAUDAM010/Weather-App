# WeatherApp 🌤️

A modern Android weather application built with Kotlin that provides real-time weather information and forecasts with beautiful, dynamic UI effects.

## Features ✨

- **Real-time Weather Data**: Get current weather conditions for any city
- **7-Day Forecast**: View detailed weather forecasts
- **City Management**: Add and manage multiple cities
- **Dynamic Backgrounds**: Weather-appropriate backgrounds that change based on conditions
- **Weather Effects**: Animated rain and snow effects
- **Day/Night Mode**: Automatic UI adjustments based on time of day
- **Blur Effects**: Modern glassmorphism UI with blur effects
- **Clean Architecture**: MVVM pattern with Repository layer

## Screenshots 📱

[Add your app screenshots here]

## Tech Stack 🛠️

### Core
- **Language**: Kotlin
- **Minimum SDK**: 26 (Android 8.0)
- **Target SDK**: 34 (Android 14)
- **Build System**: Gradle 8.5

### Architecture Components
- **MVVM Architecture Pattern**
- **ViewModel**: Lifecycle-aware components for UI data
- **LiveData**: Observable data holder
- **View Binding**: Type-safe view references

### Networking
- **Retrofit 2.9.0**: REST API client
- **OkHttp 4.12.0**: HTTP client with logging interceptor
- **Gson 2.9.1**: JSON serialization/deserialization

### UI Libraries
- **Material Design Components**: Modern Android UI components
- **ConstraintLayout**: Flexible layout system
- **WeatherView 3.0.0**: Animated weather effects (rain, snow)
- **BlurView 2.0.3**: Real-time blur effects
- **Glide 4.12.0**: Image loading and caching

## Project Structure 📁

```
WeatherApp/
├── app/
│   └── src/main/java/com/example/weatherapp/
│       ├── Activity/
│       │   ├── MainActivity.kt          # Main weather display screen
│       │   └── CityListActivity.kt      # City selection/management
│       ├── Adapter/
│       │   ├── ForecastAdapter.kt       # RecyclerView adapter for forecasts
│       │   └── CityAdapter.kt           # RecyclerView adapter for cities
│       ├── model/
│       │   ├── CurrentResponseApi.kt    # Current weather data model
│       │   ├── ForecastResponseApi.kt   # Forecast data model
│       │   └── CityResponseApi.kt       # City data model
│       ├── Repository/
│       │   ├── WeatherRepository.kt     # Weather data repository
│       │   └── CityRepository.kt        # City data repository
│       ├── Server/
│       │   ├── ApiClient.kt             # Retrofit client configuration
│       │   └── ApiServices.kt           # API service interfaces
│       └── ViewModel/
│           ├── WeatherViewModel.kt      # Weather screen ViewModel
│           └── CityViewModel.kt         # City management ViewModel
```

## Setup & Installation 🚀

### Prerequisites
- Android Studio (latest version recommended)
- JDK 17 or higher
- Android SDK

### API Key Setup
1. Get a free API key from [OpenWeatherMap](https://openweathermap.org/api)
2. Add your API key to the project (in `ApiServices.kt` or as a constant)

### Building the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/WeatherApp.git
   ```

2. Open the project in Android Studio

3. Sync project with Gradle files

4. Add your OpenWeatherMap API key

5. Run the app on an emulator or physical device

## API Endpoints 🌐

The app uses the OpenWeatherMap API with the following endpoints:
- Current weather: `/weather`
- 5-day forecast: `/forecast`
- City search: `/find`

## Key Features Implementation 💡

### Dynamic Weather Backgrounds
The app automatically changes backgrounds based on:
- Weather conditions (clear, cloudy, rainy, snowy, hazy)
- Time of day (day/night detection)

### Weather Animation Effects
- Rain effects for rainy conditions
- Snow effects for snowy weather
- Clear animation for sunny weather

### Blur View Implementation
Modern glassmorphism effect using RenderScript for real-time blur on forecast cards.

## Permissions 📋

The app requires the following permissions:
- `INTERNET`: To fetch weather data from the API
- `ACCESS_NETWORK_STATE`: To check network connectivity

## Dependencies 📦

```gradle
// Retrofit & Networking
implementation 'com.squareup.retrofit2:retrofit:2.9.0'
implementation 'com.squareup.retrofit2:converter-gson:2.9.0'
implementation 'com.squareup.okhttp3:okhttp:4.12.0'

// Architecture Components
implementation 'androidx.lifecycle:lifecycle-viewmodel-ktx:2.6.2'
implementation 'androidx.lifecycle:lifecycle-livedata-ktx:2.6.2'

// UI Libraries
implementation 'com.github.MatteoBattilana:WeatherView:3.0.0'
implementation 'com.github.Dimezis:BlurView:version-2.0.3'
implementation 'com.github.bumptech.glide:glide:4.12.0'
```

## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Future Enhancements 🔮

- [ ] Widget support for home screen
- [ ] Weather notifications
- [ ] Hourly forecast
- [ ] Weather maps integration
- [ ] Dark theme support
- [ ] Location-based weather (GPS)
- [ ] Weather history and trends
- [ ] Multiple weather providers support
- [ ] Offline mode with cached data

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments 👏

- [OpenWeatherMap](https://openweathermap.org/) for weather data API
- [WeatherView](https://github.com/MatteoBattilana/WeatherView) for weather animations
- [BlurView](https://github.com/Dimezis/BlurView) for blur effects

## Contact 📧

Your Name - [@yourusername](https://twitter.com/yourusername)

Project Link: [https://github.com/yourusername/WeatherApp](https://github.com/yourusername/WeatherApp)

---

Made with ❤️ by [Your Name]
