# Smart-Workout-Tracker
## Smart-Workout-Tracker

### Overview
This Python script tracks your workout routine and calculates calories burned using the Nutritionix API. It then stores workout data in a Google Sheet via the Sheety API.

### Prerequisites
* A Nutritionix API account with APP ID and API Key.
* A Sheety account with a created Google Sheet and API token.
* Python environment with the following libraries installed:
  * requests
  * datetime
  * os
  * dotenv

### Setup
1. **Create a `.env` file** in the same directory as your script and add the following environment variables:
   ```
   ENV_NIX_APP_ID=YOUR_NUTRITIONIX_APP_ID
   ENV_NIX_API_KEY=YOUR_NUTRITIONIX_API_KEY
   ENV_SHEETY_TOKEN=YOUR_SHEETY_TOKEN
   sheet_endpoint=YOUR_SHEETY_ENDPOINT
   ```
2. **Replace the placeholder values** with your actual API keys and Sheety endpoint.
3. **Update your personal data** (GENDER, WEIGHT_KG, HEIGHT_CM, AGE) at the beginning of the script.

### Usage
1. Run the script.
2. Enter the workout details when prompted.
3. The script will fetch workout data from Nutritionix, calculate calories, and store the data in your Google Sheet.

### How it works
1. **User input:** The script prompts the user to enter workout details.
2. **Nutritionix API call:** The script sends a POST request to the Nutritionix API with workout details and user information.
3. **Data parsing:** The script extracts relevant data (exercise name, duration, calories) from the Nutritionix API response.
4. **Sheety API call:** The script sends a POST request to the Sheety API with workout data, including date, time, and calculated calories.

### Additional Notes
* Ensure accurate personal data for precise calorie calculations.
* Customize the Google Sheet structure and headers as needed.
* Consider error handling and logging for improved robustness.
* Explore additional features like exercise history, goal setting, and progress tracking.

**Enjoy tracking your workouts and achieving your fitness goals!**
 
### Contributing
Feel free to contribute to this project by:
* Reporting issues
* Suggesting improvements
* Adding new features


**Disclaimer:** This script is provided as-is without any warranties. Use it at your own risk.
