# oscar_predictions
Predicting Oscar winners across 6 major categories from nominations, guild and precursor awards, and film/career history.

> **Status** In progress.

## The question
Each year, a few thousand Academy members vote for the winners of the Oscars from a short list of nominees. Before that happens, there are months of public signals as to who might win: guild awards, critics' awards, box office, festival buzz, and campaigns.

**Can those signals predict the winner, how confident should we be, and where do they fail?**

## Scope
| Category | Strongest expected precursor |
|---|---|
| Best Picture | PGA, DGA, total nomination count |
| Best Director| DGA |
| Best Actor | SAG, BAFTA |
| Best Actress | SAG, BAFTA |
| Best Supporting Actor | SAG, BAFTA |
| Best Supporting Actress | SAG, BAFTA |

Original and Adapted Screenplay (WGA) may be added later.

## Features (planned)

| Group | Examples |
|---|---|
| Oscar nominations | Total nominations; Director, Editing, and Screenplay nominations |
| Precursor awards | DGA, PGA, SAG, WGA, BAFTA, Golden Globes, Critics Choice (nominations and wins) |
| Person history | Prior Oscar nominations and wins, an "overdue" flag, wins for other work |
| Release and campaign | Release month, fall festival premiere, distributor |
| Film profile | Genre, runtime, biopic / true story, critic scores |
| Box office | Pre-nomination gross relative to genre |
| Role type *(stretch)* | Played a real person, physical transformation, illness: pulled from plot summaries with an LLM |

Features will be added in iterations

## Data sources

| Source | Used for | Access |
| Academy Awards database / public nominee dataset | Nominees and winners | CSV |
| Wikipedia ceremony pages | Precursor award results | Scraped (MediaWiki API) |
| IMDb non-commercial datasets | Film and person metadata | Downloadable files |
| TMDB | Release dates, genres, budgets | Free API |
| OMDb | Rotten Tomatoes and Metacritic scores | Free API |

## Results
*Coming soon.*

## Limitatoins
- **Small data:** about 95 ceremonies x 6 categories. Precursor awards also cover fewer years so the usable history is shorter than it looks.
- **Changing electorate:** the Academy's makeup has changed over the years, so the predictability of the future could be affected by this
