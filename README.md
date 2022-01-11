{\rtf1\ansi\ansicpg1252\cocoartf2580
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 HelveticaNeue-Bold;\f2\fnil\fcharset0 HelveticaNeue;
\f3\fswiss\fcharset0 ArialMT;\f4\froman\fcharset0 Times-Roman;\f5\fnil\fcharset0 HelveticaNeue-Italic;
\f6\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red27\green31\blue35;\red255\green255\blue255;\red26\green23\blue24;
\red0\green0\blue0;\red26\green23\blue24;\red0\green0\blue117;\red234\green234\blue234;\red0\green0\blue0;
\red82\green0\blue83;\red83\green85\blue2;\red16\green121\blue2;}
{\*\expandedcolortbl;;\cssrgb\c14118\c16078\c18431;\cssrgb\c100000\c100000\c100000;\cssrgb\c13725\c12157\c12157;
\cssrgb\c0\c0\c0;\cssrgb\c13725\c12157\c12157;\cssrgb\c0\c0\c53333;\cssrgb\c93333\c93333\c93333;\cssrgb\c0\c0\c0\c87059;
\cssrgb\c40000\c0\c40000;\cssrgb\c40000\c40000\c0;\cssrgb\c0\c53333\c0;}
\margl1440\margr1440\vieww27020\viewh12660\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Capstone Project: 
\f1\b\fs40 \cf2 \cb3 \expnd0\expndtw0\kerning0
Google Analytics, Google Merchandise E-commerce Store 
\f0\b0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \
\
<p align="left"><img width=\'93600" height="" src=""></p>\
\
\
\pard\pardeftab720\sa320\partightenfactor0

\f2\fs32 \cf2 \cb3 \expnd0\expndtw0\kerning0
In this bootcamp capstone project, we were called to use our analytical and modelling skills in Python, as well as our graphic design and presentation skills in Tableau, in order to tell a deep story about a dataset of our choice.  
\f0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
## Dataset\
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <p align=\'93centre><img width=\'93600" height="" src=""></p>\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\
I chose the Google Analytics sample dataset from BigQuery Public so that I could also flex my SQL muscles.\
\
\pard\pardeftab720\sl404\sa266\partightenfactor0

\f3\fs29\fsmilli14667 \cf4 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 This dataset contains Google Analytics 360 data from the Google Merchandise e-commerce Store.
\f4\fs24 \cf5 \cb1 \strokec5 \
\pard\pardeftab720\sl404\sa266\partightenfactor0

\f3\fs29\fsmilli14667 \cf4 \strokec4 The raw data spans information from Aug. 2016 to July 2017, containing 16 columns with several nested arrays within nested arrays.  The fields contain  dates, visitor IDs, visit numbers, visit start times, hits, page views, bounces, time on site, transactions and product data, traffic source details, device information, geoNetworks and a supposed \'93social engagement type\'94 for each user.
\f4\fs24 \cf5 \strokec5 \

\f3\fs29\fsmilli14667 \cf4 \strokec4 My main focus on this project is the REVENUE.\'a0 \
## The Question:  \
What 
\fs29\fsmilli14667 \cf6 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 specific
\fs29\fsmilli14667 \cf4 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4  variables in this dataset have a strong determining factor on the Total Revenue?\'a0 And what recommendations can I propose to increase sales thereafter?
\f4\fs24 \cf5 \strokec5 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 \
## Challenges\
\
\pard\pardeftab720\sl404\sa266\partightenfactor0

\f3\fs29\fsmilli14667 \cf6 \expnd0\expndtw0\kerning0
My intent was to study the full year\'92s worth of data.  The process of pulling queries using SQL directly on BigQuery in order to examine the full year\'92s performance was quite painless and pretty straightforward.  However, since the project requirement called for exploratory data analysis using Python, I had to limit the study to only two month\'92s worth of data.  This is due to the fact that Python is not as well optimized as SQL to process big data.  It took my machine almost one hour to import the full year\'92s worth of data into Python.  We had less than a week to complete this project, so in order to save time and computer processing power, I only dealt with data from December 1, 2016 to January 31, 2017.\'a0\'a0\
Another issue was that Google made some fields in this dataset obfuscated or removed for privacy reasons.\'a0 This is specifically data on marketing related details such as ads, promotions, campaigns, keyword searches and certain traffic sources.  I also discovered that the field for \'93social engagement type\'94 was filled with \'93not socially engaged\'94 users only. \
Thankfully, there was a plethora of information relating to products, prices and geographic locations where I could draw my focus.\
Last but not least, it is important to note 
\fs29\fsmilli14667 \cf4 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 that web traffic is only tracked when a user\'92s cookies are on.  Visitors who did not enable their cookies when visiting the website are not part of this dataset.  As useful and as powerful of a tool that it is, Google Analytics simply cannot obtain the full picture since it is unable to track hidden visitors and their behaviours.\
It is not perfect but we will make best efforts with the best tools that we have since the alternate would just be irresponsible.\
\pard\pardeftab720\partightenfactor0

\fs29\fsmilli14667 \cf6 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \kerning1\expnd0\expndtw0 ## The Process \
\
The first step was to query a table from BigQuery, limited to data for December and January only, as well as information on the products, prices, transactions, revenue and geo location by continent.  I then imported that table to Python Jupyter notebooks to start exploring the data.\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
**See full Jupyter Notebook [here]()**\
\
\pard\pardeftab720\sa320\partightenfactor0

\f1\b\fs32 \cf2 \cb3 \expnd0\expndtw0\kerning0
**Python libraries used**
\f2\b0 \cf2 : *
\f5\i \cf2 NumPy, Pandas, Statsmodels*\
\pard\pardeftab720\sa320\partightenfactor0

