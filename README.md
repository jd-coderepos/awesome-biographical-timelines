# Awesome Biographical Timelines [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of research on automatically constructing biographies, biographical knowledge graphs, and person-centric event timelines from text.

## Contents

- [Datasets & Benchmarks](#datasets--benchmarks)
- [Methods](#methods)

## Datasets & Benchmarks

Resources for training or evaluating systems that extract, generate, or reason about biographical information — people, life events, and their timing.

- [WikiBio](https://github.com/DavidGrangier/wikipedia-biography-dataset) - 728,321 English Wikipedia biographies paired with their infobox, tokenized. Built for structured-data-to-text generation (Lebret, Grangier & Auli, EMNLP 2016), but the de facto reference corpus for biography work generally.
- [Pantheon 1.0](https://www.nature.com/articles/sdata201575) - 11,341 manually verified globally-notable biographies with demographic data, an occupation taxonomy, and a Historical Popularity Index. Data at [pantheon.world](https://pantheon.world).
- [EventKG](https://arxiv.org/abs/1804.04526) - Multilingual, event-centric temporal knowledge graph: 690k+ events and 2.3M+ temporal relations mined from Wikidata, DBpedia, YAGO, and Wikipedia event lists.
- [BiographySampo](https://seco.cs.aalto.fi/projects/biografiasampo/en/) - Knowledge graph automatically extracted via NLP from 13,100 Finnish national biographies, ~125,000 events, ~52,000 family relations, published as Linked Open Data. Portal at [biografiasampo.fi](http://biografiasampo.fi).
- [BiographyNet / Biography Portal of the Netherlands](https://arxiv.org/abs/1801.07073) - ~125,000 biographies of ~76,000 individuals from Dutch biographical dictionaries, structured into RDF via a historically-grounded NLP pipeline.
- [Biographical](https://arxiv.org/abs/2205.00806) - Semi-supervised relation-extraction dataset built specifically around biographical relation triples.
- [Guidelines and a Corpus for Extracting Biographical Events](https://arxiv.org/abs/2206.03547) - The first annotation scheme and corpus (1,000 sentences, Wikipedia biographies of underrepresented writers) built explicitly for biographical-event extraction.
- [ADAM (A Diverse Archive of Mankind)](https://arxiv.org/abs/2509.22991) - 2025 benchmark for evaluating LLM biographical reasoning, and the best single index of prior biographical datasets (WikiBio, SynthBio, Pantheon, BiographySampo, EventKG, etc.).
- [Extraction of Historical Events from Wikipedia](https://arxiv.org/abs/1205.4138) - ~121,000 historical events extracted from Wikipedia's "year" articles, linked to 325,000+ DBpedia entities.
- [Examining the State-of-the-Art in News Timeline Summarization](https://arxiv.org/abs/2005.10107) - Introduces the Entities timeline-summarization benchmark (47 topics) and discusses the older, smaller T17 and Crisis datasets.
- [CrisisLTLSum](https://arxiv.org/abs/2210.14190) - Largest benchmark for local-crisis event timeline extraction and summarization from social media.
- [PMOA-TTS](https://arxiv.org/abs/2505.20323) - 124,699 PubMed case reports converted into structured (event, time) timelines by an LLM pipeline. Not biographical, but the closest existing analog to single-research-article-to-person-timeline extraction; see the companion method below.
- FActScore biography benchmark (Min et al., 2023) - 183-entity long-form biography-generation set, the standard testbed for LLM factuality and hallucination evaluation. See the [Ever](https://arxiv.org/abs/2311.09114) paper for one application.

## Methods

Systems and pipelines that turn text into biographical structure — knowledge graphs, event lists, or timelines — spanning classic rule and CRF pipelines through current LLM-prompting approaches.

- [Extracting and Visualising Biographical Events from Wikipedia](https://ceur-ws.org/Vol-1399/paper17.pdf) - The NewsReader pipeline (NER, coreference, temporal normalization) applied to Wikipedia biography text, reconciled against DBpedia infobox values, output as a JSON timeline.
- [BioGen](https://www.researchgate.net/publication/334082235_BioGen_Automated_Biography_Generation) - Automatic biography generation via biographical-sentence classification and SVM-based sentence ordering.
- [EventKG - the Hub of Event Knowledge on the Web - and Biographical Timeline Generation](https://arxiv.org/abs/1905.08794) - Generates person-centric biographical timelines directly from the EventKG temporal knowledge graph.
- [Paths of a Million People](https://ojs.aaai.org/index.php/ICWSM/article/download/35930/38084/39998) - Large-scale spatio-temporal life-trajectory extraction from Wikipedia biography pages (AAAI ICWSM).
- [Extracting Biographical Spatial Timelines: Corpus and Experiments](https://doi.org/10.1109/TASLP.2020.2988418) - Vempala & Blanco; LSTM-based extraction of (location, year) spatial timelines from 100 Wikipedia biographies.
- [TLEX](https://arxiv.org/abs/2406.05265) - Symbolic method that extracts provably exact timelines from TimeML-annotated text via topological sort, rather than statistical ordering.
- [CHRONOS](https://arxiv.org/abs/2501.00888) - LLM-based open-domain timeline generation via iterative self-questioning, retrieval, and event-graph construction; also introduces the Open-TLS dataset of 50 journalist-written timelines.
- [SUnSET](https://arxiv.org/abs/2507.21903) - Stakeholder- and time-aware LLM timeline generation, including a directly reusable prompt template for extracting a dated-event dictionary from a single article.
- [NTS-CoT](https://arxiv.org/abs/2606.13171) - Chain-of-thought prompting designed to reduce hallucination and information omission in LLM-based timeline summarization.
- [Multilingual and Cross-lingual Timeline Extraction](https://arxiv.org/abs/1702.00700) - SemEval-2015-Task-4-based system for cross-document event coreference and time-anchoring.
- [A Large-Language Model Framework for Relative Timeline Extraction from PubMed Case Reports](https://arxiv.org/abs/2504.12350) - Single document to single LLM prompt to structured (event, time) tuples; the closest architectural precedent for a paper-to-timeline pipeline, reporting 0.80 event recall and 0.95 temporal concordance with a single-prompt approach.
- [Critical Confabulation: Can LLMs Hallucinate for Social Good?](https://arxiv.org/abs/2511.07722) - Builds source-bounded, citation-linked chronological timelines for individual people from a document set via a single long-context LLM prompt.
- [KnowledgeTrail](https://arxiv.org/abs/2510.12113) - Generative timeline system for historical-event sensemaking that compares LLM-based against traditional NLP timeline construction.
- [Formulation Comparison for Timeline Construction using LLMs](https://arxiv.org/abs/2403.00990) - Systematically compares prompt and task formulations for LLM-based timeline construction.
- [Extrinsic Hallucinations in LLMs](https://lilianweng.github.io/posts/2024-07-07-hallucination/) - Survey covering FActScore- and SAFE-style factuality evaluation, directly applicable to scoring any biography or timeline generator.
- [A Visual Analytics System for Interactive Exploration of Historical Painter Cohorts](https://arxiv.org/abs/2511.04383) - References TimeScape, a multi-resolution timeline visualization approach for large-scale biographical data.

## Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) first.

**License:** [CC0](https://creativecommons.org/publicdomain/zero/1.0/) - to the extent possible under law, this list has been dedicated to the public domain.
