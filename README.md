# ATIS-Flight-Reservations-Information-Extraction

The ATIS (Airline Travel Information Systems) dataset consists of English language queries for booking (or requesting information about) flights in the US.

Each word in a query (i.e. a request by a user) is labelled according to its entity-type, for e.g. in the query 'please show morning flights from chicago to new york', 'chicago' and 'new york are labelled as 'source' and 'destination' locations respectively while 'morning' is labelled as 'time-of-day' (the exact labelling scheme is a bit different, more on that later).

Some example queries taken from the dataset are shown below:

{
'what flights leave atlanta at about DIGIT in the afternoon and arrive in san francisco',
 'what is the abbreviation for canadian airlines international',
 "i 'd like to know the earliest flight from boston to atlanta",
 'show me the us air flights from atlanta to boston',
 'show me the cheapest round trips from dallas to baltimore',
 "i 'd like to see all flights from denver to philadelphia"
 }

# Objective
Our objective is to build an information extraction system which can extract entities relevant for booking flights (such as source and destination cities, time, date, budget constraints etc.) in a structured format from a given user-generated query.

A structured format could be a dictionary, a JSON, etc. - basically anything that can be parsed and used for looking up relevant flights from a database.

# Dataset
The dataset is divided into five folds, each fold having a training, validation and test set.

# Table of Contents:

1. Understanding the Data

2. Information Extraction
   a. Pipeline for Information Extraction Systems
   b. Named Entity Recognition (NER)

3. Models for Entity Recognition

   a. Rule-based models
      a1. Regular Expression Based Rules (ex)
      a2. Chunking

   b. Probabilistic models
      b1. Unigram and Bigram models
      b2. Naive Bayes Classifier
      b3. Conditional Random Fields (CRFs)
