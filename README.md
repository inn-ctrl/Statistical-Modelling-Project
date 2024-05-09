# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
(fill in your description and goals here)
* This project aims at studying the underlying relationship between London restaurants and various bike stations. I will use statistical modelling to find patterns in the datasets using various APIs. These patterns should lead to the regressional analysis that shows the underlying relationship between the two variables.
  
* Project goals: 
* Compare various APIs and distinguish them based on business requirements
* Fine-tune dataset from combined APIs for readiness in future use
* Perform a regression model on the dataset and provide analysis

## Process
### Connecting to and comparing APIs
* I parsed throuh both city_bikes, Yelp, and Foursquare APIs to retrieve the data that I needed to work with.
* Most of the data needed to be transformed into python dictionaries for better future manipulation
* That allowed me to parse through them and create a panda dataframe that was easy to see and perform descriptive analysis
* Finally, I transofrmed all the dataframes into excel sheets just in case I would need to import them for future use - which turned out to be the case.

#Comparing Yelp and Foursquare APIs
* Yelp API and Foursqure APIs provide almost similary information (points of interests in London). but the following observations made me choose Yelp API:
* Yelp provides data that fits the need more (restaurants in locality)
* Yelp provides data that are more quantititive
* Yelp provide data that would easily show effect when combined with city_bikes API
  
* With this in mind, I parsed the Yelp API as a dataframe and cleaned it for future use. 
  
### Joining APIs data

* The data from city_bikes API provides information about bike stations in London and Yelp API provides information about restaurants in the same city.
* I combined them to have a more concrete dataset about restaurants and nearby bike stations in London
* I created a new dataset from the combined API with this question in mind (how does restaurant performance/perception affect nearby bike stations?)
* This particular question helped me visualize the data so that it shows how the indpenend variable (review_counts) affect dependent variables (empty_slots and free_bikes)

### Regression Model 

*result = 0.6675559949626377 shows the coefficent of determination that need improvement. 
*this must be due to presence of 'rating' in the dependent variables because when we remove it, all of a suddenthe value goes to 0.9774541690203772; indicating a high relationship between independent variables and dependent variables

#interpretation
how does restaurant performance/perception affect nearby bike stations?

From the above , we can conclude that bike slots usage is highly affected by nearby resaurants performance/perception

## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)
#Yelp API is richer in the data needed in this case compared to Foursquare API. Firstly, that is due to the presence of ratings which will make it easier for customers to relate different POIs in the area. Secondly, it provides a varied range of Points of interests and then gives enough quantititive data that would make it easier to make meaningful conclusions when measuring performance.

* Regression Model:
* variables are review_coun-independent and empty_slots and free_bikes - dependent
* The model shows high correrlation between the variables (r-square = 0.9774541690203772)
* This means that there is the performance of nearby restaurants greatly affect bike slots access. 

## Challenges 
(discuss challenges you faced in the project)
* Material understanding: This project gave me a golden opportunity to apply the skills I have been learning in the bootcamp. However, most of them I have not yet mastered which took longer to understand the questions since I first had to do researches. However, I feel very proud looking back because there is no way I would have understood what I understand now without such an opportunity. 
* Limited time: With that said, the time was not enough to complete the project to my absolute liking; but I take that as a chance to keep working on it, even after grading. 
* Health: I had health issues in the beginning of the project, which made me lag behind the deadline. I feel good about having used time very well after the recovery though. 

## Future Goals
(what would you do if you had more time?)
* In the future, I will have a lot of fun in going back in the APIs and study them some more, so that I fine-tune data fetching. I believe that will improve the performance the
regression model. 
