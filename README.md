# Anishinaabemowin (Ojibwe) AI Translation Benchmark Dataset

This repository contains data and documentation from a benchmark study evaluating the capacity of large language models (LLMs) to translate English phrases into Anishinaabemowin (Ojibwe language). The work is submitted for anonymous peer review and supports a methodology paper focused on identifying open-source LLMs suitable for fine-tuning in support of Indigenous language revitalization.

---

## Project Overview

This study evaluates nine AI language models across two rounds of systematic testing using standardized English-to-Anishinaabemowin translation prompts. The goal is not to identify a production-ready translation system, but to establish a baseline benchmark and develop a replicable methodology for assessing LLM suitability for fine-tuning in low-resource, endangered language contexts.

The evaluation framework is adapted from the **Multidimensional Quality Metrics (MQM)** framework, modified to prioritize cultural preservation and linguistic fidelity over commercial translation standards.  Analysis is conducted using **Qualcoder** qualitative analysis software.

### Three Standardized Test Phrases

All models were tested with the same three prompts, selected to probe distinct morphological features of Anishinaabemowin:

|Test|English Phrase|Grammatical Focus|
|---|---|---|
|1|"I am listening carefully to you"|VTA conjugation, 1→2 person marking, adverbial modification|
|2|"I am tired, I am going to sleep"|Stative predicates, intentional aspect, phonological contraction|
|3|"We are ending the meeting"|Inclusive plural, VTI conjugation, derived nouns|

**Known reference translations (for verification):**

- Test 1: _Gibizindawmin wewena_
- Test 2: _Ndayekoz, nwiinbaa_
- Test 3: _Gigiizhitoonmin maawinji'idiwin_

---

## Repository Structure

### Procedure and Methodology

| File                                                                 | Description                                                                                                                                                                     |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Anishinaabemowin_AI_Benchmark_Testing_Procedure-data_collection.md` | Standardized data collection protocol used across both testing rounds. Includes prompt template, file naming conventions, metadata requirements, and quality control checklist. |

### Round 1 — Open-Source Models via Groq.com (January 29, 2026)

Five open-source models were tested through the Groq.com platform. Each model received the same three prompts in fresh, independent sessions.

|File|Model|Version|
|---|---|---|
|`2026-01-29_GPT-OSS-120B_Outputs.txt`|GPT OSS|120B|
|`2026-01-29_Groq-Compound_Outputs.txt`|Groq Compound|N/A|
|`2026-01-29_Kimi-K2_Outputs.txt`|Kimi K2|0905|
|`2026-01-29_Llama-4-Scout_Outputs.txt`|Llama 4 Scout|17B|
|`2026-01-29_Qwen-3-32B_Outputs.txt`|Qwen 3|32B|

### Round 2 — Commercial/Proprietary Models (February 12, 2026)

Four commercial platforms were tested using the same standardized prompt and recording format as Round 1, enabling direct cross-round comparison.

|File|Model|Version|Platform|
|---|---|---|---|
|`2026-02-12_Claude_Sonnet_4_5_Outputs.txt`|Claude Sonnet|4.5|claude.ai|
|`2026-02-12_ChatGPT_GPT_5_2_Outputs.txt`|ChatGPT|5.2|chatgpt.com|
|`2026-02-12_OpenAI_OjibweChat_GPT_4_Outputs.txt`|OjibweChat|GPT-4|ojibwechat.com|
|`2026-02-12_Perplexity_GPT_5_1_Outputs.txt`|Perplexity|5.1|perplexity.ai|

### Metadata

|File|Description|
|---|---|
|`Testing_Metadata.csv`|Row-level metadata for all Round 1 tests (model name, version, test number, phrase, timestamp, technical notes).|
|`Testing_Metadata_Round_2.csv`|Row-level metadata for all Round 2 tests. Includes an additional **compilation time** column not present in Round 1.|

---

## Data Format

All model output files follow a consistent structure designed for direct import into QualCoder:

```
===========================================
MODEL: [Model Name]
VERSION: [Version]
TEST: Test [1/2/3]
PHRASE: "[English test phrase]"
TIMESTAMP: [Date and Time]
===========================================

[Complete model output, exactly as generated]

===========================================
SESSION SUMMARY
===========================================
...
===========================================
```

---

## Evaluation Framework

Translation outputs are analyzed using an adapted MQM coding scheme implemented in QualCoder, focused on three categories most relevant for everyday language use and fine-tuning potential:

- **Accuracy** — mistranslation, omissions, additions
- **Terminology** — consistency and correctness of linguistic forms
- **Linguistic Conventions** — register appropriateness and cohesion

Additional holistic assessment dimensions include overall proximity to the reference translation and grammatical explanation quality are also assessed

---

## Language Resources

The following publicly available dictionaries were used for reference verification during analysis:

- Nishnaabemwin Dictionary: https://dictionary.nishnaabemwin.atlas-ling.ca/
- Ojibwe People's Dictionary: https://ojibwe.lib.umn.edu/

---

## Notes for Reviewers

- All author-identifying information has been removed from this repository for anonymous review.
- The dataset spans 9 models and 27 test instances across two rounds of testing (January–February 2026).
- The methodology is designed to be generalizable to other low-resource or endangered language contexts, not specific to Anishinaabemowin alone.
- Qualcoder analysis files are not included in this repository
