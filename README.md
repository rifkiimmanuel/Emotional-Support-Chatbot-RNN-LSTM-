# Emotional-Support-Chatbot-RNN-LSTM



This is a chatbot utilizing deep learning approaches, the interaction is more efficient, adaptable, and user-friendly.


Libraries used:  
Tensorflow, numpy, pandas, skelarn, json, string, and keras.


METHODOLOGY

1. DATA SET ACQUISITION:
In this project, using a dataset from Kaggle, the dataset is in the form of a .json file where there are tags and patterns, this dataset contains a collection of questions and answers based on various topics such as emotions, psychology, sports, normal day-to-day conversations etc.

2. Preprocessing 
- Reading and loading data: The code reads data from the JSON file 'intents.json' which contains a list of conversation patterns and their associated tags.
- Collecting patterns, tags and responses: The JSON data is read and the corresponding patterns, tags and responses are put into a separate list.
= DataFrame construction: The data is then organized into a DataFrame using pandas.
- Text normalization: The text in the 'patterns' column is normalized by removing punctuation and converting letters to lowercase.

3. Tokenization and and vectorization
After normalization, the text is converted into a sequence of tokens using TensorFlow's Tokenizer. In this project, the text is tokenized using the TensorFlow/Hard Tokenizer. This Tokenizer is responsible for converting the text into a sequence of numeric tokens, where each word or token in the text is represented with a unique integer. After the text is tokenized, the Tokenizer generates a sequence of numeric tokens for each text, done using the pad_sequences function of TensorFlow/Keras.


4. Label processing and one hot encoder 
Tags that are output are encoded using LabelEncoder from scikit-learn. Then, the encoded output is converted into a one-hot vector.


5. CREATION OF LSTM MODEL:
LSTM are a special kind of RNN which are capable of learning long-term dependencies, Artificial neural network models with Embedding, LSTM, Flatten, and Dense layers are built using TensorFlow/Hard. The model was trained using the sparse categorical crossentropy method as a loss function and Adam's optimizer.

5. Train and testing data
In testing using data from json that already has tags and patterns, Once the model is trained, a loop is created to receive input from the user, perform similar preprocessing on that input, and then predict the corresponding tags using the trained model. Once the tag is predicted, the corresponding response is randomly selected from the responses associated with that tag.


6. Prediction 
Finally,  the user can input one's questions and converse with the chatbot. The results obtained are satisfactory according to review analysis.




The flowchart: 
![Flowchart (3)](https://github.com/rifkiimmanuel/Emotional-Support-Chatbot-RNN-LSTM-/assets/118416978/6e345328-e273-4fad-a255-c0811d4688b2)





Result : 
With 1000 epoch, the final accuracy is 0.9957
![image](https://github.com/rifkiimmanuel/Emotional-Support-Chatbot-RNN-LSTM-/assets/118416978/c3eba076-a0c5-4e1a-a62f-07fba04c334e)
![image](https://github.com/rifkiimmanuel/Emotional-Support-Chatbot-RNN-LSTM-/assets/118416978/52a8357d-f5a8-4740-91e2-7bfc1a66f4cd)


