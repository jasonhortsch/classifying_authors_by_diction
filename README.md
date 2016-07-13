# Classifying Authors by Diction

## DSCI-6003 (Machine Learning I) and DSCI-6004 (Natural Language Processing) Final Project December 2015

### Summary

This project had to incorporate techniques learned in our Machine Learning I and Natural Language Processing classes. Being an avid reader and former writer, I wanted to explore the machine learning potential for identifying authors by their diction. I used books from three writers whose works were freely available on Project Gutenberg – Jane Austen, Charles Dickens, and Sir Arthur Conan Doyle. 

I split each book into chunks (in one iteration each chunk was 5000 words, and in another iteration each chunk was a native chapter from the book), and used a TF-IDF vectorizer on each chunk. I then trained and tested an SVM classifier to differentiate between both two and three books. Results were mixed, in the sense that the classifier performed almost literally perfectly.

My suspicion is that the SVM simply ‘learned’ to split on character names and proper nouns. This subsequently means that my model was too specialized, and as a result would have little use in a generalized sense. However, it did accomplish what it was designed to do.

### Technologies Used

* Scikit-Learn
* The NLTK Package
* Pandas
* SVMs

### Ideas for Improvement

This was my first true data science project. As such, it is full of decisions and techniques I would change. I am proud of what I accomplished at the time, but now this project mostly serves as a reminder of how far I’ve progressed. In terms of coding, I would refactor redundant code and make use of helper functions.

In terms of the model, to start with, I would test out other algorithms besides simply an SVM. Next, I would experiment with using an NER (Named Entity Recognizer), such as [Standford's](http://nlp.stanford.edu/software/CRF-NER.shtml), to attempt to remove proper nouns from the texts. Ideally, this could potentially force the classifier to make splits based more on diction, rather than latching onto different character names.

Finally, I would also like to try using a parts of speech tagger, and incorporating parts of speech counts. For example, perhaps Author X uses far more prepositions than Author Y, and that is a good indicator for classifying a segment of text as one author or the other.
