---
layout: post
title: "Decoding Public Opinion: A Sentiment Analysis of Nintendo Switch 2 Discussions on Reddit"
subtitle: "Using Hugging Face Transformers to Perform Sentiment Analysis"
background: '/img/posts/Nintendo_Switch_2/brain.jpg'
---

This project analyzes Reddit posts about the new Nintendo Switch 2 to perform sentiment analysis and categorize emotional tones as positive, negative, or neutral across various gaming subreddits. By mapping these sentiments to specific topics and identifying dominant emotions, we gain crucial insights into overall community sentiment and pinpoint areas of widespread concern or positive engagement. This direct understanding of public sentiment from Reddit is vital for understanding trends, informing content strategies, and identifying key discussion drivers.
![png](/img/posts/Nintendo_Switch_2/nw2.png)



### **Key Findings on User Sentiment**

- **Overwhelming enthusiasm and gratitude:**  
  Most users, as expected, are very excited about the Switch 2’s launch, expressing anticipation for receiving their consoles. A recurring theme is a call for politeness and patience towards postal/delivery/customer service employees during the high-demand launch period.

- **Hardware and Design Praises:**  
  The Switch 2’s hardware improvements seem to be a success. Users are impressed with its technical performance, some saying how impressed they are with the “butter smooth 60 FPS” and visuals. The new Pro Controller has consistently received stellar reviews for its lightweight body, long battery life, excellent sticks, and ergonomic design. Most users are impressed with the new Switch 2 built-in speakers, hailed as a significant upgrade from the previous iteration.

- **Thriving Accessory Market:**  
  Users are curious and are actively seeking new accessories for their console, including carrying cases, bags, and even wall mounts. A strong desire for customization and protection for their new devices is seen through several posts.

- **Game-specific Acclaim:**  
  “Mario Kart World” is an undeniable success, garnering universal acclaim for its “impressive artistic achievement” and “innovative concept.” Without a doubt, the game is poised to be a significant sales driver for the new console. Developers from indie studios are also expressing gratitude for the new platform and highlighting successful launches for their new games.

---

### **Areas for Strategic Focus and Improvement**

- **Game Performance and Compatibility Issues:**  
  A notable number of users are expressing disappointment regarding performance for certain titles. This includes but is not limited to visual smoothness, certain games simply failing to boot up, and a general frustration of older games simply not performing well with the new console. Furthermore, some third-party accessories are no longer working with the original Switch after a software update, perhaps indicating initial signs of Nintendo slowly shifting its focus to the Switch 2.

- **Ergonomic and Controller Issues:**  
  Some users are reporting discomfort when using the Switch 2 in handheld mode due to a lack of grip on the Joy-Cons; some are even reporting cases of the notorious stick drift. In general, there are early signs of concern about the quality of the Joy-Con controllers, some mentioning a “Cheap” feel to them.

- **Feature Expectation vs. Reality:**  
  Some users are disappointed in the lack of new features, for example, the absence of anti-aliasing despite having the technical capability for it.

- **Stock Availability Frustration:**  
  While most users are largely understanding, there’s an underlying frustration acquiring the new console and certain accessories due to the initial high-demand period.

---

### **So What’s Recommended?**

1. **Prioritize Software Optimization and Compatibility Patches**  
   *Action:* Immediately investigate reported performance issues and game booting for key titles. Collaborate with third-party developers to ensure optimal game performance, especially for older Switch titles. Additionally, release firmware updates to restore compatibility for third-party accessories. This should signal to customers the commitment they still have to the original Switch users.

2. **Enhance Ergonomics and Quality Control**  
   *Action:* Investigate reported Joy-Con 2 ergonomic issues. Perhaps redesign future Joy-Cons and develop and promote first-party ergonomic grips/accessories. Begin conducting an analysis of the quality of Joy-Con 2 thumb stick components to address issues.

3. **Manage Feature Expectations and Communication**  
   *Action:* Clearly communicate to customers a technical roadmap for upcoming features for the Switch 2 to demonstrate ongoing improvements.

4. **Optimize Supply Chain**  
   *Action:* While it is expected that stock would be an issue for launch, strive to continue research and improvement for the supply chain to reduce stock scarcity. Find ways to mitigate scalpers.

---
My analysis involved examining the representative documents for each identified topic. These documents are selected as the most characteristic examples within their respective clusters, providing insight into the primary discussions and thematic coherence driving each grouping. These key discussions are summarized below for each topic as of June 22, 2025.
### **Topic (Nintendo,Switch,Games)**

