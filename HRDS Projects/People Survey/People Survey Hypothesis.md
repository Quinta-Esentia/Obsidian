

1. Collaboration (w/ STIP)
2. Action Taking
3. 
4. 

# To Do

## Data Prep
- [ ] Span & Layers from Joe
- [ ] STIP from Kenny
- [ ] Run Reyash NBs


# Hypotheses to Test

- Length of comments vs sentiment
- Is there a low eSat when people comment more (comment response rates)

## Updates for meeting
- Have gone through code for stitching together data sources, aiming to have most of that complete this week. Reaching out to Joe Matthew (DM team) re. spans & layers data.
- Next steps will be engineering features and preparing hypotheses. 

## Questions for meeting with Nicole & Hannah

### Q - Leader shadow hypothesis
Looking through notes and saw "Leader shadow hypothesis" - is this concerning spans and layers?
i.e. size of team / number of delegates under a leader, how far down the org hierarchy etc.)
### A


### Q - Rockstars data
What rockstars data will be avaliable? Do we want to assess if there is enough data to test the Rockstar vs Recognition and other rockstar related hypotheses?
### A


### Q - Are we interested in doing a BERT based sentiment analysis to assess comment hypotheses?
* We have an offline model that is relatively good at labelling text with a sentiment.
* Not all that insightful when run on all comments for a question on a survey (we **can** look at sentiment trends over time) - this is similar to the sentiment Glint gives.
* Best run on a filtered subset of comments, relating to a theme. Can use keywords to extract these comments and then run them through sentiment. eg. comments relating to Rockstars etc. 
### A

### Q - What level of org can we get with survey comments?
For purposes of joining with eSat and other survey scores. 
### A