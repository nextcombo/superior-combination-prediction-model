# Superior Combination Prediction Model!

CEEMDAN + Combination Prediction Model (BiGRU-GlobalAttention + XGBoost)
This includes power transformer data, as well as the dataset and label sets that have been generated and preprocessed using CEEMDAN decomposition. The corresponding code can be run, along with examples of CEEMDAN decomposition.
The BiGRU-GlobalAttention + XGBoost model has smaller MSE and MAE, showing significant improvement.
The code for data preprocessing with CEEMDAN, as well as complete BiGRU-GlobalAttention prediction code, XGBoost prediction model code, and visualization code are included.
Environment: Python 3.9
This paper is a reproduction and improvement of the reference literature:
Innovation 1: Optimizes the GRU based on attention mechanism into a bidirectional recurrent neural network based on global attention mechanism Global-Attention.
Innovation 2: Divides the components after time series decomposition by sample entropy calculation, then separately uses the BiGRU-GlobalAttention model and XGBoost model for combination prediction to achieve precise prediction.
Preface
This paper introduces a method of comprehensive application of the complete set empirical mode decomposition CEEMDAN and combination prediction model (BiGRU-GlobalAttention + XGBoost) to improve the prediction performance of time series data. The core of this method is to use the CEEMDAN algorithm to decompose the time series, then use the BiGRU-GlobalAttention model and XGBoost model to model the decomposed data, and finally combine the results of both models through an integrated method.
Detailed introduction to the power transformer dataset can be found in the following article:
Power Transformer Dataset Introduction and Preprocessing
1. Data Decomposition and Visualization of CEEMDAN for Power Transformers
1.1 Import data
1.2 CEEMDAN Decomposition
Based on the decomposition results, CEEMDAN has been divided into a total of 11 components. Subsequently, the sample entropy values for each component were calculated to analyze. Sample entropy is a method used to measure the complexity of sequences, which can be evaluated by calculating the uncertainty within the sequence. The higher the sample entropy, the greater the complexity of the sequence.
We roughly use the first six high-sample entropy complex components as the input for the BiGRU-GlobalAttention model for prediction, and the last five low-sample entropy simple components as the input for the XGBoost model for prediction.
2. Data Set Creation and Preprocessing
2.1 Dataset division
\tDivide the training set and test set into 9:1 ratio, then further divide the components data into 6:5 ratio.\tSet the sliding window size to 7, create the dataset.
\t  
Save data in batches for predictions by different models.
\t  
3. Combination Prediction Model Based on CEEMDAN
\t3.1 Define the BiGRU-GlobalAttention network model
\t  
3.2 Set parameters and train the model
50 epochs, MSE is 0.001179, the prediction effect of BiGRU-GlobalAttention is significant. The model can fully extract the temporal and spatial features of time series, has a fast convergence speed, superior performance, high prediction accuracy, and further improve the model's predictive performance by appropriately adjusting the model parameters.
\tNote: Adjust parameters.
\tIt is appropriate to increase the number of BiGRU layers and the dimensionality of hidden layers, and fine-tune the learning rate.
Adjust the number of attention dimensions, increase more epochs (note to prevent overfitting)
\tThe sliding window length can be changed (set the appropriate window length).
Save the training results and prediction data to be combined with the results of the subsequent XGBoost model.
4 Model Prediction Based on XGBoost
\tThe tutorial for the traditional machine learning model XGBoost is as follows:
Data loading, training data and test data grouping, 5 components, split into 5 datasets.
\tSave the predicted data, and other components of prediction are consistent with the above process, retain the final model results.
5 Results Visualization and Model Evaluation
\t5.1 Visualization of component prediction results
5.2 Visualization of Combination Predictions
5.3 Model Evaluation
The results of component prediction show that the first six complex components have a good fitting effect under the BiGRU-GlobalAttention prediction model, while the last five simple components have a particularly good fitting degree under the XGBoost model's prediction, significantly enhancing the combined prediction effect!
\t  
\n        \n  
Previously Featured Content:
Time Series Forecasting: Analysis and comparison of LSTM, ARIMA, Holt-Winters, SARIMA models
Wind Speed Prediction (Part 1) Data Set Introduction and Preprocessing
Wind Speed Prediction (II) EMD-LSTM Model Based on Pytorch
Wind Speed Prediction (III) EMD-LSTM-Attention Model
Wind Speed Prediction (IV) EMD-Transformer Model Based on Pytorch
Wind Speed Prediction (5) EMD-CNN-LSTM Model Based on Pytorch
Wind Speed Prediction (VI) - EMD-CNN-GRU Parallel Model Based on Pytorch
CEEMDAN + Combination Forecasting Model (BiLSTM-Attention + ARIMA)
CEEMDAN + Combination Forecasting Model (CNN-LSTM + ARIMA)
CEEMDAN + Combination Forecasting Model (Transformer - BiLSTM + ARIMA)
CEEMDAN + Combination Forecasting Model (CNN-Transformer + ARIMA)
Multi-feature Variable Sequence Prediction (I) - CNN-LSTM Wind Speed Prediction Model
Multi-feature Variable Sequence Prediction (II) - CNN-LSTM-Attention Wind Speed Prediction Model
Multi-feature Variable Sequence Prediction (III) - CNN-Transformer Wind Speed Prediction Model
Multi-feature Variable Sequence Prediction (IV) - Transformer-BiLSTM Wind Speed Prediction Model
Multi-feature Variable Sequence Prediction (V) CEEMDAN+CNN-LSTM Wind Speed Prediction Model
Multi-feature Variable Sequence Prediction (VI) CEEMDAN+CNN-Transformer Wind Speed Prediction Model
Predictive Model Based on the Optimized Algorithm of Sparrows SSA-CEEMDAN-BiLSTM-Attention
CEEMDAN-Transformer-BiGRU Prediction Model Based on Optimized Algorithm SSA for Sparrows
Super Predictive Model: Secondary Decomposition-Combination Prediction
Multi-feature variable sequence prediction (7) CEEMDAN+Transformer-BiLSTM prediction model
Multi-feature variable sequence prediction (8) CEEMDAN-SSA-BiLSTM prediction model based on the Sparrow Optimization Algorithm
Multi-feature variable sequence prediction (11) TCN-GRU prediction model based on Pytorch
VMD + CEEMDAN secondary decomposition, CNN-LSTM prediction model
VMD + CEEMDAN secondary decomposition, CNN-Transformer prediction model
VMD + CEEMDAN 2nd Decomposition, Transformer-BiGRU Prediction Model
Predictive Model Based on the Optimized Algorithm of Sparrows - Code All-in-One
Introduction to the Power Transformer Dataset and Preprocessing
SCI 1 Zone: High Innovation Forecast Model!

## Images

[ | Strong combination prediction model!](01.png)
[ | Strong combination prediction model!](02.png)
[ | Strong combination prediction model!](03.png)
[ | Strong combination prediction model!](04.png)
[ | Strong combination prediction model!](05.png)
[ | Strong combination prediction model!](06.png)
[ | Strong combination prediction model!](07.png)
[ | Strong combination prediction model!](08.png)
[ | Strong combination prediction model!](09.png)
[ | Strong combination prediction model!](10.png)
[ | Strong combination prediction model!](11.png)
[ | Strong combination prediction model!](12.png)
[ | Strong combination prediction model!](13.png)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
