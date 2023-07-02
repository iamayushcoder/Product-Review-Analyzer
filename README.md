#                                                 Review Rocket  

## 📝Table of Contents  

####  -Introduction  
#### -Problem Statement
#### -How Our Project Aligns with the Following Hackathon Tracks
#### -Designing and Training the Model
#### -API Documentation
#### -How to Run
#### -Dependencies   


## 💡Introduction  

Review Rocket is an innovative API endpoint powered by advanced language models (LLMs) that provides comprehensive analysis of product reviews and sentiment data. This powerful tool offers valuable insights into product quality, customer satisfaction, and opportunities for improvement. By leveraging Review Rocket, businesses can gain a deep understanding of customer feedback and make informed, data-driven decisions.

## 🔍Problem Statement  

Imagine running a business and putting your heart and soul into delivering exceptional products. However, without a clear understanding of what your customers truly think, it's challenging to make the right decisions to improve your offerings. Traditional manual methods of analyzing reviews are time-consuming, inefficient, and often miss the mark. That's where Review Rocket comes in to save the day! It acts as a lifeline, helping businesses navigate through the overwhelming sea of reviews and guiding them towards the shores of customer satisfaction. With Review Rocket, you can extract valuable insights from product reviews and make judicious business decisions.

## 🚀How Our Project Aligns with the Following Hackathon Tracks  

Our project, Review Rocket, aligns with the Mercor's Startup Gateway Hackathon tracks in the following ways:

-LLM API Endpoint: Review Rocket is an API endpoint that integrates an advanced language model (LLM), specifically the DistilBERT model, to provide sentiment analysis of product reviews. By leveraging the power of LLMs, Review Rocket offers an exciting solution to a real-world problem, which is extracting insights from customer feedback. It showcases our creativity in utilizing LLMs to address customer needs and improve products.  

## 🛠️Designing and Training the Model  

The ML code behind Review Rocket consists of a sentiment classification model trained on customer reviews using the highly effective DistilBERT model. Here's an overview of the steps involved:

#### 1. Loading and Preprocessing the Dataset: 
The code loads a dataset containing customer reviews from a CSV file. It then splits the dataset into training and validation sets, while extracting the corresponding sentiment labels.

#### 2. Tokenizing and Encoding:   
The DistilBERT tokenizer is utilized to tokenize and encode the text data, ensuring efficient processing. The labels are also encoded accordingly.

#### 3.Creating PyTorch Datasets: 
PyTorch datasets are created using the encoded input and label data, setting the stage for model training.

#### 4. Loading the Pre-trained Model: 
The pre-trained DistilBERT model for sequence classification, specifically tailored for sentiment analysis, is loaded into memory.

#### 5. Defining the Optimizer:
Review Rocket employs the AdamW optimizer, a highly effective choice for updating the model's parameters during the training process.

#### 6. Training the Model: 
The model undergoes rigorous training, with the training loop iterating over batches of data, performing forward and backward passes, and updating the model's parameters using the optimizer.

## 📃API Documentation  

The Review Rocket API leverages the powerful FastAPI framework to deploy the sentiment classification model as a RESTful API. Let's dive into how it works:

#### 1. FastAPI Setup:
The FastAPI module is imported, and an instance of the FastAPI class is created, establishing the foundation for the API.

#### 2. Request and Response Models: 
Two Pydantic models, namely ReviewItem and SentimentPrediction, are defined. ReviewItem represents the request body, including a single field called "Review" to input the text for sentiment analysis. SentimentPrediction represents the response body, encapsulating the predicted sentiment with a single field called "sentiment."

#### 3. Model Loading:
The pre-trained sentiment classification model is loaded into memory using the appropriate functions, ensuring seamless access to the model during API operations.

#### 4. Prediction Endpoint: 
An API endpoint is defined using the @app.post decorator, accessible through the /predict route. It is specifically designed to handle POST requests for sentiment prediction.

#### 5. Prediction Function: 
Within the prediction endpoint, the input review text is tokenized using the pre-trained tokenizer. The tokenized input is then passed through the loaded model, extracting the predicted sentiment.

#### 6. Response: 
The predicted sentiment is wrapped in a SentimentPrediction object and returned as the API response, providing businesses with immediate access to valuable insights.

## 💨How to Run 
To harness the power of Review Rocket, follow these simple steps:

1.Send a POST request to the /predict route, providing a JSON payload that includes the review text.

2.The API will process the request and return a JSON response containing the predicted sentiment.

Please ensure that you update the model path (model_path) in the API code to reflect the correct file path of your trained model.

## 📖Dependencies 
Review Rocket relies on the following dependencies:  

-FastAPI  
-Pedantic  
-Torch  
-Transformers  
-Pickle    


Join the Review Rocket revolution today and unlock the potential of customer feedback for your business. Say goodbye to uncertainty and embrace the power of data-driven decision-making. Together, let's reach for the stars with Review Rocket!
