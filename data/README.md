# Data guide

The empirical files retain their original field names, source titles, case descriptions and historical coding labels. This preserves their connection to the German-language manuscript and the archived analytical record. The surrounding repository documentation is in English.

## Case index

[belegstellen_v12.csv](belegstellen_v12.csv) is a UTF-8 CSV file with 24 data rows. Its columns mean:

- `fall_id`: stable internal case ID, used in the manuscript and figures.
- `belegtyp`: evidence type. `Hauptbeitrag` means main contribution (21 rows); `Ergänzende Kommentarreaktion` means additional comment (two rows); `Ergänzender Bericht` means additional report (one row).
- `kapitel`: manuscript section number; multiple sections are separated by semicolons.
- `material`: type of material, such as review, interview, production report, caption or transcript.
- `sprecherrolle`: speaker role, distinguishing the author, interviewed speakers, quoted model output and journalistic framing where relevant.
- `jahr`: year associated with the contribution.
- `fundstelle`: location of the evidence within the source.
- `belegfunktion`: the passage’s function in the argument.
- `reichweite`: the scope and limits of the inference supported by the evidence.
- `quellen_url`: public source URL. Blank entries for BookTok posts are intentional; private account and post mappings are not published.
- `pruefstand`: verification status. The entries distinguish checks against archived articles or textual layers from online checks dated 18 November 2026.

The `DE`, `CN` and `BT` prefixes identify the German portal, Chinese and BookTok material. `BT-DE` and `BT-EN` distinguish the language subsets. A-cases form the retained BookTok core; B-cases are contrast material. The 21 main contributions are a purposive selection from larger exploratory collections, as explained in [Materials and selection](../docs/Material_und_Auswahl.md).

## Other files

- [de_selection.csv](de_selection.csv): German AI-related candidates, inclusion decisions and source checksums.
- [de_document_counts.csv](de_document_counts.csv): document-level token and word-form counts for two versions of the 49 German article bodies.
- [article_sources.csv](article_sources.csv): source references for the historical German and Chinese coding collections.
- [tokenization.json](tokenization.json): counting rule and fourteen word forms.
- [family_assignments.json](family_assignments.json): historical Chinese and BookTok thematic family assignments.
- [cn_family_definitions.json](cn_family_definitions.json), [de_category_definitions.json](de_category_definitions.json) and [booktok_family_names.json](booktok_family_names.json): retained exploratory definitions and labels.
- [expected_frequencies.json](expected_frequencies.json): aggregate reference for the reproduced comparisons.
- [historical_and_stress_reference.json](historical_and_stress_reference.json): historical comparison values and an aggregate metadata stress test.

For the distinction between the current case analysis and earlier exploratory categories, and for limits on reproduction, see [Data and limitations](../docs/Daten_und_Grenzen.md).
