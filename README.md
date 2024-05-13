# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
(fill in your description and goals here)
* This project aims at studying the underlying relationship between London restaurants and various bike stations. I will use statistical modelling to find patterns in the datasets using various APIs. These patterns should lead to the regressional analysis that shows the underlying relationships.
  
* Project goals: 
* Compare various APIs and distinguish them based on business requirements
* Fine-tune dataset from combined APIs for readiness in future use
* Perform a regression model on the dataset and provide analysis

* Navigating the project:
* city_bikes.ipynb file contains bike stations API. Similarly, yelp_foursquare.ipynb file contains yelp and foursquare APIs(respectively).
* The above are combined in joining_data.ipynb, cleaned, and visualized to prepare for a model building
* The model is explored in model_building.ipynb

## Process
### Connecting to and comparing APIs
* I parsed throuh both city_bikes, Yelp, and Foursquare APIs to retrieve the data that I needed to work with.
* Most of the data needed to be transformed into python dictionaries for better future manipulation
* That allowed me to parse through them and create a panda dataframe that was easy to see and perform descriptive analysis
* Finally, I transofrmed all the dataframes into excel sheets just in case I would need to import them for future use - which turned out to be the case.

#Comparing Yelp and Foursquare APIs
* Yelp API provides crucial information about local POIs (ratings, and review counts)
* Yelp provides data that are more quantititive
* Yelp provide data that would easily show effect when combined with city_bikes API 
  
* With this in mind, I parsed the Yelp API as a dataframe and cleaned it for future use.

#Data Cleaning 
Before linear model building, I used review counts and ratings of restaurants to come up with one parameter (restaurant performance). This helped me to compare the number of bikes easily because using individual item was providing graphs whith not much insights. In marketing perpective, a hight number of reviews and a high humber of rankings show nothing more than customer trust (https://www.tidio.com/blog/ratings-and-reviews/#) Therefore, It made sense to combine them and come up with a common scale
that shows the overall performance of a restaurant. I call it performance because it shows its success in pleasing customers who make purchases. 
  
### Joining APIs data

* The data from city_bikes API provides information about bike stations in London and Yelp API provides information about restaurants in the same city.
* I combined them to have a more concrete dataset about restaurants and nearby bike stations in London
* I created a new dataset from the combined API with this question in mind 
### Regression Model 

#I wanted to discover the number number of bikes have on both empty slots and restaurant performance. Using linear regression, I found the value of r-square, which I used to see which varable as the closest varaince to free_bikes

#finding r-square value is enough because I am only interested in finding relationship between variables which I might use to provide more insights

#relationship between free_bikes and performance (of restaurants) # result = 0.9
#free_bikes and review_counts # result = 0.8
#free_bikes and review_counts # result = 1.0

#interpretation
how does restaurant the number of bikes to the nearby bike stations affect affect restaurant performance?

From the above , we can conclude that bike slots usage is highly affected by nearby resaurants performance/perception

## Results

In the model, I only used found r-square value because I wanted to see the impact number of bikes have on various factors. fristly, number of bikes and 
performance of nearby performance shows strong relationship. This shows that the restaurants performance are highly affected by being in locations where there
are more bikes in the bikes stations. Confirm this I also looked at review counts as a separate value (since performance takes reviews and ratings into account)
but the result seem to be not so different considering that ratings was ommmitted. So, that changed nothing. 

Secondly, the number of bikes and empty slots shows a strong relationship. This shows that the two factors are very important and inf restaurants could reverage them
(perhaps operate in areas with many bike slots and free bikes) that would improve their performance as well. (Why does it have an impact on the performance? Well, 
because in the first value we found a strong relationship between the free bikes and restaurant performance)

In short  we can conclude that the number of bikes highly impact bike slots and hence the perfromance of nearby resaurants in london. 

## Challenges 
(discuss challenges you faced in the project)
* Material understanding: This project gave me a golden opportunity to apply the skills I have been learning in the bootcamp. However, most of them I have not yet mastered which took longer to understand the questions since I first had to do researches. However, I feel very proud looking back because there is no way I would have understood what I understand now without such an opportunity. 
* Limited time: With that said, the time was not enough to complete the project to my absolute liking; but I take that as a chance to keep working on it, even after grading. 
* Health: I had health issues in the beginning of the project, which made me lag behind the deadline. I feel good about having used time very well after the recovery though. 

## Future Goals
(what would you do if you had more time?)
* In the future, I will have a lot of fun in going back in the APIs and study them some more, so that I fine-tune data fetching. I believe that will improve the performance the
regression model. 
