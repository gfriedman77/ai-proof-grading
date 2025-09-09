
# Data and analysis for the paper "Can AI Grade Mathematical Proofs?"

## Files

The data described in our paper appears in [data-table.csv](data-table.csv),
and its data dictionary is given below.

See [analysis.ipynb](analysis.ipynb) for the construction of tables, figures,
statistics, and tests used in the paper.

## Data dictionary

The data dictionary below is in abbreviated form, and is discussed in more
detail in the full paper, not included in this repository.

| Column name | Meaning |
|-|-|
| `ProofID` | a unique ID# assigned to each proof as it was collected |
| `InstitutionID` | a unique ID# assigned to donating institutions, to anonymize them |
| `InstitutionType` | a simplification of the Carnegie 2021 basic classification of the institution (one of five categorical values) |
| `Topic` | the mathematical topic into which the proof falls |
| `Bytes` | the length of the proof, in bytes, when in Markdown form |
| `HasHumanGrade` | boolean value indicating whether the proof was graded by a human (which not all were, due to constraints on volunteer time) |
| `M_H` | human grader's assessment of whether the proof contains at least one mistake (true = at least one mistake, false = no mistakes, empty = not graded by human) |
| `M_A` | embedded use case AI grader's assessment of whether the proof contains at least one mistake (true = at least one mistake, false = no mistakes) |
| `T_H` | human grader's assessment of which type of mistake the student's first mistake was (or "No mistake" if there was none, or empty if not graded by a human) |
| `T_A` | embedded use case AI grader's assessment of which type of mistake the student's first mistake was (or "No mistake" if there was none) |
| `S_H` | human grader's assessment of which sentence contained the student's first mistake (1 for first sentence, 2 for second, etc., -1 if no mistake, empty if not graded by a human) |
| `S_A` | embedded use case AI grader's assessment of which sentence contained the student's first mistake (1 for first sentence, 2 for second, etc., -1 if no mistake) |
| `A_H` | text containing human grader's advice to the student, if any |
| `A_A` | text containing embedded use case AI grader's advice to the student, if any |
| `A_2` | text containing student use case AI grader's assessment of the student's work, in full |
| `Con_1` | human assessment of whether the human grade is consistent with the embedded use case AI grade (yes or no, as one of two categorical values) |
| `Con_1_Comments` | text containing comments attached to the human assessment of `Con_1`, if any |
| `Con_2` | human assessment of whether the human grade is consistent with the student use case AI grade (yes or no, as one of two categorical values) |
| `Con_2_Comments` | text containing comments attached to the human assessment of `Con_2`, if any |
| `Cor` | human assessment of whether the student use case AI grade is correct (mostly correct, partly correct, or mostly incorrect, as one of three categorical values) |
| `Cor_Comments` | text containing comments attached to the human assessment of `Cor`, if any |
| `DWYD_1` | boolean value (0 or 1), whether the embedded use case AI response contained an instance of the ``do what you did'' phenomenon discussed in the paper |
| `DWYD_2` | boolean value (0 or 1), whether the student use case AI response contained an instance of the ``do what you did'' phenomenon discussed in the paper |
| `Right_1` | boolean value (0 or 1), whether the embedded use case AI response was right when the human grade was wrong |
| `Right_2` | boolean value (0 or 1), whether the student use case AI response was right when the human grade was wrong |


