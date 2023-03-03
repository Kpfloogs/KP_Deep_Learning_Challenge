# Neural Network Model Report

## Project Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With my knowledge of machine learning and neural networks, I’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, I have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 

## Results

### Preprocessing
- Dropped columns "EIN" and "NAME" to reduce noise
- Target Variable: Column "IS_SUCCESSFUL"
- Feature Variables: All Columns

### Compiling, Training, and Evaluating the Model
Initially the model was constructed as follows: 
I chose these parameters because the starter code hinted this is a good place to start. 
![image](https://user-images.githubusercontent.com/110507463/222810491-800226c8-3948-4f43-8b3c-5bdeeddb6daa.png)

I was not able to achieve the target model performance. In order to increase model performance I optimized the following:

- Attempt 1: adding a third hidden layer at 10 nuerons 

![image](https://user-images.githubusercontent.com/110507463/222811272-2ffdd96b-332a-4276-af16-3e8226c9b57d.png)

- Attempt 2: Changed the second hidden layer action function to "tanh"

![image](https://user-images.githubusercontent.com/110507463/222811498-cefd82ab-b656-4c7a-97f9-35eab906dd97.png)

- Attempt 3: Dropped more columns to reduce noise. Columns dropped = "EIN", "NAME", "SPECIAL_CONSIDERATIONS", and "AFFILIATION"

![image](https://user-images.githubusercontent.com/110507463/222811980-3ee202bb-88cd-49bc-9733-9da5b6556713.png)

### Summary
I was not able to achieve the targeted model performance. Out of all four models tested, the results are as below:
- ![image](https://user-images.githubusercontent.com/110507463/222812381-e8d28194-4b1a-4635-a788-976e6668d64f.png)
- ![image](https://user-images.githubusercontent.com/110507463/222812477-9e475fe1-1dbc-4ff1-a7b0-0c98d9a58f79.png)
- ![image](https://user-images.githubusercontent.com/110507463/222812543-5e026e34-7e16-4d5a-8baa-6711a39c8ca7.png)
- ![image](https://user-images.githubusercontent.com/110507463/222812634-4b139b63-a465-41e9-a81b-5645103275f5.png)

The results suggest that the method of introducing an hidden layer with the tanh function only slightly inproved the model performance. However the disparity between the loss and accuracy in both the first and second attempts demonstrate overfitting while the last attempt, though at lower accuracy, still has less variance between the loss and accuracy scores. Based on this evidence, next I would try to run both hidden layers as the tanh model. I would also look for outliers and remove them as neccessary to reduce noise, add columns back in, specifically the "NAME" column, and deploy a  keras tuner to find the best optimization. I tried to do this in my initial attempt to optimize but my limited understanding of Machine Learning rendered me unable to troubleshoot to errors I was receiving, even with the help of the internet. 

