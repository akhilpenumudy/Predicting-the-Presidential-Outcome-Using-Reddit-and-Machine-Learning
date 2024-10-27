# Predicting-the-Presidential-Outcome-Using-Reddit-and-Machine-Learning
This project intends to predict the outcome of the 2024 presidential election by analyzing sentiment trends on the r/politics subreddit. Using web scraping and machine learning, it classifies posts daily, detecting partisan leanings and shifts over time, with the goal of forecasting the final election result based on social media discourse.

```mermaid


flowchart LR
    A[Start: Daily Reddit Scraping] --> B[Store Post Headlines in DataFrame]
    B --> C[Use Gemini AI Model for Classification]
    C --> D{Classify Each Headline}
    D -->|Supports Republicans| E[R - Republican Favorable]
    D -->|Supports Democrats| F[B - Democrat Favorable]
    D -->|Neutral Stance| G[N - Neutral]
    
    E --> H[Store Classifications in DataFrame]
    F --> H
    G --> H
    
    H --> I[Aggregate Daily Results]
    I --> J[Merge into 'total classified posts' data set]
    J --> K[Analyze Sentiment Trends Over Time]
    K --> L[Predict Election Outcome on Final Day]
    L --> M[End: 2024 Election Outcome Prediction]

    style A stroke:#ff3,stroke-width:2px
    style M stroke:#ff3,stroke-width:2px

    style E stroke:#ba3329,stroke-width:2px
    style F stroke:#2985ba,stroke-width:2px
    style G stroke:#e0d4d3,stroke-width:2px


    A --> |Repeat Daily Until Election Day| J
