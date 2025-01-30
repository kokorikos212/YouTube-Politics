# Evaluating Political Influence Through Digital Metrics

## Overview
This project analyzes political influence on YouTube using data-driven methods. It collects and processes YouTube data, applies sentiment analysis using a fine-tuned BERT model, and examines transparency indicators such as disabled comments and likes.

## Motivation
Greek politics often face transparency concerns. By leveraging open digital data, we aim to assess the relationship between political influence and YouTube activity while identifying potential biases.

## Data Sources
- **YouTube API**: Collects video metrics (likes, views, comments, etc.).
- **Electoral & Polling Data**: Provides contextual political ground truth.
- **Sentiment Analysis Dataset**: Used for fine-tuning BERT (Greek Uncased v1).

## Technologies Used
- **SQL**: Stores structured YouTube data.
- **TensorFlow & TensorBoard**: Fine-tunes the BERT model for sentiment analysis.
- **Python & Jupyter Notebooks**: Implements data processing, visualization, and model training.
- **Docker**: Containerizes and deploys the project components.

## Project Structure
```
src/
├── EDA/
│   ├── Data preprocessing and visualization scripts.
│   ├── Sentiment analysis & comments processing.
│   └── Jupyter notebooks for exploratory analysis.
│
├── Engine/
│   ├── YouTube API data collection.
│   ├── Database creation & data storage.
│   ├── Logging and utility scripts.
│   ├── Dockerfile for deployment.
│   └── Main entry point for execution.
│
├── sentiment_analysis/
│   ├── BERT fine-tuning and inference.
│   ├── Model training and evaluation scripts.
│   ├── Sentiment-labeled datasets.
│   └── Visualization of sentiment trends.
│
└── utils/
    ├── General utility scripts.
    └── Database and data handling helpers.
```

## Key Questions
- What is the correlation between YouTube activity and political influence?
- How do transparency metrics (disabled likes/comments) relate to content?
- How can sentiment analysis be refined to reduce biases?
- What techniques improve model evaluation for political discourse analysis?

## Limitations & Future Work
- The project is an initial exploratory analysis.
- Model bias needs further investigation and mitigation.
- Cloud-based scaling is required for larger-scale sentiment analysis.
- Expanding the dataset and statistical analysis would enhance insights.

## References
- [IMEDD Report on Greek Media](https://www.imedd.org/media-capture-in-greece-a-new-report-by-ipi-mjrc/)
- [Skroutz Sentiment Analysis with BERT (Kaggle)](https://www.kaggle.com/code/nospaearth/skroutz-sentiment-analysis-with-bert-greek-v-2/edit)

## How to Use
1. Clone the repository.
2. Install dependencies (`pip install -r requirements.txt`).
3. Set up API keys and database configurations.
4. Run data collection and preprocessing scripts.
5. Train and evaluate the sentiment analysis model.
6. Analyze results using Jupyter notebooks.

Example Configuration File

Create a JSON file to configure the application:
{
    "api_key" : "API_KEY",		
  "database_path": "db/SQL/test.db",
  "yt_channel_ids": ["UCba2NEel1Go5wI2wymPrSKw",
                    "UCwzjrcwPZXoW_iDkY76FbEQ",
                    "UCew8bLiDgkU7_Cci-YP8iGA"
	]
}

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.