**Good:**  
Most posts express a positive attitude about Nintendo’s successful launch; it seems most people are impressed by the Nintendo Switch 2’s technical performance. There is significant gratitude towards Nintendo’s huge impact on the gaming industry and continued innovation. Some are interested in new game recommendations as they acquire the new console.

**Bad:**  
Most negative reactions seem to focus on game performance for certain titles. For example, "Minecraft Legends" presents issues with visual smoothness, and some games fail to boot entirely on the new console. Some users are frustrated by the lack of new features expected with new consoles. Overall, there's a general sentiment of missing older, smooth, and reliable gaming experiences.

---
### **Topic (Gameplay, Game, Games)**

**Good:**  
Most "good" posts are from indie game developers announcing and promoting their new games, emphasizing unique gameplay mechanics. Most of them are appreciative of the positive community feedback and successful launch of their games for the new console. Many are simply inviting players to try their demos.

**Bad:**  
No negative representative documents were found for this topic.

---

### **Topic (Walmart, Store, Stock)**

**Good:**  
Most users are simply excited and anticipating their console to arrive. Some users are receiving them as gifts, and there are also giveaways on the r/gaming subreddit. A recurring theme is a call for politeness and patience towards postal/delivery/customer service employees during the high-demand launch period.

**Bad:**  
A few posts display how tough it is to find the console and certain accessories in stock.

---

### **Topic (Controllers, Controller, Buttons)**

**Good:**  
A very popular post discusses the design of a custom-made, one-handed Joy-Con 2 adapter for those with disabilities. Users provide detailed and highly positive reviews of the Switch 2 Pro Controller. On the other hand, some posts address issues with controller docking problems and ergonomic concerns, seeking help from the community for solutions.

**Bad:**  
Some users are frustrated about the incompatibility of certain third-party accessories no longer working on the original Switch after a major software update, perhaps indicating initial signs of Nintendo slowly shifting its focus to its new console. Some users are annoyed at the Joy-Con thumb stick already feeling off and cheap.

---

### **Topic (Cases, Case, Nintendo)**

**Good:**  
Most users are curious about what accessories are available in the market for the new consoles. Some users are seeking recommendations while others share their experiences with recent purchases. Mostly new users are aiming to help others find beneficial add-ons for their new console.

**Bad:**  
No negative posts were found for this topic.

---

### **Conclusion**

Most users are excited for the Switch 2 and its hardware improvements; many are particularly impressed with the new "Mario Kart World" release. While the console generally receives positive feedback, some users discuss performance issues, game compatibility bugs (between Switch and Switch 2), ergonomic issues, and aspects of the console’s design, actively requesting solutions or workarounds. In general, most users are happy with their purchase, understanding of the limited stock and initial hiccups, and willing to work around them. As long as the issues stated above are addressed, the user experience can be enhanced and reinforce Nintendo’s reputation for innovation and quality.

---

### **Production and Scalability of this Project**

- Create a **modular pipeline** to extract, clean and load the data into a dashboard. Perhaps using **Airflow or Dagster**.  
- Use **Cloud infrastructure** to store scripts that run on a periodic basis such as **AWS Lambda or Azure Functions**.  
- Package **NLP models or components in Docker/Azure Containers**.  
- Give stakeholders **real-time access** to insights using a dashboard such as **PowerBI or Tableau** that updates with scheduled dumps.  
- Since a **pretrained model was used**, we could potentially retrain the model and **fine-tune it as more data comes in**.

```python
!pip install praw
!pip install nltk
```


```python
import praw
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
import pprint
import requests
from datetime import datetime, timedelta
import re
import nltk
import sklearn
from wordcloud import WordCloud
```


```python
nltk.download('punkt_tab')
```

### Crawl gaming sub reddits for Switch 2 discussions since the release of the console using PRAW


```python
# Credentials for PRAW API
user_agent = 'Reddit Sentiment Analysis 1.0'

reddit = praw.Reddit(
    client_id = client_id,
    client_secret = client_secret,
    user_agent = user_agent
)
```


```python
start_date = datetime(2025, 6, 5)
end_date = datetime (2025, 6, 22)
# Get current date and time
now = datetime.now()

# Calculate the time difference
time_difference = now - start_date

# Convert to hours
hours = time_difference.total_seconds() / 3600
```


