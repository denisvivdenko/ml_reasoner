# Idea:

Inspired by the course "Introduction to ML stategy" from Andrew Ng. The idea is to gather all the advices into one knowledge base and then use them to make reasoning for next best iteration. I want it to be a framework which will be used for model iteration.

# Functionality:

- [ ] Keep track of progress
- [ ] Keep track of metrics
- [ ] Set up optimizing and satisficing metrics
- [ ] Split dataset (train/train-dev/dev/test sets)
- [ ] Error analysis
- [ ] Detect variance/bias/data mismatch
- [ ] Suggest best strategy


# Rules:

- [ ] Implement basic recipe for Neural Networks (because for classical ML algorithms "variance/bias tradeoff" works differently, for example, RF can be used to reduce variance without affecting bias)

    Rules:

    - IF high bias THEN train bigger network
    - IF high bias THEN train longer
    - IF high bias THEN try different NN architecture

    - IF high variance THEN need more data
    - IF high variance THEN need regularization
    - IF high variance THEN try different NN architecture

- [ ] Detect variance/bias...

    Rules:
    
    - IF human level error << training error THEN high avoidable bias
    - IF trainig error << training-dev error THEN high variance
    - IF training-dev error << or >>  dev set error THEN data mismatch
    - IF test set error >> dev set error THEN overfitting to dev set

- [ ] Detect errors

    Rules:

    - IF dev/test sets have data mismatch THEN error: "dev and test sets cannot have different distributions"

# Diagrams:

![idea](diagrams/automl_diagram.png)