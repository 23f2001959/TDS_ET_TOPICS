## 1. Python Execution, Packaging & uv

* **Running scripts**: Python files are executed using `python file.py` or `uv run file.py`.
* **uv**: A modern Python package & environment manager.
* **Dependency files**:

  * `pyproject.toml` → modern standard for Python metadata & dependencies
  * `requirements.txt` → traditional dependency list
* **Installing packages with uv**: `uv add package-name`
* **Updating packages**: via `uv pip install -U package`
* **main.py**: Entry point of a Python program
* **json module**: Parses & generates JSON data
* **Linters**: Check code quality, errors, and style issues

---

## 2. Web Development Basics (HTML, CSS, JSON)

* **HTML**: Structure of web pages
* **CSS**: Styling HTML (`p {}` selects all `<p>` elements)
* **JSON**: Data format used mainly for APIs
* **Markdown (`.md`)**: Used for formatted documentation (README, docs)
* **Static websites**: Hosted using GitHub Pages or Vercel

---

## 3. JavaScript Tooling & Formatting

* **Prettier**: Code formatter

  * Command: `npx prettier --write .`
* **npx**: Runs JS packages without global installation
* **package management**: Node ecosystem tools used for formatting, builds, etc.

---

## 4. Git & GitHub (Version Control)

* **Git**: Distributed version control system
* **Key commands**:

  * `git init` → initialize repo
  * `git clone` → copy repo
  * `git status` → see file changes
  * `git add .` → stage changes
  * `git commit -m` → commit with message
  * `git pull` → fetch + merge
  * `git branch` → show branches
  * `git log` → commit history
* **.gitignore**: Prevents files from being tracked
* **GitHub CLI**: `gh repo create`
* **GitHub Pages**: Hosts static sites
* **README.md**: Project documentation

---

## 5. Terminal & Unix Commands

* **File & directory commands**:

  * `ls` / `ls -a` → list files
  * `pwd` → current directory
  * `cd ..` → move up
  * `mkdir` → create directory
  * `touch` → create empty file
  * `rm` → delete file
  * `cat` → display file contents
  * `echo` → print text/variables
* **man**: Opens manual pages
* **Bash scripts**: `.sh` extension

---

## 6. VS Code Usage

