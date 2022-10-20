# Neural_Network_Charity_Analysis
Overview

The purpose of this analysis was to develop a neural network to help determine which organizations should be considered for funding from the AlphabetSoupCharity. We used previously obtained data of organizations that have been awarded or denied funding. The neural network is to be trained on multiple inputs to classify future organization requests for funding.

Results

Data Processing

•	What variable(s) are considered the target(s) for your model?

o	The target of IS_SUCCESSFUL is currently the only target for the model.

•	What variable(s) are considered to be the features for your model?

o	APPLICATION_TYPE
o	AFFILIATION
o	CLASSIFICATION
o	USE_CASE
o	ORGANIZATION
o	ASK_AMT
o	STATUS
o	INCOME_AMT
o	SPECIAL_CONSIDERATIONS

•	What variable(s) are neither targets nor features, and should be removed from the input data?

o	EIN

o	NAME

Compiling, Training, and Evaluating the Model

•	How many neurons, layers, and activation functions did you select for your neural network model, and why? 

o	For the initial attempt at model with two layers. 80 and 30 neurons, the "relu" type, were used. The activation feature of "sigmoid" was used. This was presented by the client as the starting point for model creation, allowing the analyst two further adjust to increase optimization.

•	Were you able to achieve the target model performance? 

o	The model performance was set at 75%. The current model only achieved an accuracy rating of 74.09% on epochs 96 and 99. An overall accuracy average of 72.98% was achieved.

•	What steps did you take to try and increase model performance?

o	 In order to improve efficiency, multiple model attempts were performed. The results of each attempt are listed below:

•	Attempt 1:

o	Dropped noisy data of ASK_AMT

o	Hidden layer one: tanh type - 80 neurons

o	Hidden layer two: relu type - 30 neurons

o	Activation: sigmoid

o	Highest accuracy/epoch: 74.08%, epoch 81 of 100

o	Overall accuracy average: 72.79%

•	Attempt 2:

o	Dropped noisy data of ASK_AMT

o	Hidden layer one: tanh type - 80 neurons

o	Hidden layer two: relu type - 50 neurons

o	Hidden layer three: sigmoid type - 30 neurons

o	Activation: relu

o	Highest accuracy/epoch: 74.00%, epoch 89 of 100

o	Overall accuracy average: 73.04%


•	Attempt 3:

o	Dropped noisy data of ASK_AMT

o	Hidden layer one: sigmoid type - 100 neurons

o	Hidden layer two: sigmoid type - 75 neurons

o	Hidden layer three: relu type - 50 neurons

o	Hidden layer four: relu type - 25 neurons

o	Activation: sigmoid

o	Highest accuracy/epoch: 74.09%, epoch 99 of 100

o	Overall accuracy average: 72.92%

•	Attempt 4:

o	Dropped noisy data of ASK_AMT

o	Hidden layer one: sigmoid type - 60 neurons

o	Hidden layer two: relu type - 30 neurons

o	Hidden layer three: relu type - 15 neurons

o	Activation: sigmoid

o	Highest accuracy/epoch: 74.20%, epochs 155 and 162 of 200

o	Overall accuracy average: 72.47%

Summary

The initial setup for the model did not perform at the required level, which was at 72.98%. With an iterative design, the model was adjusted and obtained at an increased rate of 73.04% on the second optimization attempt. The rest of the models had lower final accuracies than the initial model. Adjusting the number of hidden layers and neurons had a negligible effect on increasing model accuracy. Further adjustment may lead to an invalid model or one that overfits the dataset.
I would recommend a Random Forest classifier for a different model design. This is due to Random Forest ability of performing binary classification, the ability to handle large datasets, and the reduction in code which can achieve comparable accuracy predictions.

