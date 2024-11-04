# 06_python-api-challenge

Background
Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

## Add a .gitignore File
- For this assignment, you will need to add a .gitignore file to your repo. Doing so will prevent 
  the api_keys.py file that contains your API key from being shared with the public. If you skip this step, 
  anyone using GitHub could copy and use your API key, and you may incur charges as a result.

- To get started, type `git status` in the command line to see a list of all the untracked files 
  that you have created so far.

- To add only the `WeatherPy.ipynb` file to GitHub, for example, type `git add WeatherPy.ipynb`. 
  Keep in mind that you would have to add each file individually when adding or updating a file. 
  A more efficient solution is to add all of the files that you don't want to track to the `.gitignore` file.

- Before adding your files to GitHub, add `api_keys.py` to the `.gitignore` file by following these steps:

    - Open your `python-api-challenge` GitHub folder in VS Code.
  
    - Open the `.gitignore` file and type the following code on the first line:
  
      ```plaintext
      # Adding api_keys.py file.
      api_keys.py
      ```

- In the command line, type `git status` and press Enter. The output should indicate that the `.gitignore` file 
  has been modified and that the `api_keys.py` file is untracked.

- Use `git add`, `git commit`, and `git push` to commit the modifications to the `.gitignore`, `WeatherPy.ipynb`, 
  and `VacationPy.ipynb` files to GitHub.

## Requirements

- The requirements for "Part 1: WeatherPy" are the following:

- Create Plots to Showcase the Relationship Between Weather Variables and Latitude
  - Use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code.
  - Create a scatter plot to showcase the relationship between Latitude vs. Temperature.
  - Create a scatter plot to showcase the relationship between Latitude vs. Humidity.
  - Create a scatter plot to showcase the relationship between Latitude vs. Cloudiness.
  - Create a scatter plot to showcase the relationship between Latitude vs. Wind Speed.

- Compute Linear Regression for Each Relationship
  - Linear regression scatter plot for Northern Hemisphere: Temperature (C) vs. Latitude.
  - Linear regression scatter plot for Southern Hemisphere: Temperature (C) vs. Latitude.
  - Linear regression scatter plot for Northern Hemisphere: Humidity (%) vs. Latitude.
  - Linear regression scatter plot for Southern Hemisphere: Humidity (%) vs. Latitude.
  - Linear regression scatter plot for Northern Hemisphere: Cloudiness (%) vs. Latitude.
  - Linear regression scatter plot for Southern Hemisphere: Cloudiness (%) vs. Latitude.
  - Linear regression scatter plot for Northern Hemisphere: Wind Speed (m/s) vs. Latitude.
  - Linear regression scatter plot for Southern Hemisphere: Wind Speed (m/s) vs. Latitude.

- The requirements for "Part 2: VacationPy" are the following:

  - Create a map that displays a point for every city in the `city_data_df` DataFrame.
  - Narrow down the `city_data_df` DataFrame to find your ideal weather condition.
  - For each city in the `hotel_df` DataFrame, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.
  - Add the hotel name and the country as additional information in the hover message for each city in the map.


-----------------------------------------------------------------

##CODING_PROCESS

Overall Approach
* Referenced activity assignments throughout the challenge.

WeatherPy
* I referenced the weatherpy API and converted from metric to imperical for the temp

Generate the Cities List by Using the `citipy` Library Section
* Added a limit to stop city count at 300. Initially used a limit of 10 to test code functionality and verify DataFrames.
* Learned that %s is a placeholder for strings within print statements.

Scatter Plot Section
* Researched how to format dates to yyyy-mm-dd for the title of a plot. 
* Discovered time.strftime("%x") formats based on US settings (mm-dd-yyyy).
* Used time.strftime("%Y-%m-%d") for yyyy-mm-dd format.

Compute Linear Regression for Each Relationship Section 
* Referenced Xpert Learning Assistant to assist with defining a function for creating linear regression plots.

VacationPy
* Created a separate cell to verify the API connection as initial code encountered issues.
* Displayed the URL used in code with variables to identify the error, which was in my inital labeling.