* **Ctrl + Shift + P** → Command Palette
* **Ctrl + ,** → Settings
* **Ctrl + `** → Integrated Terminal
* **.vscode folder**: Editor & extension settings
* **settings.json / extensions.json**: VS Code configuration

---

## 7. Browsers & Debugging

* **DevTools Network tab**: Inspect web requests
* **Console tab**: Logs & debugging
* **Swagger UI**: Preview FastAPI docs

---

## 8. FastAPI & Backend

* **FastAPI**: Python web framework
* **@app.get("/")**: Defines GET API route
* **uvicorn**: ASGI server to run FastAPI

  * Default port: `8000`
  * Command: `uvicorn main:app`
* **ngrok**: Exposes local server publicly

---

## 9. Jupyter & Google Colab

* **.ipynb files**: Jupyter notebooks (Python)
* **Google Colab**: Cloud notebook environment
* **Drive access**: `from google.colab import drive`
* **Package install**: `!pip install package`

---

## 10. Docker & Containers

* **Dockerfile**: Instructions to build container images
* **Key instructions**:

  * `FROM` → base image
  * `COPY` → copy files
  * `CMD` / `ENTRYPOINT` → default command
  * `EXPOSE` → expose ports
* **docker build .** → build image
* **docker run -d** → run container in background
* **docker ps** → list running containers
* **docker stop** → stop container
* **.dockerignore**: Exclude files from build context
* **Docker image format**: `.tar`
* **Docker Compose**:

  * `image:` → container image
  * `volumes:` → mount folders

---

## 11. CI/CD & GitHub Actions

* **CI/CD**: Automates testing & deployment
* **GitHub Actions**:

  * Config files: `.github/workflows/*.yml`
  * Uses YAML syntax
  * Default runner: Ubuntu
* **Jobs & steps syntax**:

  ```
  jobs:
    build:
      steps:
        - run: command
  ```

---

## 12. Deployment Platforms

* **Vercel**:

  * Serverless deployment
  * `vercel deploy`
  * Config file: `vercel.json`
  * Best for frontend & APIs
* **GitHub Pages**: Markdown/static deployment
* **MkDocs**:

  * `base_url` → documentation root path

---

## 13. Images & Compression

* **Image formats**:

  * JPG → lossy photos
  * PNG → screenshots
  * SVG → vector graphics
  * WEBP → smallest web-optimized format
* **cwebp**: CLI tool for WebP compression

  * `-q 80` → quality level
* **PIL**: Python image processing library

---

## 14. Miscellaneous Core Concepts

* **Terminal emulator**: Terminal, VS Code terminal
* **pwd vs ls**: location vs contents
* **Markdown**: Docs, README, formatting
* **Llamafile**: Run local LLMs
* **serve (Vercel)**: Static hosting
* **requirements.txt**: Deployment dependencies list

---
### **15. LLM Fundamentals**

* **Embeddings**: Numerical vectors representing semantic meaning of text.
* **Tokenizers**: Split text into tokens (sub-words) for model processing.
* **Tokens**: Unit of billing and context length.
* **Temperature / top_p**: Control randomness and diversity.
* **max_tokens**: Limits output length.
* **System message**: Sets assistant behavior.
* **Prompt**: Input instruction to the model.
* **Hallucination**: Confident but incorrect output.

---

### **16. OpenAI Models & APIs**

* **GPT**: Generative Pre-trained Transformer.
* **gpt-4o**: Multimodal (text, vision, audio), faster, 128k context.
* **gpt-4-turbo**: Best for extraction tasks.
* **Embeddings API**: `/v1/embeddings`
* **Chat API**: `/v1/chat/completions`
* **Streaming**: Partial outputs returned incrementally.
* **Model parameter**: Specifies which model to use.
* **Lower cost models**: Used for summarization and basic tasks.

---

### **17. Structured Outputs & Function Calling**

* **Function calling**: Enables structured API outputs.
* **tools**: Define available functions.
* **tool_choice**: Forces a specific function call.
* **JSON schema**: Validates structured responses.
* **json mode**: Ensures machine-readable JSON output.
* **Arguments dictionary**: Returned by function calls.

---

### **18. Embeddings & Vector Search**

* **Vector dimension**: Depends on the model (e.g., 1536).
* **Embedding output**: List of floats.
* **Cosine similarity**: Measures vector similarity (-1 to 1).
* **Vector databases**: Store embeddings for fast search.
* **Embedding search**: Retrieves similar documents.
* **Chunking**: Splitting long text into parts.
* **Token overlap**: Shared tokens between chunks.
* **RAG**: Enhances LLMs using external knowledge.

---

### **19. Multimodal & Media Handling**

* **Vision models**: gpt-4o supports image input.
* **Image input format**: Base64 or URL.
* **Base64 encoding**: Embed binary data in text.
* **Multimodal inputs**: Text, image, audio together.

---

### **20. Prompt Engineering**

* **Zero-shot prompting**: No examples provided.
* **Few-shot prompting**: Examples included.
* **Key challenge**: Avoid hallucinations.
* **Best summarization strategy**: Use TL;DR prompts.

---

### **21. Data Sourcing & Web Scraping**

* **HTML**: Semi-structured data.
* **Scraping challenges**: Site structure changes, rate limiting.
* **Headers**: Imitate browser requests.
* **Dynamic pages**: Require JavaScript rendering.
* **Delays**: `time.sleep()` avoids detection.
* **Legal risks**: IP bans, legal notices.
* **Selectors**: CSS patterns for element selection.

---

### **22. Scraping Tools & Libraries**

* **BeautifulSoup**: HTML parsing.
* **Selenium**: Browser automation.
* **Scrapy**: Large-scale scraping.
* **Tabula**: Extract tables from PDFs.
* **Tesseract**: OCR for PDFs.
* **GitHub Actions**: Automate scraping jobs.
* **pandas.read_html()**: Extract HTML tables.

---

### **23. APIs & Data Formats**

* **REST APIs**: Common data access method.
* **JSON**: Most reliable API format.
* **GeoJSON**: Geospatial data.
* **Nominatim**: Geographic data API.
* **MediaWiki API**: Wikipedia access.
* **PokeAPI**: Pokémon data.
* **Weather APIs**: Example REST endpoints.

---

### **24. Data Cleaning & Preparation**

* **OpenRefine**: Visual data cleaning tool.
* **dropna()**: Remove missing values.
* **fillna()**: Fill missing values.
* **replace()**: Substitute values.
* **astype()**: Type conversion.
* **Normalization**: Scale values.
* **Outlier removal**: IQR, z-score.
* **Regex**: Pattern-based transformation.

---

### **25. Pandas Core Operations**

* **DataFrame**: 2D labeled structure.
* **read_csv / read_excel**: Load data.
* **info()**: Dataset summary.
* **head()**: First rows.
* **groupby()**: Aggregation.
* **apply() / map()**: Apply functions.
* **sort_values()**: Sort data.
* **drop_duplicates()**: Remove duplicates.

---

### **26. Excel & Google Sheets**

* **WEBSERVICE()**: Fetch web data (Excel).
* **IMPORTXML()**: Fetch web data (Sheets).
* **TEXTSPLIT / Text to Columns**: Split text.
* **TRIM()**: Remove whitespace.
* **SUBSTITUTE()**: Replace characters.
* **FORECAST() / Forecast Sheet**: Predict values.
* **Pivot tables**: Summarize data.
* **ISBLANK()**: Check empty cells.

---

### **27. Automation & Workflow Tools**

* **Apache Airflow**: Workflow orchestration (DAGs).
* **DAG**: Directed Acyclic Graph.
* **DuckDB**: SQL on local files.
* **Bash tools**: `sort | uniq`, `cat *.csv`
* **GitHub Actions**: CI/CD and automation.

---

### **28. Data Analysis & Visualization**

* **Line chart**: Trends over time.
* **Scatter plot**: Correlation.
* **Histogram**: Distribution.
* **Correlation (CORREL)**: Relationship strength.
* **Regression (R²)**: Goodness of fit.
* **statsmodels**: Statistical analysis.
* **seaborn regplot**: Regression visualization.

---

### **29. File Formats & Utilities**

* **CSV**: Most scraping-friendly format.
* **PNG / JPEG / WebP**: Image formats.
* **HTML tables**: Common scraped data.
* **Markdown**: Documentation format.
* **Pathlib**: File path handling.

---

### **30. Core Programming Concepts**

* **Lambda**: Anonymous function.
* **enumerate()**: Index + value iteration.
* **split()**: String to list.
* **json.loads()**: JSON → Python.
* **os module**: File/system operations.

---

#### These topics together form the **end-to-end data lifecycle**:

> **Collect → Scrape → Clean → Store → Analyze → Enhance with LLMs → Automate**

---

Below is a **complete, compact, concept-wise summary** covering **ALL questions 266–350**.
✅ **Nothing is skipped**
✅ **Numbering starts from 31**, exactly as you asked
✅ Written in **exam / viva / revision-ready language**

---

## **31. SQL Core Analytics**

* **SELECT DISTINCT**: Removes duplicate rows.
* **AVG()**: Calculates average value.
* **JOIN**: Combines multiple tables.
* **Mean in SQL**: `SELECT AVG(column)`
* **Duplicate detection**: `DISTINCT`, `duplicated()` (pandas equivalent)

---

## **32. Pandas Statistical Operations**

* **.mean()**: Computes average.
* **.median()**: Middle value.
* **.describe()**: Summary statistics.
* **.groupby()**: Group + aggregate data.
* **.value_counts()**: Frequency of values.
* **.corr()**: Correlation matrix.
* **.quantile()**: Percentile values.
* **.nlargest()**: Top N values.
* **.pivot_table()**: Aggregated summary.
* **pd.crosstab()**: Cross-tabulation.
* **duplicated()**: Identify duplicate rows.

---

## **33. Correlation & Regression Analysis**

* **Correlation matrix**: Relationship strength between variables.
* **Negative correlation**: One increases, the other decreases.
* **Regression analysis**: Cause-effect relationship.
* **Linear regression**: `LinearRegression` (sklearn).
* **Logistic regression**: Classification tasks.
* **Multicollinearity**: Predictors correlated with each other.
* **Normality test**: Shapiro-Wilk test.

---

## **34. Outliers & Anomaly Detection**

* **Outlier**: Data point far from others.
* **Isolation Forest**: Anomaly detection method.
* **Boxplot**: Visualizes outliers and distribution.

---

## **35. Time Series Analysis**

* **prophet**: Time series forecasting.
* **.resample()**: Change time frequency.
* **Trend visualization**: Line charts with trendlines.

---

## **36. Geospatial Analysis**

* **geopandas**: Geospatial mapping in Python.
* **QGIS integration**: `qgis`
* **Maps & spatial data**: Coordinates, regions, layers.

---

## **37. Core Visualization Libraries**

* **matplotlib**: Base plotting library.
* **seaborn**: Statistical visualization.
* **plotly**: Interactive & customizable charts.
* **bokeh**: Real-time interactive plots.
* **Dash**: Dashboard creation.

---

## **38. Distribution & Comparison Charts**

* **Histogram**: Distribution of values.
* **Bar chart**: Categorical comparison.
* **Boxplot**: Distribution + outliers.
* **Pie chart**: Proportions.
* **Treemap**: Relative proportions.
* **Donut chart**: Pie chart with center cut-out.

---

## **39. Relationship & Correlation Charts**

* **Scatter plot**: Relationship between variables.
* **Pairplot**: Pairwise relationships.
* **Heatmap**: Intensity & correlation visualization.
* **sns.heatmap()**: Correlation matrix plot.

---

## **40. Time-Based & Forecast Visuals**

* **Line chart**: Trends over time.
* **Candlestick chart**: Stock price movement.
* **Gantt chart**: Timelines.
* **Forecast visuals**: Line + trendline.

---

## **41. Network & Flow Visualizations**

* **Network graph**: Relationships in social/network data.
* **Sankey diagram**: Flow distribution.
* **Flowchart**: Sequential flow.
* **Tree diagram**: Branching logic.
* **Kumu**: Network mapping tool.

---

## **42. Advanced & Multivariate Charts**

* **Radar chart**: Multivariate comparison.
* **Heatmaps**: Multidimensional intensity.
* **SVG**: Vector graphics format.

---

## **43. Visualization Tools & Platforms**

* **RAWGraphs**: Data visualization tool.
* **Flourish**: Drag-and-drop storytelling.
* **Google Data Studio**: Dashboards & maps.
* **Power BI / Excel Quick Analysis**: Rapid summaries.
* **Power Map / 3D Maps**: Time-based animations.

---

## **44. Matplotlib Essentials**

* **Figure**: Core object.
* **plt.bar()**: Bar chart.
* **plt.hist()**: Histogram.
* **plt.title()**: Chart title.
* **plt.xlabel()**: X-axis label.
* **plt.savefig()**: Save chart image.
* **fig, ax = plt.subplots()**: Create figure & axes.

---

## **45. Storytelling & Narrative Visualization**

* **Narrative visualization**: Data storytelling.
* **Animated transitions**: Flourish story feature.
* **Dashboards**: Monitor KPIs visually.
* **KPI cards / gauges**: Single key metric focus.

---

## **46. File Formats & Output Quality**

* **SVG**: Vector charts.
* **PDF / SVG**: High-quality prints.
* **.svg extension**: Vector visuals.

---

## **47. Interactive & Educational Tools**

* **Jupyter / Marimo**: Visualize code execution.
* **Interactive dashboards**: Dash, Plotly, Bokeh.

---

## **48. Dashboard Concepts**

* **Dashboard purpose**: Summarize & monitor data visually.
* **Real-time visuals**: Interactive updates.
* **Executive summaries**: KPI-focused views.

---

## **49. Chart Selection Best Practices**

* **Distribution** → Histogram / Boxplot
* **Relationship** → Scatter / Pairplot
* **Trend** → Line chart
* **Proportion** → Pie / Treemap
* **Flow** → Sankey
* **Network** → Network graph

---

#   T D S _ E T _ T O P I C S  
 