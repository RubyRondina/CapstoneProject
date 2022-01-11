# Capstone Project: 
## Google Analytics, Google Merchandise E-commerce Store 

<br>

<p align="left"><img width="400" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/GA360.png"></p>

In this bootcamp capstone project, we were called to use our analytical and modelling skills in Python, as well as our graphic design and presentation skills in Tableau, in order to tell a deep story about a dataset of our choice.  

<br>

## Dataset

<p align="left"><img width="800" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/GoogleMerchWebsite.png"></p>
                                                                                                                                                      
I chose the Google Analytics sample dataset from BigQuery Public so that I could also flex my SQL muscles.
                                                                                                                                                      This dataset contains Google Analytics 360 data from the Google Merchandise e-commerce Store.
                                                                                                                                                      The raw data spans information from Aug. 2016 to July 2017, containing 16 columns with several nested arrays within nested arrays.  The fields contain  dates, visitor IDs, visit numbers, visit start times, hits, page views, bounces, time on site, transactions and product data, traffic source details, device information, geoNetworks and a supposed "social engagement type" for each user.

My main focus on this project is the REVENUE.

<br>

## The Question:  
What specific variables in this dataset have a strong determining factor on the Total Revenue?
And what recommendations can I propose to increase sales thereafter?

<br>

## Challenges

My intent was to study the full year's worth of data.  The process of pulling queries using SQL directly on BigQuery in order to examine the full year's performance was quite painless and pretty straightforward.  However, since the project requirement called for exploratory data analysis using Python, I had to limit the study to only two month's worth of data.  This is due to the fact that Python is not as well optimized as SQL to process big data.  It took my machine almost one hour to import the full year's worth of data into Python.  We had less than a week to complete this project, so in order to save time and computer processing power, I only dealt with data from December 1, 2016 to January 31, 2017.

Another issue was that Google made some fields in this dataset obfuscated or removed for privacy reasons.  This is specifically data on marketing related details such as ads, promotions, campaigns, keyword searches and certain traffic sources.  I also discovered that the field for "social engagement type" was filled with "not socially engaged" users only. 

Thankfully, there was a plethora of information relating to products, prices and geographic locations where I could draw my focus.

Last but not least, it is important to note that web traffic is only tracked when a user's cookies are on.  Visitors who did not enable their cookies when visiting the website are not part of this dataset.  As useful and as powerful of a tool that it is, Google Analytics simply cannot obtain the full picture since it is unable to track hidden visitors and their behaviours.

It is not perfect but we will make best efforts with the best tools that we have since the alternate would just be irresponsible.

<br>

## The Process and Initial Analysis

The first step was to query a table from BigQuery, limited to data for December and January only, as well as information on the products, prices, transactions, revenue and geo location by continent.  I then imported that table to Python Jupyter notebooks to start exploring the data.

**See full Jupyter Notebook [here](https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/Capstone_Final.ipynb)**

**Python libraries used**: *NumPy, Pandas, Statsmodels*

My initial analysis revealed the following:

<h3 align="center">December yielded more revenue than January</h3>

<p align="center"><img width="900" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/DecVSJan.png"></p>

<h3 align="center">The following descriptive stats on product prices</h3>

<p align="center"><img width="900" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/DescriptStatsPrice.png"></p>

<br>

<h3 align="center">The highest number of units sold was the **maze pen** at 500 units</h3> 

<p align="centre"><img width="900" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/MazePen.png"></p>

<h3 align="center">North America is the continent that generated the most revenue and highest number of transactions </h3> 

<p align="left"><img width="400" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/NorthAmeica.png"></p>

<h3 align="center">The highest revenue generating product was the 26oz Double Wall Insulated Bottle, followed by the Men's zip hoodie  </h3>

<p align="center"><img width="900" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/TreeMap-Top%20Prods.png"></p>


Below is a preview image of the interactive Tableau dashboard for this project.

Click [here](https://public.tableau.com/app/profile/ruby.rondina/viz/CapstoneProject_16390620575680/Dashboard1) to access the working dashboard on Tableau public

<p align="left"><img width="700" height="" src="https://github.com/RubyRondina/CapstoneProject/blob/main/Notebook%20and%20Viz/Dashboard.png"></p>

                                                 
### Regression Modelling Solution

I called on the NumPy and Stats model libraries in Python to create a regression model in order to determine if any variables in this dataset have a strong determining factor on the Total Revenue.

That being said, marketing and advertising are usually big drivers of revenue. That data is unfortunately not included in this obfuscated dataset as previously mentioned. So we will work with what we have even though the model, in my opinion, will not be as strong without marketing data.

The dependent variable is the Total Revenue and the independent variables are date, continent, pageviews, channel grouping (meaning the traffic source for each visitor), product category, product price and product revenue.

After running the model, it generated an R-squared and adjusted R-squared value of 0.263, which is pretty low as expected (but not the worse I've ever seen).  It's telling us that the independent variables are not doing much to affect Revenue.

I retried the model again, this time eliminating the "continents" data since revenue was really skewed by the Americas.  But the R-squared values did not change.

I retried the model again and removed the "Channel Groupings" data from the independent variables.  The R-squared value decreased by 0.003 %, which is very insignificant.

I retried the model once again by removing all the "product categories" and just leaving "pageviews," "total transactions," "Product price" and "product revenue." The model got even worse with an R-squared value of 0.254.

As expected, these variables alone do not make a good model for predicting or explaining the total revenue. They probably need to be paired with marketing, ads and promotion data to yield a decent model.

However, since I was able to draw a significant amount of analysis from the products data,  I was confident enough to make a recommendation based on that aspect to increase sales.

I noticed that most of the products on offer and most of the products purchased were skewed a bit to males. Many of the products were either unisex or specifically labeled for men. Why not try to offer more products marketed towards women - and make them a bit more 'fun' and 'girly,' but still with the air of 'intelligent sleek simplicity' that the google brand is known for.  I may of course be biased to think that women buy more than men. But it might be worth a try. If not to also erase the assumption that women are not into 'tech' as much as males. Perhaps Google, as a leading tech company should make it a goal to attract more women into the industry. Offering more products that are more attractive to the average female might be a way to do this.  And it might also just increase sales.


## Loom Video

**[Watch me present this project on Loom.](https://www.loom.com/share/943e0cde27c64c1da769e64ef1e40cd2?sharedAppSource=personal_library)**
