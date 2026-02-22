---
title: "Phase 1: Data Collection"
date created: Sunday, February 15th 2026, 12:38:00 pm
date modified: Sunday, February 22nd 2026, 9:43:34 am
---

# Phase 1: Data Collection

**Version**: 1.0  
**Date Created**: January 24, 2026  
**Context**: This procedure was developed following initial benchmark testing of Claude and Qwen 2.5 models [[2026-01-24_Ojibwe_AI_Benchmark_PRT]]. It provides a standardized methodology for collecting AI model outputs for later analysis.

---

# Overview

## Purpose

To systematically collect outputs from different AI language models when translating English phrases into Anishinaabemowin (Ojibwe language). This raw data will then be analyzed by using Qualcoder qualitative analysis software.

## Method

You will:

1. Test multiple AI models using standardized prompts
2. Record all model outputs exactly as they appear
3. Organize the data in a format suitable for Qualcoder import (suggest .txt or .md filetype)
4. Document metadata about each test (model, timestamp, etc.)

You will NOT:

- Evaluate the accuracy of translations (requires Ojibwe language knowledge)
- Make judgments about quality or correctness
- Consult dictionaries or verify translations

**Note**: Language analysis will be conducted after data collection. using Qualcoder.

## Testing Platform

**GROQ.com** - The platform provides access to multiple open-source language models through a single interface, making it efficient for quick comparative testing. You need to click on `Start Building` button top right and sign in using google account.  Use your institutional account as the work is tied to your RA position and keeps your personal Google account separate from this work for your own protection of data.

## Background Context

Previous testing (January 24, 2026) revealed that both paid cloud-based models (Claude) and locally-run models (Qwen 2.5) have limitations with Ojibwe translation. This round of testing aims to collect comparable data from open source models accessible via groq.com for systematic qualitative analysis.

---

# Materials Needed

## Required Resources

