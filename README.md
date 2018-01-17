<h2>Apparel Recommendation Engine</h2>
<p>The whole project is divided into following steps:
</br>1.Data Acquisition
</br>2.Data Cleaning
</br>3.Text Pre-processing
</br>4.Text-Based Product Recommendation( Bag-of-words, TF-IDF and Word2Vec)
</br>5.Image-Based Product Recommendation 
</br>6.A/B Testing</p>
 <h4> Data Acquisition</h4>
<p> The data is collected from the Amazon site with the help of Product Advertising Key. The dataset consists of around 18k products(apparels) with around
19 features.</p>
<h4> Data Cleaning </h4>
<p>I removed the features which had a lot of missing values and selected only 6 features under consideration for the whole project.
Duplicated values were also removed(i.e. titles which were almost similar to a particular title were removed).</p>
<h4> Text Pre-processing </h4>
<p> The features seleted for the project were: </br> asin(Amazon Standard Identification Number) </br> brand </br> color </br> title</br> product_type_name
</br> medium_image_url</br> formatted_price</p>
<p>Basic Preprocessing steps were the Stopword Removal and Stemming(not helpful here). </p>
<h4>Text-Based Preprocessing  </h4>
<p> I applied Bag-Of-Words model, TF-IDF and IDF model on the dataset to convert the words into the vectors and on the basis of euclidean 
distance between the vectors, I ranked the apparels for the query apparel.</p>
<h5>Word2Vec</h5>
<p>Then I applied Average weighted Word2Vec model with the help of gensims library of python. After it, I applied IDF-weighted Word2Vec Model on the dataset.The order of the techniques on the basis of the quality of recommendation were:</br>
1. IDF-weighted Word2Vec</br>2. Average weighted Word2Vec</br>3. TF-IDF</br>4. IDF</br>5. Bag-Of-Words</p>

<h4>Image Based Recommendation</h4>
<p>I applied the Convolutional Neural Network to extract the features of the image into a one-dimensional vector and appended it into the text-based wordvectors.</p>
<h4>A/B Testing</h4>
I didn't performed this, but this can be one of the best methods to choose the best algorithm for recommendation.

