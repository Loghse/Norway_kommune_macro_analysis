# Norway_kommune_macro_analysis
Exploratory analysis of macro level socio economic conditions among Norwegian kommunes

Following is an exploratory analysis on socio economic conditions in Norway across various municipalities.
Some of the interesting questions I would like to raise and attempt to find answers to are : 
1.	Why some municipalities operate profitably and few do not?
2.	Does the immigrant population adds strength to local economy of municipalities?
3.	Does education level play a role?
4.	How does crime rate distribute across municipalities? Are there any links to education, income and immigration?
5.	Based on our findings could we recommend a municipality or a region to someone immigrating to Norway?
6.	If I were to move to Norway, which commune or locality would I choose?

The notebook and the report attempts to provide better understanding of socio economic conditions in Norway, based on realistic figures. It is targeted for people who wants to know more about Norway or to those living in Norway to know more about the municipalities they live in.

Following data were used: 
1.	Commune wise indicators
Norwegian statistics department operates a webpage. The basic facts of each municipalities are available in their webpage https://www.ssb.no/kommunefakta/. The data for each municipality looks as this https://www.ssb.no/kommunefakta/agdenes . Like this there are 422 municipalities. 

Each page contains demographics, income, education, religion and commune’s profitability. 

I used algorithmic scrapping - ‘Beautiful soup’ method to go to each webpage and scrape necessary information out of each commune page. 

2.	Crime data
Crime rate is one of the important indicators to assess well-being at living place. Unfortunately, there is no crime data available in commune pages. However, statistics department has a table available that contains total number of registered complaints per police district. 

Utilizing data manipulation and data wrangling, we can find offences per 1000 inhabitants registered at police. We can then separate them into commune wise figures.

3.	Geo Co ordinates
We need geo coordinates to create visual impact of our analysis. Geo Coordinates of each municipalities or their centroids are not directly available. I was able to find a table with postcode and their coordinates. The problem is each municipality have several post codes.  

Using data manipulation techniques, we can extract coordinates per postcodes into commune wise then find the centroid for each municipality. 

4.	Geojson
Geojson file is necessary to link our findings into geographical spread. Geonorge is the official body for creating and maintaining maps in Norway. From their page, it was possible to extract polygons for each commune and was made into geo json file. 
