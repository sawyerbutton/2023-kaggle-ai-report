# 2023 Kaggle AI Report 

https://www.kaggle.com/competitions/2023-kaggle-ai-report realate repo

## Project Goal

The primary aim of this project is to leverage the diverse expertise within the Kaggle community to centralize and summarize the rapid advancements in AI over the past two years. This project is designed to share the collective perspectives of the Kaggle community with the broader research community.

## Project Context

In this analytical competition, participants will write an essay on one of the following seven topics, elucidating what the community has learned over the past 2 years of working and experimenting with:

- Text data
- Image and/or video data
- Tabular and/or time series data
- Kaggle Competitions
- Generative AI
- AI ethics
- Other (anything that does not fall into any other category)

Kaggle has provided a collection of writeups and a collection of scholarly articles in the official competition dataset, but participants are free to use any resources. Participants will also engage in a peer feedback process that involves reviewing three peer essays. Submissions will be evaluated by an expert grading panel of seven Kaggle Grandmasters. Winning essays will be aggregated in a post-competition publication and credited to their respective authors.

## My Idea

### Project Goal

The primary goal of this project is to craft a research paper articulating the relationship between community problem-solving approaches and academic paper publications. This includes exploring questions such as: How does the community utilize academic papers to solve specific problems? Does the community prefer using techniques from newer papers or older ones? Are there any discernible trends in this respect?

Moreover, instead of manually composing the paper, I plan to employ generative models, possibly using pre-trained or addone-document Langchain technologies to aid in the generation of the paper.

### Data Analysis Approach

The dataset for this project consists of Kaggle competition write-ups and metadata from arXiv papers. The arXiv dataset includes vital information such as the title, abstract, category, and release date of the papers. However, as arXiv has its categorization system that might not align perfectly with the competition's seven topic categories, the initial task would be to re-categorize the papers into one of these seven topics to ensure relevant data for the chosen theme.

The Kaggle competition write-ups also need to be categorized based on the competition's classification. Attention should also be given to the dataset's temporal information to correlate with the release dates of the papers.

Since the write-ups dataset has already filtered the optimal and sub-optimal solutions for the former related competitions, the focus should be on establishing the connection between these solutions and published papers. The goal is to construct this connection and present it as a thesis and conclusion in the paper.

### Current Problem

At present, I am working on categorizing arXiv papers into competition categories. I've envisioned two strategies for this step:

1. Use the LLM API for Zero-Shot classification based on the paper abstracts. This approach might require a considerable budget.

2. Similar to the first approach, use LLM's free credit to generate a small-sized labeled dataset based on the paper abstracts. Given the current token consumption rate, I estimate generating around 1000 labeled instances. Then, this small dataset would be fine-tuned using an encoder model like BERT. Finally, the fine-tuned BERT, along with the classification model, would be used for classifying the remaining papers. However, I have concerns about this approach as the total number of papers to be classified is approximately 230,000. I am unsure about the effectiveness of fine-tuning with such a small sample size.

I have also tried using other Transformer-based models like BART for Zero-Shot classification. While this method is entirely free, the results have been unsatisfactory.



