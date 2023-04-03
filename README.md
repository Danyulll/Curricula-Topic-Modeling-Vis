# Data Science Curricula Topic Modeling

This project aims to apply Topic Modeling to various Data Science course calendars. The goal is to leverage Latent Dirichlet Allocation (LDA) to model pathways through degrees as a three-level hierarchical Bayesian model. This model defines a collection of documents as a random mixture over some underlying topic set where each topic is itself a distribution over our vocabulary. This then allows us to cluster words into latent topics and discover common learning outcomes in Data Science Curricula.

# Data Generating Process

The data has been collected by [Hedgemon4](https://github.com/Hedgemon4/course-scraping). From their dataset we extract the list of course codes from a given university's course calendar and the corresponding course descriptions. We then construct degree pathways by sampling courses from the calendars. This produces a reasonable approximation to a student's journey through a curriculum. Notably some limitations are that we do not check for prerequisites nor include non-science courses.

# Data Analysis

In our application of LDA we cocatenate all course descriptions from a sampled degree pathway and set these as our documents. This then means our terms are individual words and LDA clusters our words into $K$ topics.

The notebook introduces LDA and common Natural Language Processing (NLP) practices to clean text data. We then explore how one discovers an optimal $K$ and visualize our topics using [LDAvis](https://github.com/cpsievert/LDAvis).

**TO DO: **one we finish analysis provide better summary

The notebook is available on GitHub pages and may be viewed directly  [here](https://danyulll.github.io/Curricula-Topic-Modeling/). The analysis is conducted in R and presented using Quarto.


