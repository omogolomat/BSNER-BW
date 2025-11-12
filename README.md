# BSNER-BW
Botswana-centric Named Entity Recognition (NER) dataset for Setswana.
# BSNER-BW: A Botswana-Focused NER Dataset for Setswana

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Release: June 2026](https://img.shields.io/badge/Release-June%202026-blue)](#release)
[![Format: CoNLL-U](https://img.shields.io/badge/Format-CoNLL--U-green)](#data-format)
[![Language: Setswana](https://img.shields.io/badge/Language-Setswana-orange)](#)

> The first publicly available, Botswana-centric Named Entity Recognition (NER) dataset for Setswana.

---

## Public Release: June 2026

This repository is currently in pre-release.

The dataset is fully annotated and complete (delivered as part of Semester 1, 2025), but the files will be made publicly downloadable in June 2026.

Until then, this README serves as the official documentation and citation source.

---

## Overview

BSNER-BW is a unified, reproducible NER resource integrating all components from the research (Sections 3.1–3.7):

| Feature | Details |
|-------|--------|
| Size | 30 documents, ~8,000 tokens |
| Domain Split | 73% news, 27% government |
| Annotation | IOB scheme, 6 entity types, $\kappa = 0.84$ |
| Auxiliary | 750-entry gazetteer |
|*Format | [CoNLL-U](https://universaldependencies.org/format.html) |
| License | [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) |
| Release | June 2026 |
| URL | `(https://github.com/omogolomat/BSNER-BW)` |

---

## Entity Types

| Tag | Description | Example |
|-----|-------------|---------|
| `PER` | Person | Omogolo Matema |
| `ORG` | Organization | Bank of Botswana |
| `LOC` | Location | Gaborone, Okavango |
| `DATE` | Date | 12 Motsheganong 2025 |
| `TIME` | Time | 14:30 |
| `MONEY` | Monetary value | Pula 1,200 |

---

## Data Format

Data will be provided in CoNLL-U format:

```conllu
# sent_id = bw_news_001-1
# text = Omogolo Matema o nnile le Bank of Botswana mo Gaborone.
1	Omogolo	Omogolo	PROPN	PER	_	3	nsubj	_	_
2	Matema	Matema	PROPN	PER	_	1	flat:name	_	_
3	o	o	AUX	_	_	4	aux	_	_
4	nnile	nnile	VERB	_	_	0	root	_	_
5	le	le	ADP	_	_	6	case	_	_
6	Bank	Bank	PROPN	ORG	_	4	obl	_	_
7	of	of	PROPN	ORG	_	6	flat:name	_	_
8	Botswana	Botswana	PROPN	ORG	_	6	flat:name	_	_
9	mo	mo	ADP	_	_	10	case	_	_
10	Gaborone	Gaborone	PROPN	LOC	_	4	obl	_	_
11	.	.	PUNCT	_	_	4	punct	_	_
