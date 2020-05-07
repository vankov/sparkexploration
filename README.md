# sparkexploration
I couldn't find a how to run a full Spark NLP pipeline in Scala, so created it using PySpark. The problem was that some of the annotators such as Tokenizer were systematically crashing when created by Scala, either when run by sbt or in Spylon. Perhaps I am just doing something wrong but decided not to spend to much time on this and did the pipiline in Python.

There are three notebooks - two Python and one Scala one. The "Python Create TF Graph.ipynb" is used to generate a TF graph of a very simple feed-forward model. "Python Preprocess.ipynb" runs a Spark NLP pipeline on the "AGNews data set fro" new stories text classification dataset, incliduing sentence detection, tokenization, lemmalization, stop words removal, normalization, vectorization and td-idf computation. The dataset is annotated using the pipeline and then stored on the hard drive. 

The Scala notebook loads the prepropcessed dataframe and does text classification using the TF model. To do this, I have added a bunch of Scala classes in the notebook, which is pretty ugly, but I think it works for a start. The model achieves 75% accuracy on the test set which is, of course, a pretty miserable result, but the point here was to show how TF and Scala work together. 
