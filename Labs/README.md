### GCP GitHub 
Repo https://github.com/sandhyaparna/training-data-analyst <br/>
ML Glossary https://developers.google.com/machine-learning/glossary  <br/>
 <br/>
* ML 1.1 Invoking ML APIs: How to open Notebooks, start an instance, clone a repo
  * Github repo https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/CPB100/lab4c/mlapis.ipynb
  * Lab Solution https://www.coursera.org/learn/google-machine-learning/lecture/PVHTl/lab-solution
* ML 1.2 Analyzing data using Datalab (Google Cloud DataLab) and BigQuery: Invoke BigQuery Console, How to use BigQuery within Python Jupyter notebook
  * https://www.coursera.org/learn/google-machine-learning/lecture/Cj3hg/lab-debrief-analyzing-data-using-datalab-and-bigquery   
<br/>

* ML 2.1 Improve Data Quality 
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/launching_into_ml/solutions/improve_data_quality.ipynb
* ML 2.2 Exploratory Data Analysis Using Python and BigQuery
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/launching_into_ml/solutions/python.BQ_explore_data.ipynb
* ML 2.3 Introduction to Linear Regression
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/launching_into_ml/solutions/intro_linear_regression.ipynb 
* ML 2.4 Introduction to Logistic Regression
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/launching_into_ml/solutions/intro_logistic_regression.ipynb  
* ML 2.5 Maintaining Consistency in Training with Repeatable Splitting
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/launching_into_ml/solutions/repeatable_splitting.ipynb
* ML 2.6 Explore and create ML datasets
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/launching_into_ml/solutions/explore_data.ipynb
<br/>

#### Main 
  * tf.data
  * tf.feature_column
  * tf.train.example/tf.train.sequenceexample and TFRecords
  * tfdv 
  * tf
* ML 3.1 Introduction to Tensors and Variables
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/tensors-variables.ipynb
* ML 3.2 Writing Low-Level TensorFlow Code
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/write_low_level_code.ipynb
* ML 3.3 Load CSV, Numpy, and Text data in TensorFlow
 * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/load_diff_filedata.ipynb
 * Using tf.data.Dataset and tf.feature_column
    * Loads csv file stored in a folder directly using tf.data, get_dataset function to import data, show_batch is used to look at few rows of data
    * pack data before passing it into the model
    * https://github.com/tensorflow/docs/blob/master/site/en/r1/guide/feature_columns.md
    * tf.feature_column - standardization/normalization can be done using tf.feature_column.numeric_column
    * create vocab list for categorical variables: tf.feature_column.categorical_column_with_vocabulary_list
* ML 3.4 Loading images Using tf.data.experimental.make_csv_dataset
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/load_images_tf.data.ipynb
* ML 3.5 Introduction to Feature Columns: 
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/feat.cols_tf.data.ipynb
  * tf.feature_column 
    * create a tf.data dataset from a Pandas Dataframe - 
    * several types of feature column
    * tf.feature_column.embedding_column: creates embeddings for the values of a variable
* ML 3.6 TFRecord and tf.Example
  * End to end example with image data (writing to tfrecords, serialization on whole data and reading from tfrecods) https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/tfrecord-tf.example.ipynb
    * tf.train.Example is used to read and data to tfrecord files (tfrecords is a format for storing a sequence of binary records)
    * tf.data is also used to convert to tfrecords (but tf.train.Example is used mostly to convert to tfrecords)
  * tf.train.example & tf.train.sequenceexample: https://medium.com/mostly-ai/tensorflow-records-what-they-are-and-how-to-use-them-c46bc4bbb564
    * tf.train.Example is used when dataset consist of features, where each feature is a list of values of the same type 
    * Data types for tf.Example.Feature: tf.train.BytesList, tf.train.FloatList, and tf.train.Int64List
    * Variables/features of data frame are passed through tf.train.feature, which inturn is passed through tf.train.feature(s), and that is passed through tf.train.Example
    * SerializeToString() is used to serialize output from tf.train.Example
    * tf.train.Example.FromString is used to deserialize 
    * There is no requirement to use tf.Example in TFRecord files. tf.Example is just a method of serializing dictionaries to byte-strings. Lines of text, encoded image data, or serialized tensors (using tf.io.serialize_tensor, and tf.io.parse_tensor when loading).
  * Create tensorflow records from any dataset https://medium.com/nerd-for-tech/how-to-create-tensorflow-tfrecords-out-of-any-dataset-c64c3f98f4f8
