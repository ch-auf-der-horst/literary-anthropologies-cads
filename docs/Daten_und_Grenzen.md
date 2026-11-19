# Data and limitations

## Case index and selection

[belegstellen_v12.csv](../data/belegstellen_v12.csv) documents the 21 main contributions, two additional comments and one additional report. Its fields record case ID, evidence type, manuscript section, material, speaker role, year, source location, evidential function, scope, public source URL and verification status. The [case-index guide](Belegstellen_v12.md) explains source checking; [Materials and selection](Material_und_Auswahl.md) describes the selection stages. German field names are explained in the [data guide](../data/README.md).

[de_selection.csv](../data/de_selection.csv) records the 55 German candidates with an AI connection, their use and source checksums. [article_sources.csv](../data/article_sources.csv) links IDs from the earlier German and Chinese coding collections to sources. An online source may differ from its archived version.

## Word-form data

[de_document_counts.csv](../data/de_document_counts.csv) contains 49 articles in each of two text versions. `adopted` denotes the checked article bodies, including two retained closing components. `without_english_story` additionally removes the 1,217 tokens of the English model-generated story in DE-160. Each article has a portal identifier, token count, counts of fourteen word forms, and `mixed` and `summary` flags for two selection variants. Document frequency is calculated from counts greater than zero. [tokenization.json](../data/tokenization.json) describes the counting rule; there is no lemmatisation.

These data allow recalculation of aggregation, normalisation, document frequency and the retained G² comparisons. [expected_frequencies.json](../data/expected_frequencies.json) contains the aggregate reference from the earlier article-checking report. [historical_and_stress_reference.json](../data/historical_and_stress_reference.json) preserves historical comparison values and an additional metadata stress test. The latter is available only as an aggregate result and is not reproduced from its own case-level inputs. The scripts write outputs to [results/](../results/).

Extraction and tokenisation of the original articles are not fully reproducible without the private source archive. The word distributions used in manuscript v12 guide contextual reading; they measure neither the evaluation expressed in a use nor anthropological positions. No new keyness or collocation analysis was conducted for v12.

## Historical categories and thematic families

[family_assignments.json](../data/family_assignments.json) contains the earlier primary assignments of 32 Chinese core texts, 23 German BookTok A-cases and eleven English A-cases. One German A-case has no primary assignment. Recounting this file does not constitute recoding. Definitions and names are provided in `cn_family_definitions.json`, `de_category_definitions.json` and `booktok_family_names.json` under [data/](../data/).

These working categories belong to the earlier exploratory analysis. In particular, the Chinese family summaries are not additionally validated claims about national discourse. The historical German selection stages of 30 and 29 entries overlap; they do not necessarily represent 59 distinct texts. Their category descriptions contain historical case lists, not a new complete assignment of all additional texts. The current argument’s analytical dimensions and 21 close readings are distinguished from these categories. Original category labels and descriptions are retained in German to preserve the analytical record.

## Figures and provenance

[Figure 1](../figures/figure_1/README.md) shows selection pathways with separate denominators for DE, CN and BookTok. [Figure 2](../figures/figure_2/README.md) is a selective interpretative synthesis without a frequency claim. Both folders include source data and generation scripts. Their `manifest.json` files and the repository-wide [SHA256SUMS.json](../SHA256SUMS.json) record file integrity.

[Quellprovenienz.json](Quellprovenienz.json) records relative identifiers and checksums of earlier private input files. This documents their versions at that time, not public availability. Earlier manuscript labels in that provenance file identify the stage at which the data were produced.

## Publication scope

The repository contains selected research data, source references, calculation scripts and figures. It excludes third-party article full texts, complete captions and transcripts, videos, private identification keys, API keys, correspondence and manuscript drafts. The complete retrieval archive, all open coding tables and historical API run logs are also outside this publication.
