# Traffic Accidents: The where and the why.
### Kapilan Mahalingam, Business Project Proposal, August 2022

1. Client:

    The Client is the department of transportation.

2. Question/Need:

    What are the areas/conditions that lead to the most traffic accidents? The 'data science opportunity' is to optimise roadway resource allocation to minimize accidents, and providing input to the design decisions going forward.

3. Impact

    The impact is that by identifying dangerous conditions/locations, better signage and/or redesigning intersections will reduce traffic accidents.
    The impact hypothesis is that identification of high accident zones/conditions will let implement strategies to improve saftey.

4. Data Description:

    The dataset is from [Kaggle](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents), on US accidents. Due to the size of the dataset I'll only be using a portion of it, either a single year or a few months. An individual observation is a single accident. I expect to use the geographical location, time of day, weather conditions, and site of the accident (roundabout, pedestrian crossing, etc.)

5. Solution Path

    Firstly, a classification model to try and sort locations (streets, or counties) into high/low accident zones. Then looking at the realtionship between weather conditions/accident sites with frequency of accidents, and identify anomalously accident-prone areas.

    Alternative solutions could include increasing enforcement, traffic cameras, and the like globally. Forcing people to retake driving tests every decade might also help mitigate the problem of unfit drivers. Stricter penalties against inebriated/distracted driving could also discourage accident causing behavior.

6. Criteria for Success

    Success in this case would be a reduction in the number/severity of accidents.

7. Assumptions and Risks:

    I'm positing that identification will allow better resource allocation, so implicitly assuming that knowing something is dangerous will allow us to make it less so. Depending on the current condtion, ameliorating road saftey might be infeasable. For example, if there already are well-signed accident-prone locations, redesigning the roadway could be prohibitively expensive.

8. Tools:

    I'll use Excel and Tableau, because course requirements. Correlation plots, scatterplots, histograms sould be able to identify the most accident-prone locations and weather conditions. Following that, using a ML model to identify predictors of accidents might be a productive direction to take.

9. MVP Goal:

    Identifying the most dangerous street/county/city in the data would be a good starting point.