* ML 3.7 TensorFlow Dataset API
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/2_dataset_api.ipynb
  * read data using tf.data, transform features, batching and shuffle 
* ML 3.8 Feature Analysis Using TensorFlow Data Validation and Facets
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/adv_tfdv_facets.ipynb
    * TensorFlow Data Validation (TFDV) is one tool you can use to analyze your data to find potential problems in your data, such as missing values and data imbalances - that can lead to Fairness disparities
    * The TFDV tool analyzes training and serving data to compute descriptive statistics, infer a schema, and detect data anomalies. Facets Overview provides a succinct visualization of these statistics for easy browsing. 
    * Jigsaw kaggle civil comments data - Text data is not used in this example
    * tf.keras.utils.get_file is used to import tfrecords formatted file of the comments data
    * tfdv.generate_statistics_from_tfrecord is used to get statistics using TFDV.  The returned value is a DatasetFeatureStatisticsList protocol buffer 
    * tfdv.visualize_statistics(stats) for visualization of the statistics using Facets Overview.
    * for text: TFDV can also compute statistics for semantic domains (e.g., images, text). To enable computation of semantic domain statistics, pass a tfdv.StatsOptions object with enable_semantic_domain_stats set to True to tfdv.generate_statistics_from_tfrecord.Before we train the model,
* ML 3.9 Introducing the Keras Sequential API --- **TAKES CSV FILE AND GENERATES MODEL AND PREDICTIONS USING TENSORFLOW API APPROACH; DEPLOY MODEL TO AI PLATFORM GCP**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/3_keras_sequential_api.ipynb
    * read data using tf.data, transform features, batching and shuffle, create feature_Columns to send the features through keras sequential model
    * when creating batches of data using tf.data, transform features, batching and shuffle; we can use .fit_generator. In fact, when calling .fit the method inspects the data, and if it's a generator (as our dataset is) it will invoke automatically .fit_generator for training.
    * Training of model: fit() works for small data, fit_generator() is for large datasets, .train_on_batch() method is for more fine-grained control over training and accepts only a single batch of data
    * .fit() for training a model for a fixed number of epochs (iterations on a dataset).
    * .fit_generator() for training a model on data yielded batch-by-batch by a generator
    * .train_on_batch() runs a single gradient update on a single batch of data.
* ML 3.10 Basic Introduction to Logistic Regression **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/basic_intro_logistic_regression.ipynb
    * IRIS classification problem
    * Defined loss and gradient functions, created optimizer
    * Use trained model to make predictions on test dataset
* ML 3.11 Advanced Logistic Regression in TensorFlow **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/adv_logistic_reg_TF2.0.ipynb
    * Fraud detection dta
    * class weights to deal with imbalanced data: model.load_weights() is used before model.fit
* ML 3.12 Keras Functional API **Example**
  https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/4_keras_functional_api.ipynb
<br/>

* ML 4.1 Performing basic feature engineering in BQML
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/feature_engineering/solutions/1_bqml_basic_feat_eng.ipynb
* ML 4.2 Performing Basic Feature Engineering in Keras
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/feature_engineering/solutions/3_keras_basic_feat_eng.ipynb
    * Scaling of numeric features in tf.feature_column 
    * Append diff types of columns using feature columns