```python
headlines = set()
reddit_post = set()
# search the following subreddits for the following keywords
# and add the titles to the headlines set if they were created after the start date
subreddits = ["NintendoSwitch2", "NintendoSwitch", "gaming", "nintendo", "Games", "gamernews"]
keywords = ["Nintendo Switch 2", "launch", "first impressions", "review", "performance", "hands-on", "graphics", "issues", "problems", "bugs", "features", "specs", "hardware", "software", "game library", "expectations", "price"]
for subreddit in subreddits:
    for keyword in keywords:
        for submission in reddit.subreddit(subreddit).search(keyword, sort='hot', time_filter='month', limit=200):
            if submission.created_utc > start_date.timestamp() and submission.created_utc <= end_date.timestamp():
                headlines.add(submission.title)
                reddit_post.add(submission.selftext)




```


```python
reddit_post = list(reddit_post)
```

#### Cleaning up posts: removing URLS, leading spaces and symbols. Truncating long strings that exceed ~512 tokens



```python
def clean_text(text):
    pattern = re.compile(r"[^a-zA-Z0-9\s.,!?:;'\"()-]")

    # Replace any character matched by 'pattern' with a single space.
    # Then, use .strip() to remove leading/trailing whitespace.
    cleaned_text = pattern.sub(' ', text).strip()

    # Let's reduce multiple spaces to a single space.
    cleaned_text = re.sub(r'\s+', ' ', cleaned_text)
    return cleaned_text

```


```python
# clean up reddit post bodies and seperate paragraphs into sentences, remove urls and extra puncutations
failed = []
for i in range(len(reddit_post)):
  try:
    reddit_post[i] = clean_text(reddit_post[i])
  except:
    failed.append(i)
    continue

print(len(failed))
```

    0



```python
# store reddit posts into a df
posts = pd.DataFrame(reddit_post, columns=['Post'])

```


```python
def count_tokens(text):
  length = len(nltk.word_tokenize(text))
  return length
```


```python
posts['Token Count'] = posts['Post'].apply(lambda x: count_tokens(x))
print(f"Percentage of posts that exceed token limit for sentiment analysis: {len(posts[posts['Token Count'] > 512])/len(posts)}")
```

    Percentage of posts that exceed token limit for sentiment analysis: 0.07376058041112454


#### Initiate process of sentiment analysis


```python
from transformers import pipeline
# choosing sentiment analysis pipeline (Emotions)
classifier = pipeline("sentiment-analysis", model="SamLowe/roberta-base-go_emotions")

```

    Device set to use cpu



```python
# for each row conduct a sentiment analysis and categorize it, truncate string to max length
posts['Sentiment'] = posts['Post'].apply(lambda x: classifier(x, truncation=True, max_length=512)[0]['label'])
```


```python
# Add probabilities to dataframe
posts['Sentiment_Prob'] = posts['Post'].apply(lambda x: classifier(x, truncation=True, max_length=512)[0]['score'])
```


```python
print(f"Post Count {len(posts)}")
```

    Post Count 827



```python
# create a bar chart, counts for each sentiment
posts['Sentiment'].value_counts().plot(kind='bar', title='Overall Sentiment', xlabel='Sentiment', ylabel='Count')
```




    <Axes: title={'center': 'Overall Sentiment'}, xlabel='Sentiment', ylabel='Count'>




    
![png](/img/posts/Nintendo_Switch_2/nintendo_switch_sentimentanalysis_23_1.png)
    


The most common emotions according to the sentiment analysis model are neutral, curiosity and admiration. Which seems plausible and expected during the launch period of the console. Neutral perhaps means that the console has reached expectations but not necessairly exceeded them, which brings us to the curiosity of customers. Posts that show admiration seem to mostly talk about the New Mario Kart World game and the design of the console.


```python
# convert CleanedPost to string
posts['CleanedPost'] = posts['CleanedPost'].astype(str)
```


