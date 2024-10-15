# Movie Review Analysis Tool

This project is a Python-based tool that analyzes movie reviews from web pages and determines the presence or absence of specific review elements. The elements include movie release year, opening details, graphics, summary, plot synopsis, aspect evaluation, and conclusion.

## Short Description
A Python script that scrapes movie reviews from specified URLs, analyzes them for predefined review elements, and presents the results in a tabular format, with an option to save the output as a CSV file.

## Features
- Scrapes movie reviews from given URLs using BeautifulSoup.
- Analyzes the content to check for the presence of predefined review elements.
- Presents the results in a tabular format, showing which elements are present or absent in each review.
- Outputs the analysis as a CSV file for further examination or documentation.

## Setup

### Requirements
- Python 3.x
- Required Python libraries:
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - `IPython` (for displaying the DataFrame in Jupyter or Google Colab)

You can install the required packages by running:

```sh
pip install requests beautifulsoup4 pandas
```

## Usage

1. Clone this repository to your local machine:

```sh
git clone <repository_url>
```

2. Add the URLs of the movie reviews you want to analyze in the `review_links` list in the code. For example:

```python
review_links = [
    "https://www.rogerebert.com/reviews/daddys-head-shudder",
    "https://www.commonsensemedia.org/movie-reviews/lonely-planet",
    "https://www.commonsensemedia.org/movie-reviews/girl-haunts-boy",
    "https://ew.com/queer-review-daniel-craig-luca-guadagnino-pretentious-visually-appealing-slog-8710060",
    "https://ew.com/the-order-review-jude-law-nicholas-hoult-face-off-solid-crime-thriller-8709204"
]
```

3. Run the Python script. If you are using Google Colab or Jupyter Notebook, you can execute it step-by-step.

4. The script will scrape the reviews, analyze them, and display the analysis in a tabular format. The DataFrame will also be saved as a CSV file (`movie_review_analysis.csv`) if needed.

## Project Structure
- `movie_reviews_analysis.py`: The main script that performs the scraping and analysis.
- `movie_review_analysis.csv`: The output CSV file containing the analysis of the movie reviews.

## How It Works
The script extracts relevant information from movie review web pages using BeautifulSoup. It then analyzes whether the content contains certain predefined elements, such as movie release year, summary, or plot synopsis. The presence of each element is displayed in a DataFrame.

The review elements being checked are:
1. **Movie Year**: Information about the movie's release year.
2. **Opening**: Names of actors, directors, producers, companies, etc.
3. **Graphics**: Screenshots or visual scenes mentioned in the review.
4. **Summary**: General summary of the movie and its genre.
5. **Plot Synopsis**: Storyline and context for the movie.
6. **Aspect Evaluation**: Evaluation of acting, cinematography, audio, pacing, etc.
7. **Conclusion**: Reviewer opinions on who may like or dislike the movie, and its strengths or weaknesses.

The tool checks for keywords associated with each of these review elements in the scraped HTML content.

## Notes
- Make sure the URLs provided are valid movie review pages.
- The analysis depends on keyword matching, which means results may vary based on the review's format and vocabulary.
- To ensure compatibility, run the script in an environment where all required libraries are installed.

## License
This project is licensed under the MIT License.

## Contributing
If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are welcome.

## Contact
For any questions or issues, feel free to reach out or create an issue on GitHub.
