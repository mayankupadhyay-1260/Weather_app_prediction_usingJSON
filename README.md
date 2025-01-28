# 🌤️ Weather App Project

Welcome to the Weather App Project! This application allows users to check the current weather conditions of any city using the OpenWeatherMap API. The app is built using Python and Tkinter for the graphical user interface (GUI).

## 📋 Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [Contributing](#contributing)
- [License](#license)

## 🌟 Features
- Search for the weather by city name.
- Displays temperature, pressure, humidity, and wind speed.
- User-friendly GUI built with Tkinter.

## 🛠️ Technologies Used
- **Python**: Programming language used for the application.
- **Tkinter**: Standard GUI toolkit for Python.
- **Requests**: Library for making HTTP requests to the OpenWeatherMap API.
- **OpenWeatherMap API**: Provides weather data.

## 📥 Installation
To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/weather_app_project.git
   cd weather_app_project
   ```

2. **Install required packages**:
   Make sure you have Python installed. Then, install the required libraries:
   ```bash
   pip install requests
   ```

3. **Run the application**:
   Execute the following command to start the app:
   ```bash
   python weather_app_project.py
   ```

## 🚀 Usage
1. Enter the name of the city in the input field.
2. Click the "Submit" button to fetch the weather data.
3. The app will display the weather information, including:
   - City name
   - Country
   - Weather condition
   - Temperature (in Kelvin)
   - Pressure (in mb)
   - Humidity (%)
   - Wind speed (m/s)

## 📝 Code Overview
The main components of the code are as follows:

- **Imports**: The necessary libraries are imported at the beginning.
- **Tkinter GUI Setup**: The main window and widgets (labels, entry, button) are created.
- **Data Function**: The `data()` function fetches weather data from the OpenWeatherMap API based on the city name entered by the user.
- **Error Handling**: The app checks for a 404 error if the city is not found and displays an appropriate message.

### Key Code Snippet
```python
def data():
    import requests
    city_name = e.get()
    API_key = "your_api_key_here"
    ws = requests.get(f"https://api.openweathermap.org/data/2.5/weather?q={city_name}&units=imperial&appid={API_key}")
    
    if ws.json()['cod'] == '404':
        n0.config(text=f"ERROR 404\nCity name not found")
    else:
        # Display weather information
        ...
```

## 🤝 Contributing
Contributions are welcome! If you have suggestions for improvements or new features, please fork the repository and submit a pull request.

## 📄 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Thank you for checking out the Weather App Project! If you have any questions or feedback, feel free to reach out. Happy coding! 
