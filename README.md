# Movie Festival Itinerary Optimization - README
## Introduction
This project aims to optimize the movie festival experience by predicting the Audience Score of films and creating an optimal movie itinerary. We utilize Rotten Tomatoes data, focusing on the Audience Score as a key metric. Our approach combines prediction and optimization models to maximize the utility for moviegoers.

## Data
We sourced data from five datasets, primarily focusing on the "Rotten Tomato Movie Reviews" dataset for the target Audience Score. Additional data about cast, directors, and awards were obtained from "All Movie", "900 acclaimed directors awards", "IMDB Analysis", and "the oscar award" datasets. The data was cleaned and prepared for analysis, involving one-hot encoding, extraction, and type conversion processes.

## Datasets Overview:
All Movie: Contains movie details from Rotten Tomatoes.
900_acclaimed_directors_awards: Details about directors and their awards.
IMDB Analysis: Focuses on Facebook popularity of directors and actors.
Rotten Tomato Movie Reviews: Movie details, Tomatometer and Audience scores.
The Oscar Award: Information about Oscar nominees and winners from 1927-2020.
## Methods
## Prediction
We explored five models: Linear Regression, LassoCV, RidgeCV, Decision Tree Regressor, and Random Forest Regressor. The models were tested with default parameters, and further refined with feature engineering, mutual information regression, bagging, data scaling, and grid search. A stacked ensemble approach with RidgeCV as the meta-model was used for the final prediction model.

## Optimization
The optimization model aims to create an optimal itinerary based on the predicted Audience Scores. The objective function maximizes the sum of Audience Scores within various constraints.

## Constraints
We considered both preference and physical constraints:

Preference Constraints: Budget limits, genre preferences, runtime limits, specific genre at certain times, and overall genre preference.
Physical Constraints: Movie availability per time slot and avoidance of overlapping movies.
## Results
The final prediction model showed a test score of 39.9%. The optimization model, evaluated with both predicted and actual Audience Scores, produced similar itineraries, validating our approach.

## Discussion
While successful, the project faced limitations like outdated data and model sensitivity. The optimization model's structure may limit its application to more complex festival schedules due to computational constraints.

## Conclusion
The best model achieved around 40% accuracy in predicting the Audience Score. The optimization model successfully created a viable movie itinerary, demonstrating the utility of our approach in planning for movie festivals.

## Future Directions
Future work includes improving the Audience Score prediction by categorizing it into bins for classification models. Testing the model on upcoming movies will provide further insights and enhancements