* Apache Beam and cloud Dataflow
  * https://www.coursera.org/learn/feature-engineering/lecture/BZ9da/beam-and-dataflow
    * Cloud Dataflow is a platform to run data processing pipelines. It is serverless. Dataflow can change the amount of computer resources, the number of servers that will run your pipeline, and do that elastically depending on the amount of data that your pipeline needs to process. 
    * Code for Dataflow is written using Apache Beam. Write code in Apache Beam and deploy the code to cloud Dataflow
    * Apache Beam name comes from a contraction of batch and stream and it supports both
    * Batch data sources comes from cloud storage, BigQuery for example
    * Streaming data source comes from pub/sub
    * Series of steps in pipeline is called transform. Every transform gets a PCollection as input and outputs the result to another PCollection. PCollection does not store all of its data in memory. So PCollection is like a data structure with pointers to where the data flow cluster stores your data.
    * Input --> Transform --> sink (last transform in a pipeline)
    * Running a pipeline requires a runner. It takes pipeline code and executes it
    * A pipeline is a directed graph of steps. beam.pipeline is used to create a pipeline instance. Once it is created, every transform is implemented as an argument to the apply method of the pipeline. Run method is called on the pipeline instance to execute it
    * write method should only be used when working with small data sets that can be processed in a single node, because when dealing with large data, there can be multiple servers trying to write results to the file system and results in file lock contention issue
* ML 4.3 A simple Dataflow pipeline (Python)
  * https://www.coursera.org/learn/feature-engineering/lecture/M6jak/lab-solution-simple-dataflow-pipeline
    * Source code for the pipeline implementation https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/data_analysis/lab2/python/grep.py
    * Source code for the pipeline implementation that was modified to run on the Google Cloud Dataflow platform https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/data_analysis/lab2/python/grepc.py
    * Uses cloud data shell to run the code
* Data pipelines that scale
  * https://www.coursera.org/learn/feature-engineering/lecture/Ru1af/data-pipelines-that-scale
    * beam.map is used for 1:1 relationship. for eg: when we output a len for each word taken as input
    * beam.flatmap is used for non 1:1 relationships, for eg: when we output all vowels for each word as input
    * beam.GroupByKey() is used as shuffle based on a combination of features
    * combine.globally(sum) - for global aggregate operations
    * combine.perKey(sum): for operations based on variables
* ML 4.4 MapReduce in Dataflow
  * https://www.coursera.org/learn/feature-engineering/lecture/zn0dj/lab-solution-mapreduce-in-dataflow
    * source code for the apache beam pipeline https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/data_analysis/lab2/python/is_popular.py
* Cloud Data prep: Exploratory data analysis
  * https://www.coursera.org/learn/feature-engineering/lecture/DKOZG/preprocessing-with-cloud-dataprep
    * Summarize data in BigQuery using SQL. Use Datalab to write sql query and get summarized data set from big query and the visualize the data
    * Cloud Dataprep is a graphical UI to explore data and also compute flows of data transformations
    * Data prep runs a Dataflow job
    * Data prep has data wranglers
* ML 4.5 Computing Time-Windowed Features in Cloud Dataprep
  * https://www.coursera.org/learn/feature-engineering/lecture/6fV0s/lab-intro-computing-time-windowed-features-in-cloud-data
* Tensorflow playground: https://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2&seed=0.63113&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false 
* ML 4.6 Improve Machine Learning model with Feature Engineering
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/feateng/feateng.ipynb
     * Python function: if else statements is used to add sql query to the existing sql query
     * BigQuery to csv using dataflow, run beam pipeline on cloud data flow
* ML 4.7 Performing Advanced Feature Engineering in Keras **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/feature_engineering/solutions/4_keras_adv_feat_eng.ipynb
    * Similar to 3.9
    * Incorporating feature engineering in addition to existing variables: lambda function
    * layer.lambda to apply functions
    * uisng feature engineered variable in keras model
