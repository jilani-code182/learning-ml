# Introduction to ML

## What is ML ?

ML  is way of teaching computer to learn from data, just like we learn from our experience (activity).


Eg: 
- Youtube recomendation system
- Self driving car
- Face unlock feature etc. 

## Traditional programming vs ML 

### In traditional programming:

| Program + Input → Output |
|---|
- Need manual logic/code writing

### In ML:

|Input + Output → Pattern|
|---|

- It learns patterns automatically
- No need to define the logic

## AI vs ML vs DL 

### AI : Mimic human intelligence 

Eg:
- Chatbots like ChatGPT, Gemini and Claude 
- Movie recommendation in Netflix and YT 
- Voice assistant like Alexa or Siri

### ML : Learn from data

Eg:

- Spam Email Detection :

  In spam email detetion, the algorithm read past spam emails, find a patten in them then recognize the new spam email.

- Word Recommendation While Typing : 
 
  In this, the algorithm analyze the typying habit of the user and then recommend the next word based on it.

- Fraud Detection in Banking system : 

  In this , the algorithm analyze large amount of fraud happened in the past, find a common patten in them and then catch the new frauds.

### DL : Use neural network (inspired by actual structure of human brain)

Eg: 

- Face Recognition System : 

  Face recognization system uses deep neural netwrok to recognize and authenticate a face. It uses Convolution Neural Network (CNN).

 
- Real Time Language Translation : 

  Real time language translation tool processes speech through neural network to convert conversation smoothly between languages. 

- Self Driving Cars : 

  Self driving cars processes sensor informations using neural network to make quick decision while driving. 


## Types of ML 

1. Supervised Learning 
2. Unsupervised Learning 
3. Reinforcement Learning 

### 1. Supervised Learning : 

  In supervied learning, the machines learns from the labeled data. The labeled data is the correct target answer to the corresponding input. In this, we give both input and output. Based on the given inpput and output, the machine learns the patterns and predict the correct output for the new input given. 

  It is like a teacher teaching a student.  


>NOTE: 
>- In this the input can be many but the output should be only one like house price, object name, whether an email is spam or not. 
>- 99% of learning are supervised learning. 

  For eg: 

  - Spam detection in email 

    In spam detection, the model are given the large set of data already labeled as spam or not spam. It learns the pattern form there and recognize the new spams.  

    
  - House price prediction 

    The model analyses house features like size, no. of rooms, locations etc. along with its sales prices. Then it pridict the house price based on it. 

  - Object detection in photos or videos 

    In this, many images are feed with labels, the model learns from the picture and its label and then identify the object in the new picture. 


### 2. Unsupervised Learning: 

In unsupervised learning, a large amout of input is given and the model needs to find the hidden pattern in it. There is not output/label given here. 

Some techniques that is used to find patten in the given inputs are Clustering and Association.

> NOTE:
>
> Unsupervised learning is used with supervisesd learning to train models. 

For eg: 

- Searching Anything on Google:

  When you search anything on google, you only get that result that is related to the search. Here the similar items are clustered together and only that cluster is shown as an output. 

- Youtube/Netflix Reccomendation : 

  In this, the algorithm group the similar type of videos or movies based on the watch history and reccomend the new movies or videos. 

### 3. Reinforcement Learning 

In this the models learn on the basis of reward and punishment. 

For eg: 

- Teaching a Machine to Play a Game like Chess or Flappy Bird : 

  The model will become out or loose the point if it take wrong move. It will gain points or win the game if it take the right move. So, based on this reward and punishment, the machine learn to play a game.

- Training a Car for Self Driving : 

  There is a positive and negative points for good and bad behaviour. When the model drives correclty then it is rewarded with positive points and when it make mistake then it is punished with negative points. These points are determined by a mathmatical function inside the model. The good behaviour is repeated until the model becomes perfect in driving. This is how reinforcement learning occur.



## Steps to Make a ML Model

1. Define the Problem
2. Data Collection
3. Explotary Data Analysis (EDA)
4. Data Cleaning 
5. Feature Selection
6. Splitting the Dataset 
7. Model Selection 
8. Model Training 
9. Model Evaluation 
10. Hyperparameter Tuning 
11. Model Testing. 