```python
# Define mapping of predicted emotions to 'good', 'bad', or 'neutral'
emotion_mapping = {
    'admiration': 'good',
    'amusement': 'good',
    'anger': 'bad',
    'annoyance': 'bad',
    'approval': 'good',
    'caring': 'good',
    'confusion': 'neutral',
    'curiosity': 'neutral',
    'desire': 'neutral',
    'disappointment': 'bad',
    'disapproval': 'bad',
    'disgust': 'bad',
    'embarrassment': 'bad',
    'excitement': 'good',
    'fear': 'bad',
    'gratitude': 'good',
    'grief': 'bad',
    'joy': 'good',
    'love': 'good',
    'nervousness': 'bad',
    'neutral': 'neutral',
    'optimism': 'good',
    'pride': 'good',
    'realization': 'neutral',
    'relief': 'good',
    'remorse': 'bad',
    'sadness': 'bad',
    'surprise': 'neutral',
    'neutral': 'neutral',
    'embarrassment': 'bad',
    'excitement': 'good',
    'fear': 'bad',
    'gratitude': 'good',
    'grief': 'bad',
    'joy': 'good',
    'love': 'good',
    'nervousness': 'bad',
    'optimism': 'good',
    'pride': 'good',
    'realization': 'neutral',
    'relief': 'good',
    'remorse': 'bad',
    'sadness': 'bad',
    'surprise': 'neutral'
}

# Apply the mapping to create a new column 'Categorized Sentiment'
posts['Categorized Sentiment'] = posts['Sentiment'].map(emotion_mapping)

# You can then visualize the counts of these new categories
posts['Categorized Sentiment'].value_counts().plot(kind='bar', title='Categorized Sentiment', xlabel='Sentiment Category', ylabel='Count')
```




    <Axes: title={'center': 'Categorized Sentiment'}, xlabel='Sentiment Category', ylabel='Count'>




    
![png](/img/posts/Nintendo_Switch_2/nintendo_switch_sentimentanalysis_26_1.png)
    


To simplify the emotions we gathered using the sentiment analysis model, we categorized them into 3 bins ("Neutral", "Good" and "Bad"). Most posts fall into the Neutral and Good bins, a sign that the console has met expectations and customers are potentially happy about the purchase or excited to acquire it.


```python
# bertopic inspired model helps reduce the appearence of stop words and improves topic represenation
!pip install bertopic
from bertopic import BERTopic
from bertopic.representation import KeyBERTInspired
```


```python
representation_model = KeyBERTInspired()
topic_model = BERTopic(embedding_model="sentence-transformers/all-MiniLM-L6-v2", representation_model=representation_model,
                       min_topic_size=20)
```


```python
topics, probs = topic_model.fit_transform(posts['CleanedPost'][1:])
```


```python
topic_model.get_topic_info()
```





<style>
table {
    border-collapse: collapse;
    width: 100%;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-size: 14px;
    margin: 20px 0;
}
thead {
    background-color: #f7f7f7;
}
th, td {
    padding: 12px 15px;
    border: 1px solid #ddd;
    text-align: left;
}
tbody tr:nth-child(even) {
    background-color: #f9f9f9;
}
tbody tr:hover {
    background-color: #f1f1f1;
}
th {
    background-color: #eaeaea;
    font-weight: bold;
}
</style>