* Tensorflow Transform https://www.coursera.org/learn/feature-engineering/lecture/WNo8c/tensorflow-transform
  * tf transform is a hybrid of Apache beam and tensorflow 
  * for example: if we want to scale inputs by the max & min; we first need to traverse through the entire data set for finding min and max of a variable - this is done using Apache Beam in cloud Data flow). We then use min and max to scale the feature - which is done using tendorflow transform
    * Analysis phase(compute min/max/vocab etc) is executed in Beam while creating the training dataset
    * Transform phase(scale/vocab etc) is executed in TensorFlow during prediction
  * tf.transform provides 2 PTransforms
    * AnalyzeAndTransformDataset(preprocess): Executed in Beam to create the training dataset. Analyze is done here because min and max should be taken only from training dataset
    * TransformDataset: Executed in Beam to create the evaluation dataset
* Analyze phase - only on train data https://www.coursera.org/learn/feature-engineering/lecture/x5L7x/analyze-phase
  * We have to tell beam what data to expect
  * set up a dictionary called raw data schema and add entries for all the string columns i.e. tensorflow datatype
  * Update schema for numeric columns
  * At this step we will have raw data schema that has all the columns in the dataset that will be processed by beam on dataflow, raw data schema is used to create a metadata template
  * Next, run the analyze-and-transform Ptransform on the training dataset to get back pre-process training data and the transform function. 
  * beam.io.read to read train data from big query, beam.filter is used to filter out data that u dont want
  * raw data from above line and metadata template is passed into AnalyzeAndTransformDataset. outcome is transformed dataset (PCollection data format) and a resuable transform function
  * transformed dataset is written out as TFRecords but instead of meta data schema above, we use transformed meta data schema needs to used
* Transform phase: https://www.coursera.org/learn/feature-engineering/lecture/aHO4x/transform-phase
  * Things that we do in preprocess() will get added to the Tensorflow graph, and be executed in Tensorflow during serving
  * preprocess function can use only tensorflow functions
  * on evaluation dataset, transform function that is computed on training data is needed
  * then it is writted to TFRecords
* Support Serving https://www.coursera.org/learn/feature-engineering/lecture/zeghG/supporting-serving
  * build_training_input_fn
* ML 4.8 Exploring tf.transform
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/11_taxifeateng/tftransform.ipynb
</br> 

* ML 5.1 Reviewing Learning Curves
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/art_and_science_of_ml/solutions/learning_rate.ipynb
* ML 5.2 Export data from BigQuery to Google Cloud Storage
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/art_and_science_of_ml/solutions/export_data_from_bq_to_gcs.ipynb
* ML 5.3 Performing Hyperparameter Tuning
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/art_and_science_of_ml/solutions/hyperparameter_tuning.ipynb
* ML 5.4 Build a DNN using the Keras Functional API
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/art_and_science_of_ml/solutions/neural_network.ipynb
* ML 5.5 Training Models at Scale with AI Platform
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/art_and_science_of_ml/solutions/training_models_at_scale.ipynb
* ML 5.6 Introducing the Keras Functional API
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/introduction_to_tensorflow/solutions/4_keras_functional_api.ipynb
</br>

* AML 1.1 Explore the dataset
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/06_structured/1_explore.ipynb
* AML 1.2 Create a sample dataset
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/end_to_end_ml/solutions/sample_babyweight.ipynb
* AML 1.3 Create TensorFlow model **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/end_to_end_ml/solutions/keras_dnn_babyweight.ipynb
* AML 1.4 Preprocessing using Cloud Dataflow
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/end_to_end_ml/solutions/preproc.ipynb
* AML 1.5 Training on Cloud AI Platform
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/06_structured/5_train.ipynb
* AML 1.6 Deploying and predicting with Cloud AI Platform
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/end_to_end_ml/solutions/deploy_keras_ai_platform_babyweight.ipynb
</br>

* AML 2.1 Predict Babyweight with TensorFlow using AI Platform
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/blogs/babyweight/train_deploy.ipynb
* AML 2.2 Serving ML Predictions in batch and real-time
  * https://www.coursera.org/learn/gcp-production-ml-systems/lecture/ikJI4/lab-solution-serving-ml-predictions-in-batch-and-real-time
