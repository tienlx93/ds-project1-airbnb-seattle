### Please allow me 1 more day to complete this project. Thanks very much !

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

This is my first project into the Data Science field to apply the Crips-DM ([link](https://en.wikipedia.org/wiki/Cross-industry_standard_process_for_data_mining)) methodology.

For this project, I was interestested in using Airbnb listing data of Seattle to better understand:
- What is the interesting parts about the data, included pricing, size, how to create a good description for a listing...
- What aspect impact the pricing and popularity of a listing

## File Descriptions <a name="files"></a>

- `Seattle Airbnb analysis.ipynb`: Main notebook file included all the works. This included 4 parts:
1. Part 1: Review & cleanup data
2. Part 2: Pricing overview
3. Part 3: How to get good impression by title, description & user reviews
4. Part 4: What aspect affect pricing & user review
- `data/listings.csv`: detail of the listing, include detail of rental, place, pricing, user review
- `data/reviews.csv`: detail of all review of places
- `data/calendar.csv`: detail of pricing & avaiability of listings by day
- `output`: folder containing output tables, images

## Results<a name="results"></a>

Throughout the project file `Seattle Airbnb analysis.ipynb` it will help to demostrate the CRIPS-DM method.

* Business Understanding
    * Question 1: When is the busiest time to visit Seatle? Where is the common place to be visited?
    * Question 2: Based on the description & review, what we can learn to create a more attractive listing?
    * Question 3: What aspect impacted the most on nighly pricing? What aspect impacted the popularity of a listing, based on number of reviews per month?

* Data Understanding: The provided data included:
    * `listings.csv`: detail of the listing, include detail of rental, place, pricing, user review
    * `reviews.csv`: detail of all review of places
    * `calendar.csv`: detail of pricing & avaiability of listings by day

* Prepare Data: Through the first part of 'Review & cleanup data', we run through some clean up & prepare like:
    * Cleanup the numeric & pricing value for a clean numberic output
    * Remove the unnessary data
    * Create the statistic tables, correlation matrix, data distribution for better understanding of data
    * For the question 1, we merge the `listings.csv` and `calendar.csv` to see the pricing distribution. It is covered on the Part 2 of the project
    * For the question 2, we merge the `listings.csv` and `reviews.csv` for the review & descritions of a listing. We applied the words deviding, then count the appearance of each word, to compare the difference between the most attractive listing (based on number of reviews per month) and all listing.

* Modeling
    * Fit model: After clearing & enrich data, create columns for categorical values, we fit the model into the standard linear regression model. This is done in the 4th part on the notebook.
    * Validate the model: After changing the parameter, we removed some columns that create overfitting data, only focus on most interesting data
    * After apply the modeling, we can answer Question 3, what aspect affect the most on pricing and popularity

* Evaluation: The main findings of the project can be found at the post available [here](https://medium.com/@bestoneguy/how-to-create-a-best-listing-on-airbnb-a-study-from-seattle-airbnb-listing-data-9055d4b92be3).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

The data inside `data` folder is credited to Airbnb for the. You can find the Licensing for the data and other descriptive information at the Kaggle link available [here](https://www.kaggle.com/airbnb/seattle). 

The notebook is created for educational purpose. Please freely to contribute, remix and make it your own work / with or without any credit to original works.
