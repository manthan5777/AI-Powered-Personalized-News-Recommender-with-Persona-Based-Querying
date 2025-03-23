# AI-Powered-Personalized-News-Recommender-with-Persona-Based-Querying

📌 Project Overview
The AI-Powered Personalized Newsletter Generator is a multi-source, real-time news extraction system designed to deliver highly relevant articles tailored to user queries or predefined personas. It leverages NLP (Natural Language Processing) models like Sentence-BERT (all-MiniLM-L6-v2) to rank and filter news articles based on relevance. The project is built on Google Colab with a focus on real-time news extraction via RSS Feeds, relevance-based filtering using semantic similarity, support for user-defined queries and personalized personas, and experimentation with different embedding models and ranking techniques.

🔍 Key Features
The project offers multi-source news extraction, fetching real-time articles from reliable sources in categories such as Technology, Finance, Sports, Entertainment, and Science. It incorporates semantic search using the all-MiniLM-L6-v2 model, which provides high accuracy for encoding and ranking articles. The system supports custom query input, allowing users to define personalized searches or select from predefined personas for tailored results. It uses cosine similarity for relevance-based ranking, prioritizing the most relevant articles, and enables users to download preprocessed data as categorized CSV files for further analysis.

🎭 User Personas
The system supports both predefined personas and custom queries.

1.Alex Parker (Tech Enthusiast) is interested in AI, Cybersecurity, Blockchain, Startups, and Programming, with sources like TechCrunch, Wired, and Ars Technica.
2.Priya Sharma (Finance & Business Guru) focuses on Global Markets, Fintech, Cryptocurrency, and Economics, gathering news from Bloomberg, Financial Times, and 
  Forbes.
3.Marco Rossi (Sports Journalist) explores topics such as Football, F1, NBA, Esports, and Olympic Sports, with sources including ESPN, BBC Sport, and The Athletic.
4.Lisa Thompson (Entertainment Buff) enjoys Movies, Celebrity News, Music, and TV Shows, referencing sources like Variety, Rolling Stone, and Billboard.
5.David Martinez (Science & Space Nerd) is passionate about Space Exploration, Biotech, Physics, and Renewable Energy, with sources such as NASA, Science Daily, 
  and Nature.

⚙️ Technologies Used
The project utilizes Python for programming and is executed on Google Colab. It employs Sentence-BERT (all-MiniLM-L6-v2) for semantic similarity, Pandas for data preprocessing, and PyTorch for tensor computations. RSS Feeds are used to fetch real-time data.

🏗️ Project Structure
The project is organized as follows:

📁 Preprocessed_News_By_Genre: Contains CSV files categorized by genre:

Technology_News.csv
Finance_News.csv
Sports_News.csv
Entertainment_News.csv
Science_News.csv

🚀 How It Works
The project follows a structured pipeline to deliver personalized news:

1.Data Collection: News articles are extracted from multiple RSS Feeds across different genres.
2.Preprocessing: The system handles missing values, merges title and summary for meaningful context, and removes duplicate entries.
3.Encoding: Articles and user queries are converted into embeddings using all-MiniLM-L6-v2.
4.Similarity Scoring: Cosine similarity is computed between query embeddings and article embeddings to rank relevance.
5.Results: The system displays the top 5 most relevant articles for each query and allows downloading categorized CSV files.

🔬 Challenges Faced & Solutions
The project encountered several challenges during development, which were addressed with effective solutions:

1.Model Selection: Initial attempts with models like multi-qa-MiniLM-L6-cos-v1 failed to encode accurately. Switching to all-MiniLM-L6-v2 significantly improved 
  performance.
2.Relevance Ranking: Ranking diverse topics was complex. A hybrid approach using cosine similarity improved ranking precision.
3.Encoding Large Datasets: Encoding large numbers of articles led to performance lags. Batch encoding in Sentence-BERT optimized the process.
4.Persona Integration: Hardcoding persona choices limited flexibility. Allowing dynamic input enabled support for both predefined personas and custom queries.
5.Excessive Results: Displaying too many articles overwhelmed users. Limiting the output to the top 5 articles per query improved clarity.
6.Similarity Scores Visibility: Showing similarity scores cluttered the output. Removing scores from the final results enhanced readability.

✅ If you found this project helpful, please ⭐ star the repository!
