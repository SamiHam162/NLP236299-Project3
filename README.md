# CS236299 Project 3: Parsing - The CKY Algorithm

This repository contains the implementation of Project Segment 3 for the CS236299 course. The goal of this project is to develop a system for constituency parsing using the CKY algorithm. The project involves implementing both a non-probabilistic and a probabilistic version of the CKY algorithm and applying them to the ATIS dataset.

## Table of Contents

- [Project Overview](#project-overview)
- [Goals](#goals)
- [Implementation Details](#implementation-details)
- [Setup](#setup)
- [Usage](#usage)
- [Evaluation](#evaluation)
- [Discussion](#discussion)
- [License](#license)

## Project Overview

The primary objective of this project is to implement the CKY algorithm for parsing sentences relative to context-free grammars (CFGs). The project is divided into five parts:

1. Completing a CFG for the ATIS dataset.
2. Implementing the CKY algorithm for recognizing grammatical sentences.
3. Extending the CKY algorithm to construct parse trees.
4. Constructing a probabilistic context-free grammar (PCFG).
5. Extending the CKY algorithm to handle PCFGs for probabilistic parsing.

## Goals

1. Finish the CFG for the ATIS dataset.
2. Implement a CKY recognizer to determine if a sentence is grammatical.
3. Extend the CKY recognizer to build parse trees for grammatical sentences.
4. Construct a PCFG based on the ATIS dataset and evaluate its effectiveness.
5. Extend the CKY algorithm to return the most probable parse tree using a PCFG.

## Implementation Details

### Part 1: Finish the CFG for the ATIS Dataset

- **Grammar Expansion**: The project begins by expanding a hand-crafted grammar for the ATIS dataset to cover more sentences. This involves adding rules to handle specific phrases related to places, airlines, and more.

### Part 2: Implement a CKY Recognizer

- **CKY Recognizer**: A CKY algorithm-based recognizer is implemented to determine if a given sentence can be parsed by the grammar.

### Part 3: Implement a CKY Parser

- **CKY Parser**: The CKY algorithm is extended to build parse trees for sentences that can be parsed by the grammar. This involves maintaining back-pointers to reconstruct the parse tree from the CKY table.

### Part 4: PCFG Construction

- **PCFG Creation**: A probabilistic context-free grammar (PCFG) is constructed from a set of annotated training trees. The grammar is transformed into Chomsky Normal Form (CNF) and then used for probabilistic parsing.

### Part 5: Probabilistic CKY Parsing

- **Probabilistic CKY**: The CKY algorithm is further extended to handle PCFGs, allowing it to return the most probable parse tree for a given sentence. This is achieved by working in log space to avoid underflows during probability calculations.

## Setup

To set up the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/SamiHam162/NLP236299-Project3.git
   cd NLP236299-Project3# NLP236299-Project3
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
3. Download the necessary datasets and scripts as outlined in the `project3_tree-Submission.ipynb` file.

## Usage

1. **Grammar Expansion**:
   - Modify the grammar file in `data/grammar` to expand coverage for ATIS queries.
2. **CKY Recognizer**:
   - Implement and test the CKY recognizer on various sentences to ensure it correctly identifies grammatical sentences.
3. **CKY Parser**:
   - Extend the CKY recognizer to build parse trees and test it on sample sentences.
4. **PCFG Construction**:
   - Construct a PCFG from the training trees in `data/train.trees` and convert it to CNF.
5. **Probabilistic CKY Parsing**:
   - Implement the probabilistic CKY parser and evaluate its performance on the ATIS test set.

## Evaluation
The evaluation of the grammar and parsing algorithms is done using precision, recall, and F1-score metrics computed by the `evalb` tool. The project also includes systematic evaluation scripts to test the coverage and accuracy of both the non-probabilistic and probabilistic CKY algorithms.

## Discussion
The final section of the project involves a discussion on the strengths and limitations of the implemented parsing algorithms, as well as any challenges encountered during the implementation.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
