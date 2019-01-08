### Project 3: Spatiotemporal Analysis with Spark (v 1.0)

In this assignment, we’ll analyze a dataset collected by NOAA for modeling and predicting climate phenomena: the _North American Mesoscale Forecast System (NAM)_. You’ll write Spark jobs that filter and aggregate features from the dataset. You are allowed to use any Spark-compatible programming language, and can use any libraries as long as they don’t implement/complete the assignment for you (check with the instructor first if you’re unsure).

#### Dataset Location
You can find the files in /bigdata/mmalensek/data/nam on orion01.
For more information about the dataset, see the data dictionary page.

#### Warm-up
Note: each member of your group (if applicable) should answer the following questions individually.

* **[0.5 pt]** _Unknown Feature_: Choose a feature from the data dictionary above that you have never heard of before. Inspect some of the values for the feature (such as its average, min, max, etc.) and try to guess what it measures. Was your hypothesis correct? (Note: if you are a professional meteorologist, you can skip this question ;-))

* **[0.5 pt]** _Hot hot hot_: When and where was the hottest temperature observed in the dataset? Is it an anomaly?

* **[1 pt]** _So Snowy_: Find a location that is snowy all year (there are several). Locate a nearby town/city and provide a small writeup about it. Include pictures if you’d like.

#### Analysis
* **[1 pt]** _Strangely Snowy_: Find a location that contains snow while its surroundings do not. Why does this occur? Is it a high mountain peak in a desert?

* **[1 pt]** _Lightning rod_: Where are you most likely to be struck by lightning? Use a precision of at least 4 Geohash characters and provide the top 3 locations.

* **[1 pt]** _Drying out_: Choose a region in North America (defined by one or more Geohashes) and determine when its driest month is. This should include a histogram with data from each month.

* **[2 pt]** _Travel Startup_: After graduating from USF, you found a startup that aims to provide personalized travel itineraries using big data analysis. Given your own personal preferences, build a plan for a year of travel across 5 locations. Or, in other words: pick 5 regions. What is the best time of year to visit them based on the dataset?
    * One avenue here could be determining the comfort index for a region. You could incorporate several features: not too hot, not too cold, dry, humid, windy, etc. There are several different ways of calculating this available online, and you could also analyze how well your own metrics do.
* **[1 pt]** _Escaping the fog_: After becoming rich from your startup, you are looking for the perfect location to build your Bay Area mansion with unobstructed views. Find the locations that are the least foggy and show them on a map.

* **[2 pt]** _SolarWind, Inc._: You get bored enjoying the amazing views from your mansion, so you start a new company; here, you want to help power companies plan out the locations of solar and wind farms across North America. Locate the top 3 places for solar and wind farms, as well as a combination of both (solar + wind farm). You will report a total of 9 Geohashes as well as their relevant attributes (for example, cloud cover and wind speeds).
    * If you’d like to do some data fusion to answer this question, the maps here and here might be helpful.
* **[2 pt]**  _Climate Chart_: Given a Geohash prefix, create a climate chart for the region. This includes high, low, and average temperatures, as well as monthly average rainfall (precipitation). Here’s a (poor quality) script that will generate this for you.
    * Earn up to 1 point of extra credit for enhancing/improving this chart (or porting it to a more feature-rich visualization library)
* **[2 pt]** _Influencers_: Determine how features influence each other using Pearson’s correlation coefficient (PCC). The output for this job should include (1) feature pairs sorted by absolute correlation coefficient, and (2) a correlation matrix visualization (heatmaps are a good option).
* **[2 pt]** _Prediction/Classification_: Using what you learned above as your guide, choose a feature to predict or classify via machine learning models in MLlib. You will need to explain:
    * The feature you will predict/classify
    * Features used to train the model
    * How you partitioned your data

#### Advanced Analysis
You’ve had the opportunity to analyze two datasets thus far; now it’s time to analyze a dataset of your own. Find a dataset online and use Spark (or Hadoop) to analyze it. You should:

1. **[0.5 pt]** Describe the dataset
2. **[0.5 pt]** Outline the types of insights you hope to gain from it
3. **[1 pt]** Make hypotheses about what you might find
4. **[6 pt]** Design at least 3 “questions” (along the lines of those above) and answer them. Remember that presentation matters here.

#### Wrap-Up
* **[1 pt]** _Project retrospective_
