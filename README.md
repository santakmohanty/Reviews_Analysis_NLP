# Introduction
## A sentiment analysis on the Health Insurance Reviews off a policy comparison website.

**Here we dont not use API or scraping, we are reading text from saved webpages. IMO, the method that never fails**

For purposed related to speed and ease of processing, we are using 20 pages with 20 reviews each. The model should be linearly scalable fairly easily.

Process-Flow:
We save and read all the files from the directory into a single file. We need codecs library to extract the source code from the html files. The file is a collection of objects, we add a space to seperate them.

We use BeautifulSoup to parse the html files. If we look into the source code of the html files we easily find the associated tags for the review text element in the webpage. As per the rating parameter, directly finding such a tag proved to be difficult, we accept it for the moment and will take care of it during cleaning.

We use re to claenup the extracted string, a bit of playing aroung is needed for this step. For the ratings part we had to use a string search function, although such a procedure is not recomemded for very high volume of data.

Train-Test Split: Usual, normal procedure

Converting into feature-vectors: We need to convert both the train and test strings into feature vectors, this in essense, makes these words machine readable. We craete a sparse matrix using the tf-idf method. We can play around with other methods as long as it produces a sparce matrix.

We use Multinomial Naive Bias to train the model. Again we can test with other models. Ideally we should test with multiple models and compare the results.

To-do:
Try to implement SpaCy in tone detection.
Compare the results with directy availlable libraries for the the same work
Cheers!
