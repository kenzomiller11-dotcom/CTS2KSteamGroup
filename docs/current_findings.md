# Current findings and limitations

**Evidence status:** these are the saved outputs in the supplied working
notebook. The original spreadsheets were not available for a complete fresh
run during setup. Reproduce and verify before using the figures as final.

## Review groups with non-missing text

| Game | Recommended | Not recommended | Total with text |
| --- | ---: | ---: | ---: |
| Destiny 2 | 521 | 476 | 997 |
| Warframe | 938 | 60 | 998 |

Each spreadsheet originally contains 1,000 rows. The excluded-text counts
are 3 for Destiny and 2 for Warframe in the saved outputs.

## Percentage of reviews mentioning the exact token `money`

| Game | Recommendation | Matches | Group total | Percentage |
| --- | --- | ---: | ---: | ---: |
| Destiny 2 | Recommended | 16 | 521 | 3.07% |
| Destiny 2 | Not recommended | 85 | 476 | 17.86% |
| Warframe | Recommended | 21 | 938 | 2.24% |
| Warframe | Not recommended | 1 | 60 | 1.67% |

## Broader spending-keyword search

| Game | Recommendation | Matching reviews | Group total | Percentage |
| --- | --- | ---: | ---: | ---: |
| Destiny 2 | Recommended | 54 | 521 | 10.36% |
| Destiny 2 | Not recommended | 173 | 476 | 36.34% |
| Warframe | Recommended | 62 | 938 | 6.61% |
| Warframe | Not recommended | 2 | 60 | 3.33% |

Each review is counted once if it matches at least one spending keyword.
These are percentages of reviews, unlike the earlier per-1,000-word table.

## Manual review checks

| Game | Negative keyword matches | Checked | Coded as clear monetization complaints |
| --- | ---: | ---: | ---: |
| Destiny 2 | 173 | 5, sampled with seed 42 | 5 |
| Warframe | 2 | Both matching reviews | 0 |

The Warframe reviews concern quest design/time spent waiting and a ban/
support issue. The labels are manual judgements encoded in the notebook;
no classifier produced them. The lists of labels depend on those same
examples in the same order and must be checked if inputs change.

## Interpretation supported by these results

Spending keywords occur more often in the negative Destiny group in this
dataset. Reading the matches shows why the terms need contextual checking:
a word such as `spend` can refer to time, and a mention of money can appear
in a complaint about a ban. Keyword matches are not complaint counts.

## Limits to keep in the paper and presentation

- Five checked Destiny reviews are not an estimate of complaints across all
  476 negative Destiny reviews or all Steam players.
- No pricing complaints in two checked Warframe matches does not establish
  that Warframe has no monetization complaints.
- The games have very different recommendation-group sizes.
- Exact keywords can miss synonyms and capture unrelated uses.
- First matching examples are illustrative, not random samples.
- Review labels can coexist with mixed or ironic opinions.
- Historical collection and relevance ordering limit representativeness.
- No causal relationship or current game-quality ranking is established.
- The current notebook does not complete the broader gameplay/story scope.

## Suggested chart task — not yet implemented

Make a grouped bar chart showing the percentage of reviews matching the
broader spending list, by game and recommendation status. Display group
sizes and label it as keyword mentions, not confirmed complaints. Reproduce
the source counts first and use methods the group can explain.
