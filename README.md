# Thesis

## Pipeline

The analysis runs as a sequence of numbered notebooks, grouped into four stages. Everything is fully reproducible except the event clusters in `3.1`, where a random seed was not set, so the embedding clusters differ slightly on re-run.

### 1. Cleaning and EDA

- `1_cleaning.ipynb`: Clean the raw scrape into `stylecom_cleaned.csv`.
- `1.2_eda.ipynb`: Exploratory plots of the cleaned corpus (reviews over time, per-author and per-designer counts, coverage thresholds).

### 2. Topic modelling (RollingLDA)

- `2.1_topic_modelling_preprocessing.ipynb`: Noun-token extraction and the fashion ontology → `df_with_noun_tokens.pkl`.
- `2.2_topic_modelling_general_prep.ipynb`: Vocabulary filtering and term diagnostics → `chosen_vocab.pkl`.
- `2.3_topic_modelling_rlda_initialisation.ipynb`: Init-period and K sweeps (diagnostic; the model is refit in 2.4).
- `2.4_topic_modelling_rlda_fitting.ipynb`: Fit the RollingLDA model → `outputs_rlda_fitting/`.
- `2.5_topic_modelling_inspection.ipynb`: Topic stability, word evolution, and prevalence diagnostics.
- `2.6_topic_modelling_codebook.ipynb`: Top-word tables and representative documents feeding the codebook.
- `2.7_topic_modelling_coding_sample.ipynb`: Stratified 200-review sample for manual coding.
- `2.8_topic_modelling_intercoder_reliability.ipynb`: Merge human, LLM, and model topic labels on the sample.
- `2.9_topic_modelling_llm_annotation.ipynb`: LLM topic assignment for the full corpus → `stylecom_cleaned_annotated.csv`.

### 3. Event chains

- `3.1_events_clustering.ipynb`: Extract verb triples and cluster them into event types → `event_sequences.jsonl`.
- `3.2_order_signal.ipynb`: Test whether the order of events carries signal.
- `3.3_composition_signal.ipynb`: Test whether event composition varies between reviews.
- `3.4_composition_at_scale.ipynb`: Test whether composition differences are organised by year, author, or brand.
- `3.5_composition_maps.ipynb`: Descriptive composition and chain-length maps across units and eras.

### 4. Topic analysis

- `4.1_eda_topics.ipynb`: Topic shares by year and season, and overall prevalence.
- `4.2_topic_prevalence_over_time.ipynb`: Per-topic logistic trend across the corpus period.
- `4.3_topic_order_composition.ipynb`: Topic trajectory position and composition by brand.

## `data/`

The corpus, topic annotations, event/cluster labels, and reference ontologies used across the pipeline.

### Corpus

- `stylecom_raw.csv`: Raw scraped Style.com runway reviews. Columns: year, season, designer, author, city, date, image (HTML), review.
- `stylecom_cleaned.csv`: Cleaned corpus, 6,501 reviews. Columns: year, season, designer, author, city, date, review.
- `stylecom_cleaned_annotated.csv`: Cleaned corpus with a `review_id` and RollingLDA `topic_number` per review (6,501 rows).

### Topic annotation

- `topic_codebook.md`: Coding instructions and the ten-topic (0–9) codebook, including inclusion/exclusion criteria.
- `topic_interpretations.xlsx`: Interpretive notes for the topics.
- `full_llm_annotation.csv`: LLM topic assignment for the full corpus (review_id, topic_number; 6,500 rows).
- `coding_sample_200.csv`: 200-review sample used for the coding exercise.
- `coding_sample_200_intercoder.csv`: Same sample with coder_1, coder_2, llm_coder, and model_assignment columns for inter-coder comparison.
- `coder_1.csv`, `coder_2.csv`: Individual human coder topic assignments on the sample (199 rows each).
- `coder_llm.csv`: LLM coder topic assignment on the sample (review_id, topic_number; 199 rows).

### Event and cluster labels

- `cluster_labels.csv`: 30 verb clusters. Columns: Cluster, Top verbs, Label.
- `event_labels.csv`: 30 event labels mapped to analytic categories. Columns: Top verbs, Label, Motta-Roth, Agency, Group.
- `label_to_nested_mapping_reference.csv`: Mapping of each label to its nested Motta-Roth and Agency categories.

### Reference ontologies

- `fashion_ontology.csv`: Fashion term ontology (term, category, subcategory, n_words; 1,255 terms).
- `fashionpedia_ontology.csv`: Fashionpedia terms (term, category; 302 terms).
- `instances_attributes_val2020.json`: Fashionpedia validation annotations (source for the ontology).

## `checkpoints/`

Serialized intermediate artifacts so pipeline stages can be resumed without re-running earlier steps.

- `rlda_init_vocab.pkl`: Initial candidate vocabulary before final selection.
- `chosen_vocab.pkl`: Final vocabulary used for RollingLDA.
- `df_with_noun_tokens.pkl`: Corpus DataFrame with extracted noun tokens per review.
- `df_with_term_stats.pkl`: Term-level frequency and statistics used in vocabulary selection.
- `event_sequences.jsonl`: Per-review ordered event sequences extracted for the event-chain analysis.

## Outputs

Generated tables, figures, and interactive plots, grouped by pipeline stage.

- `cleaning_outputs/`: Suspect-token lists flagged during corpus cleaning (`suspect_tokens.csv`, `last_remaining_suspect_tokens.csv`).
- `outputs_rlda_preprocessing/`: Vocabulary and term diagnostics, stopword record, K and init sweeps, and the preprocessing-stage pyLDAvis (`ldavis_init.html`).
- `outputs_rlda_fitting/`: The fitted RollingLDA model (`rollinglda_official_model.rds`), doc–topic and topic–word matrices, top-word tables, and a pyLDAvis HTML.
- `outputs_rlda_codebook/`: Per-topic top-word plots, representative documents, topic stability, and topic interpretations feeding the codebook.
- `outputs_rlda_inspection/`: Topic-word evolution (lift and relevance), chunk cosine similarity, entry/exit tables, prevalence-per-year, and a pyLDAvis HTML.
- `inputs_llm_annotation/batches/`: Per-batch `review_id,review` CSVs prepared for the full-corpus LLM annotation in 2.9.
- `outputs_event_chains/`: Event-chain extraction and analysis — raw triples (`triples_raw.jsonl`), cluster inspection, domain-verb diagnostics, and the event-type map. Subfolders:
  - `order/`: Event-order signal summary.
  - `composition/`: Event-composition signal summary.
  - `composition_maps/`: Composition and chain-length tables and figures across units (Cluster_30, MR_4, Agency_6) by year and era.
  - `representations/`: Chain representation audit and feature files.
  - `experiment/`: Composition-at-scale results.
