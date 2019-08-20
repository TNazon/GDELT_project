# GDELT Project 

### What the GDELT Project is 
Access [The GDELT Project](https://www.gdeltproject.org/)

Databases used for the project: 

**GDELT Event Databse**
> The GDELT Event Database records over 300 categories of physical activities around the world, from riots and protests to peace appeals and diplomatic exchanges, georeferenced to the city or mountaintop, across the entire planet dating back to January 1, 1979 and updated every 15 minutes.

**GDELT Global Knowledge Graph**
> Much of the true insight captured in the world's news media lies not in what it says, but the context of how it says it. The GDELT Global Knowledge Graph (GKG) compiles a list of every person, organization, company, location and several million themes and thousands of emotions from every news report, using some of the most sophisticated named entity and geocoding algorithms in existance, designed specifically for the noisy and ungrammatical world that is the world's news media.

### Goal
Build a resilient and efficient NoSQL infrastructure on which to query 5 different requests on the GDELT database: 
1. Display number of articles/events published/that occured for a triplet Day/Country/ArticleLanguage
2. For a given "Actor", display events related to such an actor in the last 6 months
3. Find topics gathering the highest number of articles with a positive/negative tone for a triplet Month/Country/ArticleLanguage
4. Find which Actor/Country/Organization received the highest number of articles with a positive/negative tone for every triplet Month/Country/ArticleLanguage
5. Estimate the evolution of geopolitical relationship between two given countries based on articles coverage

### Approach
- Build a MongoDB infrastructure via AWS EC2 
- Pre-process GDELT via Spark Scala to store 1 year of data on MongoDB (going from 700GB of data down to 79GB after pre-processing)

### Results
- Infrastructure able to requests all required information
- Resilient 
- Low-cost