1. **Computer with internet access**
2. **Groq.com account** (create free account at https://groq.com using institutional account)
3. **Text editor or word processor** for recording outputs (Microsoft Word, Google Docs, or plain text editor)
4. **Spreadsheet software** (Excel, Google Sheets, or similar) for organizing metadata
5. **This procedure document**
6. **Reliable note-taking method** (digital preferred for easy copying/pasting)

## Optional But Helpful

- Screen capture tool to save screenshots of outputs
- Timer to track session duration
- Second monitor for easier copying between windows

---

# Pre-Testing Setup

## Step 1: Access Groq Platform

1. Go to https://groq.com
2. Log in or create account
3. Navigate to the chat/model interface
4. Familiarize yourself with available models

## Step 2: Identify Models to Test

Make a list of available models on groq.com. As of this procedure's creation, groq typically hosts models such as:

- Llama variants (Meta)
- Mixtral variants (Mistral AI)
- Gemma variants (Google)
- Others as available

**Action**: Document which models are available for testing. Plan to test at least 3-5 different models if available.

## Step 3: Set Up Data Collection Files

Create two files for organizing your data collection:

**File 1: YYYY-MM-DD_Model_XX_Outputs.txt** (or .docx)

- This will contain the raw text outputs from each model
- Use clear formatting to separate different models and test phrases
- This file will be imported into QualCoder for analysis

**File 2: Testing_Metadata.xlsx** (or Google Sheets)

- This will track metadata about each test
- Set up columns: Model Name, Model Version, Test Number, Test Phrase, Timestamp, Session Notes
- This helps organize and track the data collection process

See "Data Collection Format" section below for detailed structure.

Store all documents in MS TEAMS folder [GROQ_Testing_Ojibwe_Translation](https://yuoffice.sharepoint.com/:f:/r/sites/YORK-UserExperienceUXResearchDesign/Shared%20Documents/General/21.16%20Language%20Bot/GROQ_Testing_Ojibwe_Translation?csf=1&web=1&e=w9zMQ4)

---

# Data Collection Protocol

## Standard Test Phrases

Use these three phrases in order for each model:

**Test 1**: "I am listening carefully to you"

**Test 2**: "I am tired, I am going to sleep"

**Test 3**: "We are ending the meeting"

**Important**: Test each model with ALL THREE phrases before moving to the next model.

## Testing Each Model

For EACH model available on groq.com, follow this procedure:

### Step 1: Start Fresh Conversation

- Begin a new chat session with the model
- Note the model name and any version information displayed
- Record the current date and time

### Step 2: Use Standard Prompt

Copy and paste this EXACT prompt (replace [INSERT TEST PHRASE HERE] with the actual test phrase):

```
Please translate the following English phrase into Anishinaabemowin (Ojibwe language): 

[INSERT TEST PHRASE HERE]

Please provide the Ojibwe translation and explain the grammatical structure if possible.
```

### Step 3: Record the Complete Output

Copy the ENTIRE response from the model and paste it into your Model_Outputs.txt file.

**Use this format:**

```
===========================================
MODEL: [Model Name]
VERSION: [Version if shown]
TEST: Test 1
PHRASE: "I am listening carefully to you"
TIMESTAMP: [Date and Time]
===========================================

[PASTE COMPLETE MODEL OUTPUT HERE - include everything the model says]

===========================================
END OF OUTPUT
===========================================


```

### Step 4: Record Metadata

In your Testing_Metadata.xlsx spreadsheet, add a row with:

- Model Name
- Model Version (if available)
- Test Number (1, 2, or 3)
- Test Phrase (the English phrase)
- Timestamp
- Any technical issues or notes (e.g., "model took 30 seconds to respond", "received error message first", etc.)

### Step 5: Repeat for All Three Test Phrases for Model

- Continue with Test 2, using the same format
- Then Test 3
- Keep all three tests with one model together in your output file

### Step 6: Move to Next Model

- Start a completely new session/conversation
- Repeat Steps 1-5 with the next available model

**Important**: Do NOT skip around between models. Complete all three tests with one model before starting the next model.

---

# Data Collection Format for QualCoder

## File Structure

Your Model_Outputs.txt file should follow this consistent structure for every test:

```
===========================================
MODEL: Llama-3-70B
VERSION: v1.2
TEST: Test 1
PHRASE: "I am listening carefully to you"
TIMESTAMP: 2026-01-27 10:15 AM
===========================================

[Complete model output goes here, exactly as it appeared]

===========================================
END OF OUTPUT
===========================================


===========================================
MODEL: Llama-3-70B
VERSION: v1.2
TEST: Test 2
PHRASE: "I am tired, I am going to sleep"
TIMESTAMP: 2026-01-27 10:18 AM
===========================================

[Complete model output goes here, exactly as it appeared]

===========================================
END OF OUTPUT
===========================================
```

## This Structured Format Allows the Coder To:

- Import the file into QualCoder easily
- Code each model output as a separate segment
- Track which model and test phrase each output corresponds to
- Maintain consistent metadata across all data points

## Metadata Spreadsheet

Your Testing_Metadata.xlsx should something look like this:

| Model Name   | Model Version | Test Number | Test Phrase                     | Timestamp           | Notes                    |
| ------------ | ------------- | ----------- | ------------------------------- | ------------------- | ------------------------ |
| Llama-3-70B  | v1.2          | 1           | I am listening carefully to you | 2026-01-27 10:15 AM | No issues                |
| Llama-3-70B  | v1.2          | 2           | I am tired, I am going to sleep | 2026-01-27 10:18 AM | Response took 25 seconds |
| Llama-3-70B  | v1.2          | 3           | We are ending the meeting       | 2026-01-27 10:20 AM | No issues                |
| Mixtral-8x7B | v0.1          | 1           | I am listening carefully to you | 2026-01-27 10:25 AM | No issues                |

## What to Include in Notes Column

Record any technical observations:

- Response time if unusually long or short
- Error messages before successful response
- If model declined to translate
- If connection issues occurred
- Any other technical anomalies

**No need to include:**

- Your opinions about the translation quality
	- Whether it "looks correct" or not
- Comparisons to other models

---

# Completing Data Collection

## Step 1: Review Your Files

Before submitting, check that you have:

**Model_Outputs.txt file with:**

- Separator lines (`=========) between each output
- MODEL, VERSION, TEST, PHRASE, and TIMESTAMP clearly marked for each entry
- Complete model outputs copied exactly as they appeared
- Clear END OF OUTPUT markers

**Testing_Metadata.xlsx file with:**

- One row for each test conducted
- All columns filled in (Model Name, Version, Test Number, Phrase, Timestamp, Notes)
- Consistent model names across all rows
- Any technical issues noted

## Step 2: Create Session Summary

At the END of your Model_Outputs.txt file, add a brief session summary:

```
===========================================
SESSION SUMMARY
===========================================
Date of Testing: [Date]
Total Models Tested: [Number]
Total Tests Conducted: [Number = Models × 3]
Testing Duration: [Start time] to [End time]
Platform Used: Groq.com
Technical Issues: [List any if they occurred, or write "None"]
===========================================
```

## Step 3: File Naming

Save your files with these names:

- **YYYY-MM-DD_[Groq_Model]_Outputs.txt** (e.g., 2026-01-27_Llama-3-70B_Outputs.txt) this file holds only test data for one LM at a time
- **YYYY-MM-DD_Groq_Testing_Metadata.xlsx** (e.g., 20260127_Groq_Testing_Metadata.xlsx) this spread sheet holds information on all tests

## Step 4: Submit Files

Upload all files to the shared folder. These files will be:

1. Imported into QualCoder for qualitative analysis
2. Coded and analyzed for patterns
3. Used in research documentation

---
[[Anishinaabemowin AI Benchmark Testing Procedure-Analysis]]
# Checklist

## Before You Begin:

- [ ] Groq.com account created and accessible
- [ ] Model_Outputs.txt file created with proper formatting template
- [ ] Testing_Metadata.xlsx spreadsheet set up with column headers
- [ ] This procedure document reviewed and understood
- [ ] Time blocked for testing session (1.5-2 hours recommended)
- [ ] Quiet workspace with stable internet connection
- [ ] Text readily available to copy/paste test phrases and prompts

## During Testing (For Each Model):

- [ ] Started fresh conversation/session
- [ ] Recorded model name and version (if shown)
- [ ] Used exact prompt wording for each test
- [ ] Copied complete output (not just the Ojibwe translation)
- [ ] Used proper formatting in output file
- [ ] Filled in metadata spreadsheet row
- [ ] Noted any technical issues in Notes column

## After Testing All Models:

- [ ] Session summary added to end of Model_Outputs.txt
- [ ] All metadata rows complete in spreadsheet
- [ ] Files saved with proper naming convention (YYYYMMDD_Groq_…)
- [ ] Files reviewed for completeness
- [ ] Both files submitted to lead researcher

# Troubleshooting

## If groq.com is Unavailable:

- Document the downtime in your session notes
- Try again later
- If it remains down, contact lead researcher before trying alternative platforms

## If a Model Refuses to Translate:

- Copy the refusal message exactly into your output file
- Mark it clearly: "MODEL REFUSED TO TRANSLATE"
- Continue with the next test phrase or next model
- Note the refusal in your metadata spreadsheet

## If You Receive an Error Message:

- Copy the exact error message
- Try the same prompt one more time
- If it fails again, note "REPEATED ERROR" and move on
- Include error details in metadata Notes column

## If You're Unsure about Technical Details:

- Record what you CAN see (model name as displayed, timestamp)
- If version number isn't shown, write "Version not displayed"
- When in doubt, copy MORE rather than less (you can always use more context)

## If groq.com Interface Changes:

- Take a screenshot of the new interface
- Document what changed in your session summary
- Follow the same basic process: prompt model, record output
- Contact lead researcher if you're unsure how to proceed

---

# Research Context (For Reference)

This data collection is part of research on **community technological empowerment** and **Indigenous educational sovereignty**. The goal is to document limitations of current AI systems for Indigenous languages and build evidence for community-controlled language technology development.

Your careful, systematic data collection directly supports this research by providing comparable, unbiased outputs from multiple AI models that can then be analyzed for patterns and limitations.

---

# Questions or Issues?

If you encounter problems:

1. **Document everything** - Exact error messages, timestamps, what you tried
2. **Continue if possible** - Move to next model/test if one fails
3. **Don't interpret** - Just record what happened, not what you think it means
4. **Contact lead researcher** - Send questions along with your collected data

---

# Timeline Expectation

**Estimated time per model**: 15-20 minutes

- New session setup: 2 minutes
- Testing 3 phrases: 10-12 minutes (3-4 minutes per phrase including prompt and response time)
- Recording outputs and metadata: 3-5 minutes

**Total estimated time for 5 models**: 75-100 minutes (1.5-2 hours)

**Recommended approach**:

- Test all available models in one sitting if possible (maintains consistency)
- If you need to break, complete all 3 tests with one model before stopping
- Don't split a single model's tests across multiple sessions

Plan for breaks as needed. Accuracy in copying outputs is more important than speed.

---
