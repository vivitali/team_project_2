## README TEAM #3
#### VITALII / ADITHYA / AMRIT / SHIYAM

How will you select your dataset?
We selected our dataset from Kaggle, specifically the "Credit Score Classification" dataset by Paris Rohan. This dataset was chosen due to its relevance to our analysis objectives, its comprehensive features, and the fact that it provides sufficient data points to perform meaningful statistical analysis and visualizations. This was the same dataset as our first project.

How will you make sure all team members can contribute to the project?
To ensure all team members can contribute to the project, we will:

We used version control system like Git to manage our codebase, allowing everyone to work on different parts of the project simultaneously.
Assign specific roles and tasks based on each team member's strengths and interests, such as data cleaning, visualization, model development, and documentation.
Conduct regular team meetings to discuss progress, address any issues, and plan the next steps.

How will you make decisions?
Decisions will be made collaboratively through group discussions and consensus.

For more complex or technical decisions, we will:

Present and discuss the options during team meetings.
Use data and empirical evidence to support our choices.
If necessary, vote on the best course of action.
Ensure all voices are heard and considered to maintain a democratic process.

What are the specific objectives and success criteria for our machine learning model?
The objective of our machine learning model is to create a credit rating system (graded "Poor", "Standard", "Good") of an individual, with the use of five key inputs: annual income, number of credit inquiries, credit utilization ratio, outstanding debt and credit mix.
With this ML decisioning system, personal loan applications can be automated with only the need for five inputs and more importantly, remove any bias/PII in the data by not including non-finanical discriminators such as name, sex, address, post code, SIN etc.

How can we select the most relevant features for training our machine learning model?
The team ranked all the feature data provided based on what is most important for a credit rating system, while also ensuring that features with PII or potential bias were excluded. We chose the top five features - too many features would lead to drop-off in the application process for new potential customers, while not enough features may provide a poor accuracy and hence, bad lending metrics. A balance is required here.

Are there any missing values or outliers that need to be addressed through preprocessing?
The dataset provide over 100k rows of data. Many of the feature columns required cleaning (removing spaces, underscores etc.), type conversion (string --> float) and filtering the dataframe, while a couple of features had numerical inputs that were outliers and most likely incorrect. In aggregate, the cleaning process significantly reduced the dataset, which was not ideal.

Which machine learning algorithms are suitable for our problem domain? What techniques can we use to validate and tune the hyperparameters for our models?
This is a multiclass classification problem. A neural network (like the one used in this project) is generally the better ML algorithm to use if there is sufficient data at hand. Other methods include logistic regression, support vector machines and gradient boosting machines. The neural netowrk used for this problem has ~6.3m parameters across eight layers. Hyperparameters include the Adam optimizer set at the default learning rate (0.001) and categorical crossentrophy loss, whichs is commonly used with models that output a probability distribution across multiple classes, such as in multiclass classification. We trained the model over five epochs using ten observations batches plus used the test holdout dataset for validation. Some manual changes where made to the hyperparameters to optimize our metrics. We achieved an accuracy of ~62%, with our training and validation losses converging at the 5th epoch. A confusion matrix at the end of the file is used to evaluate the performance of the classification model.

How should we split the dataset into training, validation, and test sets?
We split the training data file for 80% traiing and 20% validation. We started at 70:30, but found improvements at 80:20. A separate file for testing was included in the Kaggle dataset.

Are there any ethical implications or biases associated with our machine learning model?
As mentioned earlier, we chose to focus on financial features only (annual income, number of credit inquiries, credit utilization ratio, outstanding debt and credit mix), and did not include any feature data that could imply a bias in the model (name, sex, address, post code). PII data, such as SIN, was excluded as well. Source data was never altered and is fully available. Code for cleaning the features is well documented as well.

How can we document our machine learning pipeline and model architecture for future reference?
Code documentation is well-commented and held on a jupyter notebook for easy evaluation. We store this on git to track changes and maintain history of code updates. The original readme file has been left as is, while this readme file serves to allow any new user/viewer of the repository to easily get up to date with the project's objective, data sources, code and results.


### Teams video

[Video link for Adithya's Video Link](https://www.loom.com/share/37a578c34d0e41afae01ef9671634978?sid=1a2f98a2-34b0-4199-89f6-84fc734d8140)

[Vitalii Vasinkevych Video link]

[Amrit Mehta's Video Link]

[Shiyam Mehta's Video Link]
