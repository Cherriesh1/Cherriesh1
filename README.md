Load the dataset
data = pd.read_csv("disease_data.csv")

# Separate features and target variable
X = data.drop("Disease", axis=1)
y = data["Disease"]

# Split data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a Decision Tree classifier
model = DecisionTreeClassifier()

# Train the model
model.fit(X_train, y_train)

# Make predictions on the testing set
y_pred = model.predict(X_test)

# Evaluate the model's accuracy
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)

# Create a function to predict disease based on user input
def predict_disease(symptoms):
    # Preprocess user input (e.g., convert to numerical features)
    user_input = preprocess_input(symptoms)

    # Make prediction
    predicted_disease = model.predict([user_input])

    return predicted_disease- 👋 Hi, I’m @Cherriesh1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Cherriesh1/Cherriesh1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
