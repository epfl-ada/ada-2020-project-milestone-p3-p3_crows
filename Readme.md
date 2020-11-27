# Title:

Google Trends insight in understanding what drives Norwegians into purchasing an electric vehicle

# Abstract:

Norway is well advanced compared to other countries in the expansion of its electric vehicle (EV) fleet thanks to strong incentives (100% tax for combustion vehicles which are exempted for EV). It has even reached the top place in total EV sales despite its country size. Understanding the evolution of EV car sales in Norway could help predicting future sales in other countries. 

Now that we have a working model to assess the predictive power of Google Trends on a certain output, we will then extend this on investigating which set of indicators best improve the short-term prediction of a Norway EV sales. The indicators will be grouped in categories such as environment, car models, infrastructure or policy related. Additionally, we will assess the impact of corner-stone events such as the Paris Climate Accord, the release of the Tesla model 3 as well as the implementation of tax-cuts for EVs in Norway on car sales. All of this will help us assess which category of indicators/events influence most the consumer propensity to switch from combustion to electric.

# Research Questions:

- Which category of indicators influence most EV sales in Norway?  Is it environment, car models, infrastructure (charging stations) or government policies?
- Which event influenced most EV sales in Norway (the Paris Climate Accord, the release of the Tesla model 3 or the implementation of tax-cuts for EVs in Norway)?
- Is there a coherent correlation between the answers of both questions above? 

# Proposed dataset:

1) Opplysningsrådet for Veitrafikk - Road Traffic Information Council

- https://ofv.no/ 
- The data should be bought but as students we managed to request it for free
- We have not accessed the data yet, so we do not know the full content of it and cannot infer its size yet. Most probably it would be at around 100 rows (1 per month for 10 years).

2) Google Trends:

- https://trends.google.com/trends
- We will pick several indicators and investigate which ones help us best in predicting. Indicators will be grouped in these categories:
  - Environment
  - Car models
  - Infrastructure (charging stations)
  - Government policies

# Methods:

We will: 

- use the same method in the paper for Motor Vehicles and Parts,  select relevant terms for google trends
- do several experiments to find a suitable match
- use the expanding window to train the data and make prediction

The models will be:

- Base model features: 1 month lag + 12 month lag
- Indicators model features: 
  - Base + environment related indicators
  - Base + car model related indicators
  - Base + infrastructure related indicators
  - Base + government policies related indicators
  - Base + all indicators
- Indicators and events model features (Discontinuous regression model): 
  - Base + all indicators + Paris Climate accord passed? [0,1] + Tesla model 3 released? [0,1] + Norway EV tax-cut implemented? [0,1]

# Proposed timeline:

- Week 1: 
  - Data gathering & wrangling
  - Train the 3 models (base + with indicators + with indicator & events)
- Week 2: 
- Analyse and visualise the results
- Week 3: 
  - Clean and comment Notebook
  - Data story 
  - Video

# Organization within the team:

| Task                                                  | Owner   |
| ----------------------------------------------------- | ------- |
| Get the dataset  of Norway EV car sales               | Jostein |
| List the relevant  indicators and categories them     | Jostein |
| Extract csv files  of indicators via pytrends library | Max     |
| Data wrangling  and cleaning                          | Max     |
| Train the 3 models                                    | Sha     |
| Analyse the results                                   | All     |
| Results visualisation                                 | Sha     |
| Clean and comment the Notebook                        | Max     |
| Data story                                            | Max     |
| Video                                                 | Jostein |