<table>
    <thead>
        <tr>
            <th>Topic</th>
            <th>Count</th>
            <th>Name</th>
            <th>Representation</th>
            <th>Representative Docs</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>-1</td><td>432</td><td>-1_switch_games_nintendo_game</td><td>[switch, games, nintendo, game, playing, play,...]</td><td>[i know everyone wants to hate on this game fo...]</td></tr>
        <tr><td>0</td><td>72</td><td>0_gameplay_game_games_play</td><td>[gameplay, game, games, play, build, combat,...]</td><td>[hello there! i'm brulo, director of flatline ...]</td></tr>
        <tr><td>1</td><td>67</td><td>1_walmart_store_stock_inventory</td><td>[walmart, store, stock, inventory, stores,...]</td><td>[had been checking targets and walmarts in my ...]</td></tr>
        <tr><td>2</td><td>62</td><td>2_1080p_ps4_framerate_60fps</td><td>[1080p, ps4, framerate, 60fps, 720p, 30fps,...]</td><td>[last update : june 7. new confirmed finds wil...]</td></tr>
        <tr><td>3</td><td>61</td><td>3_controllers_controller_grip_buttons</td><td>[controllers, controller, grip, buttons,...]</td><td>[so, to preface this : i mostly love the new p...]</td></tr>
        <tr><td>4</td><td>45</td><td>4_games_game_kirby_mario</td><td>[games, game, kirby, mario, play, pokemon,...]</td><td>[i usually play casual cs2 matches or league o...]</td></tr>
        <tr><td>5</td><td>34</td><td>5_case_nintendo_accessories_carrying</td><td>[case, nintendo, accessories, carrying,...]</td><td>[i ordered these 4 cases to see which is the b...]</td></tr>
        <tr><td>6</td><td>27</td><td>6_kart_karts_prix_nintendo</td><td>[kart, karts, prix, nintendo, mario,...]</td><td>[i ll start with the positives. the game oozes...]</td></tr>
        <tr><td>7</td><td>26</td><td>7_nintendo_games_switch_console</td><td>[nintendo, games, switch, console, issues,...]</td><td>[source ( https : en - americas - support. nin...]</td></tr>
    </tbody>
</table>

While the relative order of topics varied daily, their core identities remained largely consistent throughout this process. Temporal analysis could offer valuable insights into how customer focus is shifting over time.

```python
# drop first row empty string
posts = posts.drop(posts.index[0]).reset_index(drop=True)

posts['topic_id']= topics

# Remove Outlier
df_posts_filtered = posts[posts['topic_id'] != -1]

# add human readable topic names
topic_id_to_name = {row['Topic']: row['Name'] for index, row in topic_model.get_topic_info().iterrows()}
df_posts_filtered['topic_name'] = df_posts_filtered['topic_id'].map(topic_id_to_name)

# add human readable topic names
topic_id_to_name = {row['Topic']: row['Name'] for index, row in topic_model.get_topic_info().iterrows()}
df_posts_filtered['topic_name'] = df_posts_filtered['topic_id'].map(topic_id_to_name)

sentiment_by_topic
```
<style>
  table {
    width: 100%;
    border-collapse: collapse;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    font-size: 14px;
    margin: 20px 0;
  }
  thead {
    background-color: #f0f0f0;
  }
  th, td {
    border: 1px solid #ddd;
    padding: 10px 12px;
    text-align: left;
  }
  tbody tr:nth-child(even) {
    background-color: #f9f9f9;
  }
  tbody tr:hover {
    background-color: #eef6ff;
  }
  th {
    background-color: #e2e8f0;
    font-weight: bold;
  }
</style>

<table>
  <thead>
    <tr>
      <th>Topic Name</th>
      <th>Bad</th>
      <th>Good</th>
      <th>Neutral</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>0_gameplay_game_games_play</td><td>0.013889</td><td>0.388889</td><td>0.597222</td></tr>
    <tr><td>1_walmart_store_stock_inventory</td><td>0.119403</td><td>0.208955</td><td>0.671642</td></tr>
    <tr><td>2_1080p_ps4_framerate_60fps</td><td>0.096774</td><td>0.467742</td><td>0.435484</td></tr>
    <tr><td>3_controllers_controller_grip_buttons</td><td>0.147541</td><td>0.393443</td><td>0.459016</td></tr>
    <tr><td>4_games_game_kirby_mario</td><td>0.066667</td><td>0.555556</td><td>0.377778</td></tr>
    <tr><td>5_case_nintendo_accessories_carrying</td><td>0.000000</td><td>0.441176</td><td>0.558824</td></tr>
    <tr><td>6_kart_karts_prix_nintendo</td><td>0.111111</td><td>0.481481</td><td>0.407407</td></tr>
    <tr><td>7_nintendo_games_switch_console</td><td>0.115385</td><td>0.076923</td><td>0.807692</td></tr>
  </tbody>
</table>


```python
# stacked bar chart visualization
# add labels to bar chart for each stacked bar

ax = sentiment_by_topic.plot(kind='barh', stacked=True ,colormap='Pastel1')
plt.title('Sentiment by Topic')
plt.xlabel('Proportion')
plt.ylabel('Topic')

plt.legend(title='Sentiment', bbox_to_anchor=(1.05, 1), loc = 'upper left')

# Add labels to the bars
for container in ax.containers:
    labels = [f'{w:.2f}' if (w := v.get_width()) > 0 else '' for v in container]
    ax.bar_label(container, labels=labels, label_type= 'center')

plt.show()



```


    
![png](/img/posts/Nintendo_Switch_2/nintendo_switch_sentimentanalysis_39_0.png)
    


Overall, the sentiment appears to lean heavily towards neutral, followed by a significant proportion of good sentiment, and a smaller but consistent presence of bad sentiment across most topics. No single topic is overwhelmingly negative or positive, suggesting a diverse range of opinions or discussions, with many comments simply being factual or non-emotional. While some topics like "games_game_kirby_mario" and "kart_karts_nintendo" have a noticeable "good" proportion.


```python
# avg emption by topic
emotion_by_topic = df_posts_filtered.groupby('topic_name')['Sentiment'].value_counts(normalize=True).unstack()
score_threshold = 0.1
filtered_emotion_by_topic_data =emotion_by_topic[(emotion_by_topic > score_threshold).any(axis=1)]
index_text = filtered_emotion_by_topic_data.columns
```


```python
# Create the heatmap
from matplotlib.patches import Rectangle
row_max = filtered_emotion_by_topic_data.idxmax(axis=1)
num_emotions = filtered_emotion_by_topic_data.shape[0] # Rows are emotions
num_topics = filtered_emotion_by_topic_data.shape[1]   # Columns are topics


fig_width = max(12, num_topics * 0.9)  # More space for each topic column
fig_height = max(8, num_emotions * 0.6) # More space for each emotion row


plt.figure(figsize=(fig_width, fig_height)) # Apply size

ax = sns.heatmap(
    filtered_emotion_by_topic_data,
    annot=True,
    fmt='.2f',
    cmap='YlGnBu',
    linewidth=0.5,
    cbar_kws={'label': 'Average Emotion Score'}
)

for row_idx, emotion_label in enumerate(filtered_emotion_by_topic_data.index):
    # Get the topic with the maximum score for the current emotion
    max_topic_for_emotion = row_max[emotion_label]
    # Get the column index (position) of that topic in the heatmap
    position = filtered_emotion_by_topic_data.columns.get_loc(max_topic_for_emotion)

    # Add a red rectangle around the cell with the max value
    offset = 0.02
    shrink = 0.04 # 2 * offset

    ax.add_patch(Rectangle((position + offset, row_idx + offset), 1 - shrink, 1 - shrink,
                       fill=False, edgecolor='red', linestyle='--', lw=2))

plt.title('Average Emotion Scores (Transposed) per Topic', fontsize=16)
plt.xlabel('Emotion', fontsize=12)
plt.ylabel('Topic', fontsize=12)
plt.xticks(rotation=45, ha='center', fontsize=10)

plt.show()
```


    
![png](/img/posts/Nintendo_Switch_2/nintendo_switch_sentimentanalysis_42_0.png)
    


Neutrality is the most prevalent emotion across most discussions, particularly strong in topics like "gameplay_game_games_play" and "walmart_store_stock_inventory." While emotions like curiosity and optimism emerge in specific topics such as "nintendo_games_switch_console" and "kart_karts_nintendo".


```python
from sklearn.datasets import fetch_20newsgroups
from sentence_transformers import SentenceTransformer
from bertopic import BERTopic
from umap import UMAP


posts.reset_index(drop=True, inplace=True)
# visualize clusters of topics
# wrap documents for easier reading in visualization
topic_model.visualize_documents(posts['CleanedPost'])

```
<!-- 
![png](/img/posts/Nintendo_Switch_2/topics2d.png) -->

<img src="/img/posts/Nintendo_Switch_2/topics2d.png" width=500/>
The graph above shows the similarity and clustering of the topics, for example topic 3 and 5 are mostly talking about console peripherals.


```python
from wordcloud import WordCloud
import matplotlib.pyplot as plt

def create_wordcloud_all_topics(topic_model, top_n_words=50):

    all_words_frequencies = {}

    # Iterate through all topics
    for topic_id in topic_model.get_topics():
        if topic_id == -1:  # Skip the outlier
            continue

        # Get the top words for the current topic
        # topic_model.get_topic(topic_id) returns a list of (word, value) tuples
        topic_words = topic_model.get_topic(topic_id)

        # Add to dictionary
        for word, value in topic_words[:top_n_words]: # Consider only top N words from each topic
            all_words_frequencies[word] = all_words_frequencies.get(word, 0) + value

    if not all_words_frequencies:
        print("No words found to generate a word cloud. The topic model might be empty or topics are not well-defined.")
        return

    # Create the word cloud from all_word_frequencies
    wc = WordCloud(background_color="white", max_words=1000, width=800, height=400)
    wc.generate_from_frequencies(all_words_frequencies)

    # Display the word cloud
    plt.figure(figsize=(10, 5))
    plt.imshow(wc, interpolation="bilinear")
    plt.axis("off")
    plt.title("Word Cloud for All Topics Combined")
    plt.show()
```


```python
create_wordcloud_all_topics(topic_model, top_n_words=100)
```


    
![png](/img/posts/Nintendo_Switch_2/nintendo_switch_sentimentanalysis_47_0.png)
    


Key themes revolve around gaming (e.g., "game," "games," "play," "Nintendo," "Switch," "Mario"), hardware (e.g., "controller," "controllers," "joyscons," "ps4," "1080p"), and retail/inventory (e.g., "Walmart," "store," "stock," "inventory").
