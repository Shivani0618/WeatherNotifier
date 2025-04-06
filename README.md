# 🌤️ Weather Notifier ⛅
Get real-time weather updates straight to your desktop! This cross-platform Python app fetches current weather data and sends clean, concise notifications right to your screen.

**✨ Features**
-	🌍 Real-time weather updates for any city
-	🖥️ Cross-platform support (macOS, Windows, Linux)
-	🔔 Desktop notifications using native tools (mac: pync, others: plyer)
-	⏱️ Set your own notification interval (default: every hour)
-	⚙️ Configuration stored in a simple JSON file (auto-created if missing)
-	🔒 API key and location flexibility
-	🧠 Error handling for invalid city names or API keys

**🚀 How It Works**

This Python script uses the OpenWeatherMap API to retrieve weather data such as temperature, humidity, pressure, and a short description of the current weather. It then displays a desktop notification on your system at scheduled intervals.

**🧪 Example Notification**
<br>
<img src="https://github.com/Shivani0618/WeatherNotifier/blob/main/Notification.png?raw=true" alt="Weather Notifier Preview" width="400"/>

**🛠️ Getting Started**
1.	Install the dependencies:
```
pip install requests schedule plyer pync
```
2.	Set up your config (optional):
You can edit config.json or just run the script and it will create one for you automatically.
```
{
“api_key”: “your_openweathermap_api_key”,
“city”: “Greater Noida”,
“notification_interval_minutes”: 60,
“platform”: “mac”  // or “windows”, “linux”
}
```
3.	Run the script:
```
python weather_notifier.py
```
4.	(Optional) Set custom parameters from the command line:
```
python weather_notifier.py –city “Delhi” –interval 15
```
**📦 File Structure**
```
WeatherNotifier/
├── config.json           # Stores API key, city, and settings
├── weather_notifier.py   # Main script
├── README.md             # You’re here!
└── WeatherNotifier.ipynb # Notebook version (for exploration)
```
**🔐 Note**

-Make sure to replace the placeholder API key with your actual OpenWeatherMap API key. <br>
-You can get one free from https://openweathermap.org/api.
1. Sign Up on OpenWeatherMap 
- Go to OpenWeatherMap: [https://openweathermap.org/current](url)
- Create a free account by providing your email and password.
- Verify your email and log in.
2. Get Your API Key
- After logging in, go to your API keys section: [https://home.openweathermap.org/api_keys](url)
- You will see a default key named something like "default" under "API keys."
- If you don’t see one, click "Create Key" and give it a name (e.g., "MyWeatherApp"), and save.

💡 Tip: Set notification_interval_minutes to a small number (like 1) for quick testing.

**🧹 To Stop the Script**

-Simply press Ctrl+C in your terminal to stop the scheduler. It will log “Weather notifier stopped.”

**🧠 Why JSON?**

-The config.json file allows you to tweak the behavior of the app (like the city name and update frequency) without modifying the code.

**📋 Requirements**

•	Python 3.6+
•	Dependencies: requests, schedule, plyer, pync (for macOS only)

