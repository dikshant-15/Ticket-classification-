Ticket Classification Project - Documentation

 Project Goal
The goal of this project is to automatically classify support tickets based on their text content. This helps teams route tickets to the right department quickly, reducing response time and improving customer service.



 Dataset Overview
We use a dataset of support tickets. Each ticket has a text field (the message) and a category label (like "billing", "technical issue", etc.).

Example data:
- "I can't access my account" → "technical issue"
- "Please refund my last payment" → "billing"


 Key Steps and Design Choices

1. **Text Cleaning**
   - Removed missing values and unnecessary characters.
   - Converted all text to lowercase.

2. **Tokenization and Vectorization**
   - Used `TfidfVectorizer` to convert text into numerical form that ML models can understand.

3. **Model Training**
   - Chose Logistic Regression for its simplicity and strong performance on small datasets.
   - Split data into training and testing sets (usually 80/20).

4. **Model Evaluation**
   - Used accuracy, precision, recall, and F1-score to measure how well the model performs.
   - Accuracy = How many tickets it classifies correctly out of total.
   - F1-score = Balance between precision (correct guesses) and recall (finding all right labels).

 Results (Example)
- Accuracy: ~89%
- F1 Score: ~0.87

This means the model works quite well and can be trusted to help classify tickets.


 Limitations
- The model may struggle with very short or vague tickets.
- New or rare categories not seen during training might be misclassified.
- Heavily depends on the quality of labeled data.


 Future Improvements
- Use deep learning (e.g., BERT) for better accuracy.
- Add spell-check and synonym recognition.
- Build a web app (Streamlit) so non-technical users can try it easily.


