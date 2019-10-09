# NLP-Tools-in-Python
- Topic Modeling (LDA), n-gram
- Funnel Tagging with Google NL API and Classification 
    - Goal: Classify the keywords into three pre-determined market funnels by known tagging rules
    - https://blog.alexa.com/how-to-optimize-for-three-types-of-buyer-keywords/
    - While we can only have a limited number of tagging rules, we want to find out how the search result pages behave in each market funnel, so that we can simplify the manual tagging process
    - E.g. any keywords with 'price' is a transactional keyword, and we will label every keyword with 'price' as transactional. Then we may miss the label 'payment' if it is not in our tagging rule knowledge base. While all transactional keywords may have similar features shown up in the search results, we want to model the common features with known transactional words to predict the unknown transactional words.
    - Create features based on search results (titles) applying NLP using Google Natural Language API
    - Features include: search result type, sentiment, syntax (part of speech, label), entity types
    - Predict the market funnels of each keyword by a random forest model (Sklearn)
