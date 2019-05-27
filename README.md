# jigsaw-nlp
Jigsaw Unintended Bias in Toxicity Classification. To detect toxicity across a diverse range of conversations.

## Overview
The Conversation AI team, a research initiative founded by Jigsaw and Google (both part of Alphabet), builds technology to protect voices in conversation. A main area of focus is machine learning models that can identify toxicity in online conversations, where toxicity is defined as anything rude, disrespectful or otherwise likely to make someone leave a discussion.

## Motivation
Models built by Conversation AI team, predicted a high likelihood of toxicity for comments containing those identities (e.g. "gay"), even when those comments were not actually toxic (such as "I am a gay woman"). This happens because training data was pulled from available sources where unfortunately, certain identities are overwhelmingly referred to in offensive ways. Training a model from data with these imbalances risks simply mirroring those biases back to users.

## Current Work
To build a model that recognizes toxicity and minimizes this type of unintended bias with respect to mentions of identities. We'll be using a dataset labeled for identity mentions and optimizing a metric designed to measure unintended bia and also to develop strategies to reduce unintended bias in machine learning models.

## Dataset
### Features: 
id
comment_text
severe_toxicity
obscene
identity_attack
insult
threat
asian
atheist
bisexual
black
buddhist
christian
female
heterosexual
hindu
homosexual_gay_or_lesbian
intellectual_or_learning_disability
jewish
latino
male
muslim
other_disability
other_gender
other_race_or_ethnicity
other_religion
other_sexual_orientation
physical_disability
psychiatric_or_mental_illness
transgender
white
created_date
publication_id
parent_id
article_id
rating
funny
wow
sad
likes
disagree
sexual_explicit
identity_annotator_count
toxicity_annotator_count

### Subtype attributes(additional avenue for research):
severe_toxicity
obscene
threat
insult
identity_attack
sexual_explicit

### Examples
Here are a few examples of comments and their associated toxicity and identity labels. Label values range from 0.0 - 1.0 represented the fraction of raters who believed the label fit the comment.

Comment: i'm a white woman in my late 60's and believe me, they are not too crazy about me either!!
* Toxicity Labels: All 0.0
* Identity Mention Labels: female: 1.0, white: 1.0 (all others 0.0)

Comment: Why would you assume that the nurses in this story were women?
* Toxicity Labels: All 0.0
* Identity Mention Labels: female: 0.8 (all others 0.0)

Comment: Continue to stand strong LGBT community. Yes, indeed, you'll overcome and you have.
* Toxicity Labels: All 0.0
* Identity Mention Labels: homosexual_gay_or_lesbian: 0.8, bisexual: 0.6, transgender: 0.3 (all others 0.0)

In addition to the labels described above, the dataset also provides metadata from Jigsaw's annotation: toxicity_annotator_count and identity_annotator_count, and metadata from Civil Comments: created_date, publication_id, parent_id, article_id, rating, funny, wow, sad, likes, disagree. Civil Comments' label rating is the civility rating Civil Comments users gave the comment.


## References
1. [Online Hate Index (OHI) Research Project, University of California, Berkeley](http://dh.berkeley.edu/projects/online-hate-index-ohi-research-project?utm_source=BCNM+Subscribers&utm_campaign=d5d78bba5e-natasha-schull-oct12_COPY_01&utm_medium=email&utm_term=0_eb59bfff9e-d5d78bba5e-281420185)
2. [Biased models](https://medium.com/the-false-positive/unintended-bias-and-names-of-frequently-targeted-groups-8e0b81f80a23)
3. [Civil comments](https://medium.com/@aja_15265/saying-goodbye-to-civil-comments-41859d3a2b1d)