\f2\i0 \cf2 My initial analysis revealed the following:
\f0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <h3 align="center">December yielded more revenue than January</h3>\
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <p align=\'93centre><img width=\'93600" height="" src=""></p>\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <h3 align="center">The following descriptive stats on product prices</h3>\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <p align=\'93centre><img width=\'93600" height="" src=""></p>\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <h3 align="center">The highest number of units sold was the **maze pen** at 500 units</h3> \
\
<p align=\'93centre><img width=\'93600" height="" src=""></p>\
\
<h3 align="center">North America is the continent that generated the most revenue and highest number of transactions </h3> \
\
<p align=\'93centre><img width=\'93600" height="" src=""></p>\
\
<h3 align="center">The highest revenue generating product was the 26oz Double Wall Insulated Bottle, followed by the Men\'92s zip hoodie  </h3>\
\
<p align=\'93centre><img width=\'93600" height="" src=""></p>\
\
\
Below is a preview image of the interactive Tableau dashboard for this project.  You can click on the image to access the working dashboard on Tableau public\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 <p align=\'93centre><img width=\'93600" height="" src=""></p>\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab720\partightenfactor0

\f6\fs30 \cf7 \cb8 \expnd0\expndtw0\kerning0
\shad\shadx20\shady-20\shadr20\shado0 \shadc0 <a\cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0  \cf10 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 href\cf11 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 =\cf12 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 "https://public.tableau.com/app/profile/ruby.rondina/viz/CapstoneProject_16390620575680/Dashboard1"\cf7 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 >\cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 \
\'a0 \'a0 \'a0 \'a0 \'a0\cf7 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 <img\cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0  \cf10 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 alt\cf11 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 =\cf12 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 "Dashboard\'94
\fs26 _
\fs30 \cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0  \cf10 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 src\cf11 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 =\cf12 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 ""\cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 \
\'a0 \'a0 \'a0 \'a0 \'a0\cf10 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 width\cf11 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 =\cf12 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 150" height="\cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 70\cf12 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 ">\cf9 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 \
\'a0 \'a0 \'a0 \cf7 \shad\shadx20\shady-20\shadr20\shado0 \shadc0 </a>
\f0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \shad0 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
### Regression Modelling Solution\
\
I called on the  NumPy and Stats model libraries in Python to create a regression model in order to determine if any 
\f3\fs29\fsmilli14667 \cf4 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 variables in this dataset have a strong determining factor on the Total Revenue.\'a0 \

\f4\fs24 \cf5 \strokec5 \
\pard\pardeftab720\sl386\partightenfactor0

\f3\fs28 \cf4 \strokec4 That being said, marketing and advertising are usually big drivers of revenue. That data is unfortunately not included in this obfuscated dataset as previously mentioned. So we will work with what we have even though the model, in my opinion, will not be as strong without marketing data.\

\f4\fs24 \cf5 \strokec5 \

\f3\fs28 \cf4 \strokec4 The dependent variable is the Total Revenue and the independent variables are date, continent, pageviews, channel grouping (meaning the traffic source for each visitor), product category, product price and product revenue.
\f4\fs24 \cf5 \strokec5 \

\f3\fs28 \cf4 \strokec4 \
After running the model, it generated an R-squared and adjusted R-squared value of 0.263, which is pretty low as expected (but not the worse I\'92ve ever seen).\'a0 It\'92s telling us that the independent variables are not doing much to affect Revenue.\'a0\'a0
\f4\fs24 \cf5 \strokec5 \

\f3\fs28 \cf4 \strokec4 \
I retried the model again, this time eliminating the \'93continents\'94 data since revenue was really skewed by the Americas.  But the R-squared values did not change.
\f4\fs24 \cf5 \strokec5 \

\f3\fs28 \cf4 \strokec4 \
I retried the model again and removed the \'93Channel Groupings\'94 data from the independent variables.\'a0 The R-squared value decreased by 0.003 %, which is very insignificant.\

\f4\fs24 \cf5 \strokec5 \

\f3\fs28 \cf4 \strokec4 I retried the model once again by removing all the \'93product categories\'94 and just leaving \'93pageviews,\'94 \'93total transactions,\'94 \'93product price\'94 and \'93product revenue.\'94\'a0 The model got even worse with an R-squared value of 0.254.\

\f4\fs24 \cf5 \strokec5 \

\f3\fs28 \cf4 \strokec4 As expected, these variables alone do not make a good model for predicting or explaining the total revenue.\'a0 They probably need to be paired with marketing, ads and promotion data to yield a decent model.
\f4\fs24 \cf5 \strokec5 \
\

\f3\fs28 \cf4 \strokec4 However, since I was able to draw a significant amount of analysis from the products data,  I was confident enough to make a recommendation based on that aspect \cf6 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 alone\cf4 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 , to increase sales.\
\
\pard\pardeftab720\sl386\partightenfactor0

\f4\fs24 \cf5 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 ### Recommendation \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
\pard\pardeftab720\sl386\partightenfactor0
\cf5 \
\pard\pardeftab720\sl386\partightenfactor0

\f3\fs28 \cf4 \cb3 \strokec4 I noticed that most of the products on offer and most of the products purchased were skewed a bit to males. Many of the products were either unisex or specifically labeled for men. Why not try to offer more products marketed towards women - and make them a bit more 'fun' and 'girly,' but still with the air of 'intelligent sleek simplicity' that the google brand is known for.\'a0 I may of course be biased to think that women buy more than men. But it might be worth a try. If not to also erase the assumption that women are not into 'tech' as much as males. Perhaps Google, as a leading tech company should make it a goal to attract more women into the industry. Offering more products that are more attractive to the average female might be a way to do this.\'a0 And it might also just increase sales.
\f4\fs24 \cf5 \cb1 \strokec5 \
}