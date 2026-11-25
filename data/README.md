# Data guide

## Source

Thomas Byers, *Steam User Review Data – 1,000 Most Recent Reviews from
500 Popular Games*.

- [Dataset page](https://figshare.unimelb.edu.au/articles/dataset/Steam_User_Review_Data_1_000_Most_Recent_Reviews_from_500_Popular_Games/30842609)
- [DOI](https://doi.org/10.26188/30842609.v1)
- [Publisher metadata](https://api.figshare.com/v2/articles/30842609)
- Published: December 15, 2025.
- Collection described by the publisher: December 6, 2023.
- Listed licence: CC0.

Publisher metadata was checked while preparing this setup. It describes
recent reviews and games ordered by organic visibility/relevance at
collection, rather than a random sample of all Steam users. Avoid treating
our subset as representative of all current players.

## Exact input filenames expected by the existing notebook

| Game | File | Sheet |
| --- | --- | --- |
| Destiny 2 | `7_Destiny_2_1085660xlsx.xlsx` | `Reviews` |
| Warframe | `16_Warframe_230410.xlsx` | `Reviews` |

The spelling of the Destiny filename matches the current code. Do not
silently rename it or alter the loader during repository organization.

The source spreadsheets have not been uploaded yet. Put the original Destiny 2 file in
[data/raw/destiny2/](raw/destiny2/) and the Warframe file in
[data/raw/warframe/](raw/warframe/). Keep both filenames and their contents unchanged.
These folders accept dataset files in Git. When running the notebook, select both
spreadsheets in its Google Colab upload cell; it does not load the repository folders automatically.

## Fields used by the current analysis

| Field | Meaning/use |
| --- | --- |
| `review` | Review text; missing values are excluded from text analysis |
| `voted_up` | True = recommended; False = not recommended |

The dataset contains other metadata, but do not claim those fields were
analysed just because they exist. Language filtering and duplicate handling
are not explicitly implemented in the current notebook; document decisions
before adding either.

## Cleaning limitations

`dropna()` removes missing text, not necessarily blank strings. Cleaning
splits on whitespace, trims punctuation at token edges and lowercases.
It does not perform stemming, lemmatization or a complete language filter.
The match for a word is an exact cleaned-token match, so spelling variants
and hyphenation can affect results. Never manually edit raw reviews.