</br>

* AML 3.1 Linear Models for Image Classification
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/08_image/mnist_linear.ipynb
* AML 3.2 DNN Models for Image Classification  &  3.3 DNN with Dropout for Image Classification  &  3.4 CNNs for Image Classification
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/image_classification/solutions/2_mnist_models.ipynb
* AML 3.5 Implementing image augmentation
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/08_image/flowers_fromscratch.ipynb
* AML 3.6 Train a Neural Network Model to Classify Images
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/image_classification/solutions/5_fashion_mnist_class.ipynb
* AML 3.7 Training with Pre-built ML Models using Cloud Vision API and AutoML
  * https://www.coursera.org/learn/image-understanding-tensorflow-gcp/lecture/GWMnr/lab-solution-training-with-pre-built-ml-models-using-cloud-vision-api-and-automl
</br>

* AML 4.1 Using linear models for sequences & 4.2 Using DNNs for sequences & 4.3 Using CNNs for sequences & 4.4 Time series prediction: end-to-end (rnn) & 4.5 Time series prediction: end-to-end (rnn2)
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/09_sequence/sinewaves.ipynb
* AML 4.6 Time Series Prediction - Temperature from Weather Data
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/09_sequence/temperatures.ipynb
* AML 4.7 Text Classification using TensorFlow/Keras on Cloud AI Platform **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/09_sequence/text_classification.ipynb
* AML 4.8 Evaluating a pre-trained embedding from TensorFlow Hub **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/09_sequence/reusable-embeddings.ipynb
* AML 4.9 Keras for Text Classification using AI Platform **Example**
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/text_classification/solutions/keras_for_text_classification.ipynb
* AML 4.10 Getting Started with Dialogflow
  * https://www.coursera.org/learn/sequence-models-tensorflow-gcp/lecture/TIeW2/lab-solution-dialogflow
</br>

* AML 5. Create a Content-Based Recommendation System
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/10_recommend/content_based_by_hand.ipynb
* AML 5. Create a Content-Based Recommendation System Using Neural Networks
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/10_recommend/content_based_preproc.ipynb
* AML 5. Collaborative filtering on the MovieLense Dataset
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/recommendation_systems/solutions/als_bqml.ipynb
* AML 5. Hybrid Recommendations with the MovieLens Dataset
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive2/recommendation_systems/solutions/als_bqml_hybrid.ipynb
* AML 5. Recommendation Systems with TensorFlow
  * https://github.com/GoogleCloudPlatform/training-data-analyst/blob/master/courses/machine_learning/deepdive/10_recommend/cf_softmax_model/target/cfmodel_softmax_model_target.ipynb
</br>

Rent-a-VM to Process Earthquake Data https://www.coursera.org/learn/google-machine-learning/lecture/Qonu0/lab-debrief  <br/>
  Qwiklabs https://www.qwiklabs.com/focuses/1846?catalog_rank=%7B%22rank%22%3A1%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=1953907  <br/>
   <br/>


Activate datalab
* In Google cloud platform, open cloud shell - datalab create vminstancename --zone us-central1-a
* To open instance that has already been created - datalab connect vminstancename

In the datalab clone a github repository: <br/>
%bash <br/>
git clone https://github.com/GoogleCloudPlatform/training-data-analyst <br/>
rm -rf training-data-analyst/.git <br/>



Using Cloud DataPrep - join data, create new features; save data to BigQuery-Perform Aggregation; Use DataLab to visualize data
https://www.qwiklabs.com/focuses/610?locale=en&parent=catalog

Feature Creation https://github.com/sandhyaparna/training-data-analyst/blob/master/courses/machine_learning/feateng/feateng.ipynb <br/>

Tf transform https://github.com/sandhyaparna/training-data-analyst/blob/master/courses/machine_learning/feateng/tftransform.ipynb  <br/>
