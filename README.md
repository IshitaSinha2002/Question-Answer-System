<h1>Question Answering System (Mini QA Bot)</h1>

<h2>Overview</h2>
<p>This project focuses on building a Question Answering (QA) system using Natural Language Processing (NLP).
The system takes a context (paragraph) and a question as input, and returns the most relevant answer extracted from the context.</p>
<p>The model is based on TF-IDF similarity and identifies the most relevant sentence that answers the given question.</p>

<h2>Objective</h2>
<ul>
  <li>Build a QA system that answers questions from a given context</li>
  <li>Understand text similarity using TF-IDF</li>
  <li>Implement extractive question answering</li>
  <li>Evaluate model performance on real dataset</li>
</ul>

<h2>Dataset</h2>
<p>Link: https://www.kaggle.com/datasets/stanfordu/stanford-question-answering-dataset</p>
<p>The dataset used is the Stanford Question Answering Dataset (SQuAD v1.1).</p>
<p>It contains paragraphs along with questions and corresponding answers.</p>

<ul>
  <li>Context (paragraph)</li>
  <li>Question</li>
  <li>Answer (text span from context)</li>
</ul>

<p>Dataset Files:</p>
<ul>
  <li>train-v1.1.json</li>
  <li>dev-v1.1.json</li>
</ul>

<h2>Tech Stack</h2>
<ul>
  <li>Python</li>
  <li>Pandas, NumPy</li>
  <li>Scikit-learn</li>
  <li>Natural Language Processing (NLP)</li>
</ul>

<h2>Data Preprocessing</h2>
<p>The dataset is originally in JSON format and was converted into a structured tabular format.</p>
<ul>
  <li>Extracted context, question, and answer fields</li>
  <li>Converted nested JSON into a DataFrame</li>
  <li>Cleaned text by removing special characters and converting to lowercase</li>
</ul>

<h2>Model Approach</h2>

<h3>TF-IDF Based Similarity Model</h3>
<ul>
  <li>Split context into individual sentences</li>
  <li>Convert sentences and question into TF-IDF vectors</li>
  <li>Compute cosine similarity between question and each sentence</li>
  <li>Select the most relevant sentence as the answer</li>
</ul>

<p>This approach is extractive and selects existing text rather than generating new content.</p>

<h2>Model Evaluation</h2>
<p>The model is evaluated using a simple accuracy metric:</p>
<ul>
  <li>Check if the actual answer text is present in the predicted sentence</li>
</ul>

<p>This provides an approximate measure of performance.</p>

<h2>Sample Input and Output</h2>

<p>
<b>Context:</b> Super Bowl 50 was won by the Denver Broncos.<br>
<b>Question:</b> Who won Super Bowl 50?<br>
<b>Output:</b> Super Bowl 50 was won by the Denver Broncos.
</p>

<h2>Key Insights</h2>
<ul>
  <li>TF-IDF effectively captures keyword-based similarity</li>
  <li>The model works well for direct factual questions</li>
  <li>Performance depends on sentence structure and wording</li>
  <li>The model retrieves sentences, not exact answer spans</li>
</ul>

<h2>Limitations</h2>
<ul>
  <li>Does not extract precise answer spans</li>
  <li>Fails for complex or paraphrased questions</li>
  <li>Limited understanding of context semantics</li>
</ul>

<h2>Future Work</h2>
<ul>
  <li>Implement BERT-based Question Answering</li>
  <li>Improve answer extraction to phrase-level</li>
  <li>Enhance semantic understanding</li>
  <li>Deploy as an API or chatbot</li>
</ul>

<h2>Conclusion</h2>
<p>This project demonstrates how a basic QA system can be built using TF-IDF and cosine similarity.
It highlights the importance of text representation and similarity in NLP tasks and provides a strong foundation for more advanced models.</p>
