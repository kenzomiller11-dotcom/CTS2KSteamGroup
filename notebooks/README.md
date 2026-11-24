# Analysis notebooks

## Canonical working notebook

[Steam_Reviews_D2_VS_Warframe.ipynb](Steam_Reviews_D2_VS_Warframe.ipynb)

The setup includes the latest annotated notebook available in the project
conversation. Its 31 code cells, calculations and saved outputs are retained.

## Run it in Google Colab

1. Open the notebook in Google Colab using its GitHub URL or upload it.
2. Run the first cell and upload both original Excel files.
3. Confirm the filenames match the [data guide](../data/README.md).
4. Run the remaining cells from top to bottom.
5. Keep the downloaded Destiny and Warframe CSVs in `results/tables/`.
6. Save the notebook back to the working branch and describe the change.

`google.colab.files` is specific to Colab. The current notebook is not
promised to run unchanged in local Jupyter or Codespaces. Repository setup
runs there using standard Python; analysis still uses the Colab workflow.

## Important steps

- Example review cleaning and word counts.
- Destiny recommendation split and normalized keyword frequencies.
- Warframe recommendation split and review percentages.
- A broader spending-word list and contextual review inspection.
- Five sampled Destiny matches and all two Warframe matches, manually coded.
- Separate CSV exports and a final manual-check comparison table.

## Presentation notebook

Not prepared yet. Build the final live notebook from the working analysis
once the question, chart and findings are agreed. Follow the three sections
in [the presentation plan](../presentation/run_of_show.md). Avoid competing
files named final_v2/final_final; use Git history and clear notebook roles.
