Articles: 

* [Reuters](https://www.reuters.com/article/us-india-trafficking-technology/big-data-maps-indias-human-traffic-hot-spots-idUSKBN18R21N)
* [Analytics India Magazine](https://analyticsindiamag.com/big-data-tackles-human-trafficking-indian-ngo-aussie-analytics-firm-quantium-partner-save-lives/)

Questions:

* Of the problem types introduced in the lecture, with which one does this use case most closely align?
    * This is an identification problem. This means that we're identifying, whether each village in India is or is not at risk for human trafficking.
* How did the company/organization use data science to achieve a desired impact?
    * The My Choices Foundation in India partnered with the Australian analytics firm Quantium to create an analytics tool which would help My Choices Foundation know how to allocate its resources.
* What was their impact hypothesis?
    * The desired impact is to reduce the number of people trafficked.
    * The impact hypothesis is that by identifying villages at risk for human trafficking, the My Choices Foundation can offer educational programs to inform parents, teachers, village leaders and children about traffickers, thus reducing the number of people who are trafficked.
* What was their data science solution path? Can you think of any other solution paths they may have or could have considered?
    * We would most likely use a classification algorithm to address this problem.
    * Alternatively, we could potentially use clustering to see the groups that villages naturally fall into. 
    * We could also use a time series model to predict when traffickers are likely to strike, as indicated in the Analytics India article. 
    * Building on these methods, we might find it useful to ensemble multiple models and methods, passing results from one model into another. 
    * Also building on the above methods, we could create something like a recommendation system to identify villages that are similar to villages we know are at risk.
    * As always, we could add important EDA to identify patterns and trends.
* What data did they use?
    * The data include data from India’s census, education and health data, data related to drought risk, poverty levels, job opportunities, proximity to transportation, distance to police stations, crime data, etc.
* What lingering questions do you have about this case study?
    * Ideally, we would offer a figure to answer the question of by how much we would like to reduce the number of people trafficked. We could come up with a reasonable number on our own, but more information from the organization would allow us to determine what reduction would make a meaningful difference, measured according to some specific practical criteria, such as by how much (in dollars, people, etc) we might like to reduce the power of trafficking in a given time period.
    * What does one row of data look like? Since there are 600,000 villages, it would make sense if one row were one village, but could we (or should we) go more granular than that?
    * In order to make predictions, we need to have several observations, or rows, with a target value already determined (i.e. at risk or not at risk). How are we making these determinations in our training data such that we can then successfully apply what we learned from them to new data?
