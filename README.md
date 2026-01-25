# Probablistic Deterministic News Analyser & Predictor


###### I’ve created using Grok an updated visualizer prgoram that can be used in realtime for multiple purposes.


##### * Robust News Analyzer & Risk Visualizer (no scikit-learn)
##### * Works in Colab, local Jupyter, even restricted browser environments
## Run in Google Colab: 
## paste → run cells → enter topic when prompted


example:

<img width="1518" height="982" alt="image" src="https://github.com/user-attachments/assets/8ab6c57a-2be1-4cf5-8131-0d5b9e784f0d" />



### NOTE: You may have to install some dependencies so that Google Collab runs the code correctly without crashing.

### If you run into issues try using this as the very first cell, run it to install the dependencies required:

#### !pip install feedparser requests beautifulsoup4 nltk scikit-learn matplotlib pandas



Definistions:

VADER (Valence Aware Dictionary and sEntiment Reasoner)

Heuristic risk (or heuristic risk score/assessment) refers to a quick, approximate, rule-of-thumb way of estimating or scoring risk, rather than using a precise, data-heavy, or statistically rigorous model. The "Heuristic Risk" (the orange bars on the plot, averaged at e.g. 37%) is a simple, custom formula I created as a proxy for perceived escalation potential in news coverage. It's not a formal probability from a trained ML model or historical data simulation — it's a practical shortcut (heuristic) that combines:60% weight on how negative the VADER sentiment is (stronger negativity → higher risk contribution, since doom-laden language often signals tension). 40% weight on counting hits of escalation keywords (e.g., "war," "attack," "nuclear," "strike") — more hits push the score up. Clamped to 0–1 scale for easy interpretation (0 = no risk vibe, 1 = extreme alarm in the text).


