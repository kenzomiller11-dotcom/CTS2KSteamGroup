# Destiny 2 vs Warframe — Steam Reviews

CTS*2000 group project. We compare recommended and not-recommended Steam reviews.

## Where everything goes

| Item | Location | What belongs here |
| --- | --- | --- |
| Destiny 2 raw dataset | [data/raw/destiny2/](data/raw/destiny2/) | Original `7_Destiny_2_1085660xlsx.xlsx` |
| Warframe raw dataset | [data/raw/warframe/](data/raw/warframe/) | Original `16_Warframe_230410.xlsx` |
| Destiny 2 output | [outputs/destiny_negative_sample_check.csv](outputs/destiny_negative_sample_check.csv) | Saved manual-review results for Destiny 2 |
| Warframe output | [outputs/warframe_negative_sample_check.csv](outputs/warframe_negative_sample_check.csv) | Saved manual-review results for Warframe |
| Working notebook | [notebooks/Steam_Reviews_D2_VS_Warframe.ipynb](notebooks/Steam_Reviews_D2_VS_Warframe.ipynb) | The code that reads and compares both games |

## Step 1: add the two datasets

1. Open each game's raw dataset folder above.
2. Click **Add file → Upload files** and choose that game's Excel file.
3. Keep the original filename and contents, then commit the upload.

Each spreadsheet should contain a sheet named `Reviews`.

## Step 2: run the notebook when ready

1. [Open the working notebook in Google Colab](https://colab.research.google.com/github/kenzomiller11-dotcom/CTS2KSteamGroup/blob/main/notebooks/Steam_Reviews_D2_VS_Warframe.ipynb).
2. Run its upload cell and select both original Excel files from your computer.
3. Run the remaining cells in order. Upload the downloaded CSVs to [outputs/](outputs/) and save your updated notebook back to GitHub.
