<h1 align="center">Emotion detection in tweets using Bidirectional LSTM
with CNN</h1>
<h3>Abstract</h3>
<p>
Emotion detection is one of the branches of text analysis. It deals with detection of sentiment
analysis and extraction of emotions. With increasing involvement of human beings on social
media sites it has become evident to recognise emotions involved in tweets to avoid abusive
tweets. People nowadays use social media sites for abusive tweets. If we can detect such
emotions then we can prevent the people from posting them on social media. Since emotions
play an important part in human life, therefore tweets and messages will continue to have
such emotions. But we can detect use of machine learning and NLP for detection of any tweet
which shows anger and the user can be asked to modify it into a normal sentence.
Exaggerated emotional tweets can sometimes be very harmful as they can insight riots, or we
can stop any suicidal message having emotions of fear sadness to prevent suicide etc. In the
current project, the aim is to detect emotions in tweets such as love, sadness, fear, anger and
happiness using Bidirectional LSTM with CNN.  
</p>
  
<h3>Method</h3>
<h4>Dataset</h4>
<p>For emotion classification in tweets we are using 
<a href="https://github.com/indobenchmark/indonlu">IndoNLU</a>. <a href="https://github.com/indobenchmark/indonlu">IndoNLU</a> is a collection of
Natural Language Understanding (NLU) resources from Bahasa Indonesia with 12 downstream
tasks. They provide the code to reproduce the results and large pre-trained models (​ IndoBERT
and ​ IndoBERT-lite​ ) trained with around 4 billion word corpus (​ Indo4B​ ), more than 20 GB
of text data. This project was initially started by a joint collaboration between universities and
industry, such as Institut Teknologi Bandung, Universitas Multimedia Nusantara, The Hong
Kong University of Science and Technology, Universitas Indonesia, Gojek, and Prosa.AI.</p>

<p>The tweets data csv files are available in the <a href="https://github.com/indobenchmark/indonlu/tree/master/dataset/emot_emotion-twitter">IndoNLU/emot_emotion-twitter<a> repository. The
repository proves two csvs train_preprocess.csv and valid_preprocess.csv. The below table [1]
shows the gist of the dataset. The csv consists of two columns “label” and “text”. The “label”
consists of emotions values represented by the tweets in the text column. Both training and
validation dataset consists of 3521 twitter text. Figure 1. shows the bar graph with counts of
the tweets with different counts of emotion labels. The distribution of ‘anger’, ‘sadness’ and
‘happy’ emotions is the maximum in the corpus. Figure 2 and Figure 3 shows the univariate
distribution plot. It is used basically for a univariant set of observations and visualizes it
through a histogram i.e. only one observation and hence we choose one particular column of
the dataset. Figure 2 depicts the distribution showing the length of the tweets in the corpus.
While Figure 3 shows the distribution showing the word count of the tweets in the corpus.
 </p>
  
 <figure style="text-align: center;">
    <img src='Screenshot from 2020-11-30 21-05-21.png' />
    <figcaption>Table 1. Table shows train dataset with label and text column.</figcaption>
</figure>

 <figure style="text-align: center;">
    <img src='Distrubution_emotions.png' />
    <figcaption>Figure 1. Bar graph showing the counts of the tweets with different emotions in the corpus</figcaption>
</figure>

 <figure style="text-align: center;">
    <img src='Distrubution_of_legth_of_tweets.png' />
    <figcaption>Figure 2. Distribution showing the length of the tweets in the corpus</figcaption>
</figure>

 <figure style="text-align: center;">
    <img src='Distribution_of_word_count_tweets.png' />
    <figcaption>Figure 3. Distribution showing the word count of the tweets in the corpus</figcaption>
</figure>

<h3>Results</h3>
<p>We trained the model for around 20 epochs and the model is saved as model_weights.h5 file.
This model is then used to do prediction on the validation data set. Figure 5 shows the
confusion matrix with prediction accuracy for each class. For tweets related to ‘anger’ and
love the model shows the highest accuracy with 71 % and 67 % respectively.</p>

 <figure style="text-align: center;">
    <img src='Confusion_matrix.png' />
    <figcaption>Figure 4. Confusion matrix for the prediction results</figcaption>
</figure>

<Br>
<table>
  <tr>
    <th>Statistic</th>
    <th>Anger</th>
    <th>Fear</th>
    <th>Happy</th>
    <th>Love</th>
    <th>Sadness</th>
  </tr>
  <tr>
    <th>Precision</th>
    <th>0.6</th>
    <th>0.76</th>
    <th>0.61</th>
    <th>0.705</th>
    <th>0.38</th>
  </tr>
  <tr>
    <th>Recall</th>
    <th>0.71</th>
    <th>0.523</th>
    <th>0.43</th>
    <th>0.672</th>
    <th>0.51</th>
  </tr>
  <tr>
    <th>F-score</th>
    <th>0.65</th>
    <th>0.618</th>
    <th>0.51</th>
    <th>0.688</th>
    <th>0.43</th>
  </tr>
  <tr>
    <th>Support</th>
    <th>110</th>
    <th>65</th>
    <th>102</th>
    <th>64</th>
    <th>99</th>
  </tr>
  
</table>
Table 2. Table shows precision, recall, fscore and support value calculated for different emotions with LSTM
CNN model trained.


<h3>Appendix</h3>
<h2>Instructions to run the code<h2>
<p>1. Extract the code folder</p>
<p>2. Install the requirements for the code mentioned in requirement.txt file by using the
below command
<b>pip install -r requirements.txt<b></p>
<p>3. Run the jupyter notebook ‘Emotion detection in tweets using Bidirectional LSTM
with CNN.ipynb’ file inside the ‘notebooks’ folder.</p>
<p>4. This notebook contains all steps to do exploratory data analysis, model training and
prediction on the datasets.</p>
<p>5. Folder name ‘datasets’ contains the train_preprocess.csv and valid_preprocess.csv.</p>
<p>6. Folder name ‘models’ contains the saved weights of the trained model in .h5 format
after training.</p>
