<h1>Goal</h1>

<p>
Analyze League of Legends match data and build a model to predict match outcomes using in-game statistics (focusing on the game objectives).
</p>

<hr>

<h2>Dataset used</h2>

<p>
<a href="https://www.kaggle.com/datasets/paololol/league-of-legends-ranked-matches?resource=download">
  <strong>Kaggle – League of Legends ranked matches</strong>
</a>
</p>

<p>
This dataset had gathered a few years' worth of data from competitive LoL matches starting in 2014, so the dataset is quite outdated as the game and meta changes quite frequently, but for the sake of this project, it is well-suited :)
</p>

<hr>

<h2>!! IMPORTANT !!</h2>

<p>
Due to file size constraints of the dataset, raw data is <strong>not included</strong> in the repository.
</p>

<h2>Setup</h2>

<ol>
  <li>
    Download the dataset from:<br>
    <a href="https://www.kaggle.com/datasets/paololol/league-of-legends-ranked-matches?resource=download">
      Kaggle Dataset Link
    </a>
  </li>
  <li>Extract the files into: <code>data/raw/</code></li>
  <li>
    The expected structure is:
    <pre>
ml-analysis-lol/
└── data/
    └── raw/
        └── matches.csv  (7 CSV files in total)
    </pre>
  </li>
</ol>

<p>
The notebooks will handle processing the data, so a folder <code>data/processed</code> will also appear later on.
</p>

<h2>Requirements</h2>

<p>
This project uses Python 3 and the following Python libraries:
</p>

<ul>
  <li>pandas</li>
  <li>numpy</li>
  <li>matplotlib</li>
  <li>jupyter</li>
  <li>seaborn</li>
  <li>scikit-learn</li>
</ul>

<p>
Install the required dependencies by running:
</p>

<pre>
pip install -r requirements.txt
</pre>


<hr>

