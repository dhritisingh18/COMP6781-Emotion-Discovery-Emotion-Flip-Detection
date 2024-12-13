# COMP6781-Emotion-Discovery-Emotion-Flip-Detection
# Emotion Detection and Emotion Flip Detection in Conversations

## Project Overview
This project aims to analyze conversational data to accomplish two key tasks:
1. **Emotion Discovery**: Classify each conversational utterance into one of seven emotions: joy, anger, sadness, surprise, neutral, disgust, and fear.
2. **Emotion Flip Detection**: Identify emotional shifts between consecutive utterances in conversations.

## Team Members
- **Dhriti Singh**: [dhriti.singh@mail.concordia.ca](mailto:dhriti.singh@mail.concordia.ca)
- **Karthik Dammu**: [kdammu@live.concordia.ca](mailto:kdammu@live.concordia.ca)

## Dataset
- **Primary Dataset**: MELD (Multimodal EmotionLines Dataset)
- **Additional Dataset**: DailyDialog (for addressing class imbalance)
- **Challenges**:
  - Class imbalance with the dominance of "neutral" class.
  - Underrepresentation of minority classes like "fear" and "disgust."

## Key Highlights
- **Models Used**: Fine-tuned **DistilBERT** for both tasks.
- **Techniques Implemented**:
  - Focal Loss to mitigate class imbalance.
  - Random sampling for balanced class representation.
  - Confusion matrices and Precision-Recall curves for performance analysis.
- **Performance**:
  - Task A achieved **50% accuracy** in emotion classification.
  - Task B demonstrated **99% performance** in emotion flip detection.

## Methodology
1. **Baseline Model**: Used MELD dataset with basic BERT and CrossEntropyLoss.
2. **DistilBERT Integration**: Improved computational efficiency and performance for minority classes.
3. **Dataset Augmentation**: Combined MELD and DailyDialog to address class imbalance.
4. **Focal Loss Implementation**: Enhanced prediction for hard-to-classify emotions.
5. **Random Sampling**: Balanced dataset distributions for better minority class predictions.
6. **Parameter Tuning**: Adjusted batch size and learning rate to test sensitivity.

## Results
- **Best Configuration**: DistilBERT with **Focal Loss** and **random sampling of 1500 MELD data points**.
- **Performance Insights**:
  - Highest AUC scores: "Neutral" (0.83) and "Surprise" (0.88).
  - Lowest AUC scores: "Fear" (0.77).
  - Average Precision scores highlight difficulties with minority classes like "Fear" (0.19) and "Disgust" (0.36).

## Limitations
- Limited computational resources restricted the use of larger models like BERT-large or GPT.
- Style mismatches between MELD and DailyDialog reduced model generalization.
- Minority class predictions, though improved, still require further enhancement.

## Future Work
- Incorporate **K-fold cross-validation** to improve robustness.
- Expand the dataset with additional conversational data from other sources.
- Develop reasoning capabilities for detected emotional shifts to enhance real-world applicability.


## References
Refer to the project report for detailed references and methodology documentation.

---

For further inquiries, feel free to reach out to the team members via the provided email addresses.
