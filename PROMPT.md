# Fruit Freshness Project — AI Prompt Document

> This document is a **prompt pack** for building a master-level computer vision coursework project on **nonlinear fruit freshness assessment using handcrafted visual features and lightweight models**.  
> It is designed to be **fed directly to AI tools** in stages.

---

## 1. Recommended Usage

Use this prompt document in the following order:

1. **Master Prompt** — use once to establish the whole project
2. **Stage Prompts** — use one by one for each phase
3. **Refinement Prompts** — use when you already have code/results and want iteration
4. **Output Constraints** — append to any prompt when needed

This project should **not** be framed as a pure end-to-end CNN classification task.  
The main line is:

- handcrafted feature extraction
- low-level image analysis
- nonlinear freshness representation
- lightweight but solid models
- interpretability and coursework-style analysis

---

## 2. Project Positioning Summary

### Project title
**Nonlinear Fruit Freshness Assessment Using Handcrafted Visual Features and Lightweight Models**

### Core idea
Instead of treating fruit quality as only a binary classification problem, this project explores whether handcrafted visual cues — especially **color, texture, and boundary-related features** — can be used not only for **fresh/rotten classification** but also for constructing an **exploratory nonlinear freshness score**.

### Dataset assumption
Use the **Fresh and Rotten Fruits Dataset for Machine-Based Evaluation of Fruit Quality** or another similar fresh/rotten fruit dataset.

### Technical preference
- Prefer **Pillow + NumPy** for low-level processing
- Use **scikit-learn** for traditional models
- Use **PyTorch only if needed** for a lightweight CNN baseline
- Avoid over-reliance on high-level black-box APIs
- Emphasize feature engineering, analysis, and interpretation

---

## 3. Master Prompt

Use this prompt first.

```text
I am building a master-level computer vision coursework project on fruit freshness assessment.

Project theme:
Nonlinear fruit freshness assessment using handcrafted visual features and lightweight models.

Core requirements:
1. Do NOT turn this into a pure end-to-end CNN project.
2. The main focus should be traditional image processing, handcrafted feature extraction, and interpretable analysis.
3. Use color, texture, and edge/boundary-related features as the main feature groups.
4. I want both:
   - a basic fresh vs rotten classifier
   - an exploratory nonlinear freshness score
5. The dataset only has binary labels, so do not pretend that I have true continuous freshness labels.
6. Use Python.
7. Prefer Pillow + NumPy for image processing and feature extraction.
8. Use scikit-learn for classical models.
9. PyTorch is allowed only for a lightweight comparison model such as MobileNetV3 or ResNet18.
10. The project should feel like a serious coursework project rather than an API demo.

Please help me design the whole project from a practical coursework perspective.

I want:
- a clear problem definition
- suitable research questions
- a complete pipeline
- feature design
- preprocessing strategy
- model selection
- nonlinear freshness score strategy
- experiment design
- evaluation metrics
- result visualization ideas
- report structure
- likely limitations
- a realistic implementation sequence

Output requirements:
- Be concrete and actionable
- Avoid empty generalities
- Organize the answer in sections
- Prioritize feasibility, interpretability, and coursework quality
```

---

## 4. Stage Prompt A — Refine the Research Framing

Use this when you want the AI to help you shape the project concept and research questions.

```text
Help me refine the research framing for my computer vision coursework project.

Project topic:
Nonlinear fruit freshness assessment using handcrafted visual features and lightweight models.

Please do the following:
1. Propose 3 to 5 coursework-appropriate project titles.
2. Write a concise project objective.
3. Generate 4 to 6 research questions.
4. Make sure the framing reflects:
   - handcrafted visual features
   - color, texture, and boundary analysis
   - exploratory nonlinear freshness estimation
   - comparison with at most one lightweight deep learning baseline
5. Keep the framing academically credible:
   - do not claim true physical freshness measurement
   - treat the continuous freshness score as exploratory or derived
6. Give me a final recommended version suitable for a master-level report and presentation.

Output format:
- Title options
- Objective
- Research questions
- Final recommended framing
```

---

## 5. Stage Prompt B — Design the Whole Pipeline

```text
Please design a full end-to-end pipeline for my fruit freshness coursework project.

Project constraints:
- The dataset has fresh / rotten labels only
- The project should focus on handcrafted visual features
- Use Pillow + NumPy as much as possible
- Use scikit-learn for the main models
- Add at most one lightweight CNN baseline
- Emphasize interpretability and analysis

Please design the pipeline from:
1. data loading
2. preprocessing
3. feature extraction
4. feature standardization
5. classification modeling
6. nonlinear freshness score construction
7. evaluation
8. visualization
9. reporting

For each step, explain:
- what to do
- why it matters
- what output it should produce

Also give me a recommended implementation order that minimizes risk and helps me progress steadily.
```

---

## 6. Stage Prompt C — Feature Engineering Design

```text
I want to build this project mainly around handcrafted visual features.

Please help me design a feature engineering plan organized into these three major groups:
1. color features
2. texture features
3. edge / boundary / shape features

Requirements:
- Use mainly Pillow + NumPy
- Add minimal necessary support from scikit-image or OpenCV only if justified
- For each feature group, give specific computable features rather than abstract concepts
- Explain why each feature may relate to fruit freshness
- Distinguish which features are better for:
  - classification
  - exploratory freshness score construction
- Recommend a compact but strong final feature set suitable for a coursework project

Please present the answer as:
- feature group
- specific features
- intuition
- implementation notes
- risks / limitations
- final recommendation
```

---

## 7. Stage Prompt D — Implement Low-Level Feature Extraction

```text
Help me implement a handcrafted image feature extraction pipeline in Python for fruit freshness assessment.

Important constraints:
- Prefer Pillow + NumPy
- Avoid jumping directly to large black-box code
- Build the solution step by step
- Keep the code clean and coursework-friendly
- Do not over-engineer the project

My feature goals:
1. basic color statistics
2. HSV-based features
3. grayscale texture statistics
4. edge strength and edge density
5. boundary / contour-related descriptors if possible
6. output a fixed-length feature vector for each image

Please do this in order:
1. propose module structure
2. define functions and their inputs/outputs
3. write the code gradually
4. explain each part briefly
5. ensure the result is suitable for batch dataset processing

Do not dump everything at once. First give the module design.
```

---

## 8. Stage Prompt E — Nonlinear Freshness Score Design

```text
My dataset only provides binary labels: fresh and rotten.
However, I want to extend the project into exploratory nonlinear freshness estimation.

Please design several valid ways to construct a derived freshness score without falsely claiming that I have true continuous labels.

I want methods from at least these categories:
1. model-probability-based score
2. feature-space-distance-based score
3. cluster-based or ranking-based score

For each method, explain:
- core idea
- implementation steps
- strengths
- weaknesses
- how to describe it honestly in a coursework report
- how to visualize the results

At the end, recommend:
- one main freshness score method
- one backup method

The answer should prioritize feasibility and academic defensibility.
```

---

## 9. Stage Prompt F — Model Selection

```text
I already have handcrafted feature vectors extracted from fruit images.
Please help me choose models for this project.

Candidate models:
- Logistic Regression
- SVM with RBF kernel
- Random Forest
- XGBoost or LightGBM
- small MLP
- one lightweight CNN baseline such as MobileNetV3 or ResNet18

Please compare them specifically for:
- small to medium-sized handcrafted feature data
- nonlinear decision boundaries
- training cost
- interpretability
- coursework presentation value
- overfitting risk
- practicality

Then recommend:
1. one main model
2. one backup model
3. one comparison model

Also propose a sensible experiment order so I can start simple and progressively improve.
```

---

## 10. Stage Prompt G — Experiment Design

```text
Help me design the experiments for my fruit freshness coursework project.

Project direction:
- handcrafted visual features
- fresh/rotten classification
- exploratory nonlinear freshness score
- lightweight CNN comparison baseline

I want the experiment section to be analytical rather than just reporting final accuracy.

Please design:
1. baseline classification experiments
2. feature-group ablation experiments
3. nonlinear freshness score experiments
4. comparison with one lightweight CNN baseline
5. failure case analysis
6. robustness analysis if feasible

For each experiment, include:
- purpose
- input
- method
- evaluation metrics
- expected observations
- suitable visualization format

Make the design suitable for a master-level coursework report.
```

---

## 11. Stage Prompt H — Report Outline

```text
Please help me write a report structure for my master-level computer vision coursework project.

Project topic:
Nonlinear fruit freshness assessment using handcrafted visual features and lightweight models.

Requirements:
1. The report should look like strong coursework, not a conference paper.
2. It must include:
   - introduction
   - related rationale or background
   - method
   - experiments
   - discussion
   - limitations
   - future work
3. It should clearly emphasize:
   - handcrafted visual features
   - interpretability
   - nonlinear freshness score as an exploratory construct
   - comparison with a lightweight learning model
4. For each section, explain what content should be written.
5. Give me some useful academic-style sentence templates for:
   - introduction
   - method
   - discussion
   - limitations
```

---

## 12. Stage Prompt I — Codebase Structure

```text
I want to organize my coursework code into a clean, medium-sized Python project.

The project includes:
- data loading
- preprocessing
- handcrafted feature extraction
- classical ML models
- exploratory freshness score construction
- evaluation
- visualization
- optional lightweight CNN comparison

Please design:
1. a recommended folder structure
2. the responsibilities of each module
3. how to separate notebooks from reusable code
4. how to keep the project extensible without over-engineering it
5. how to organize outputs such as plots, metrics, saved models, and tables

Make the structure suitable for a coursework submission.
```

---

## 13. Stage Prompt J — Result Interpretation

Use this after you already have results.

```text
I will provide you with my experiment results for a fruit freshness coursework project.

The project includes:
- handcrafted color, texture, and boundary-related features
- fresh/rotten classification
- exploratory nonlinear freshness score
- comparison with one lightweight CNN baseline

Please help me analyze the results from a coursework perspective.

I want you to:
1. interpret the numbers instead of only restating them
2. compare the contribution of color, texture, and boundary features
3. explain why some fruit categories may be easier or harder
4. discuss differences between handcrafted-feature models and the CNN baseline
5. evaluate whether the nonlinear freshness score is actually meaningful
6. identify limitations shown by the results
7. write discussion-style paragraphs that I can adapt into my report

I will provide:
- metrics tables
- confusion matrices
- selected plots
- some example images if needed
```

---

## 14. Stage Prompt K — Viva / Presentation Preparation

```text
I need to prepare for a coursework presentation or viva about my fruit freshness project.

Project topic:
Nonlinear fruit freshness assessment using handcrafted visual features and lightweight models.

Please help me prepare concise but strong answers for likely questions such as:
1. Why did you choose handcrafted features instead of relying only on CNNs?
2. Why do you argue that freshness should be treated as nonlinear?
3. If the dataset only has binary labels, how can you justify a continuous freshness score?
4. What is the value of your approach compared with direct image classification?
5. What are the main limitations of the project?
6. How would you improve it in future work?

Requirements:
- answers should sound like a student in a master-level presentation
- concise but intelligent
- not overly theoretical
- each answer should be roughly around one minute when spoken
```

---

## 15. Refinement Prompts

These are for later-stage iteration.

### 15.1 Improve code quality
```text
I will give you a Python module from my coursework project.
Please help me improve it for readability, modularity, and correctness without over-engineering it.

Constraints:
- keep it suitable for a student coursework project
- preserve the current logic unless there is a real issue
- explain any structural changes
- prefer simple, maintainable code
```

### 15.2 Improve visualizations
```text
I have generated some plots for my fruit freshness project.
Please suggest how to improve them so they communicate results more clearly in a coursework report or presentation.

Focus on:
- readability
- comparison clarity
- consistency
- whether each plot actually supports a claim
```

### 15.3 Strengthen discussion
```text
I will give you the current draft of my discussion section.
Please rewrite it to make it more analytical, more connected to the experiments, and more academically appropriate for a master-level coursework report.

Do not exaggerate claims.
Do not pretend the freshness score is a true physical measurement.
```

---

## 16. Output Constraints Block

Append this block to any prompt when you want tighter AI behavior.

```text
Output constraints:
- Be concrete and implementation-oriented
- Avoid generic advice
- Do not inflate claims
- Do not pretend I have ground-truth continuous freshness labels
- Prioritize handcrafted feature analysis over black-box end-to-end solutions
- Keep the solution suitable for a master coursework project
- Prefer clear structure with headings and bullet points
- If giving code, keep it clean and directly runnable
- If giving methodology, explain both rationale and feasibility
```

---

## 17. Recommended Final Project Configuration

If the goal is **good quality + manageable workload + strong coursework value**, use this configuration:

### Main line
- handcrafted color features
- handcrafted texture features
- handcrafted edge / boundary features
- SVM or Random Forest as the main classifier
- derived nonlinear freshness score using either:
  - model probability, or
  - feature-space distance

### Comparison line
- one lightweight CNN baseline
- recommended: **ResNet18** or **MobileNetV3**

### Key experiments
- fresh/rotten classification
- feature-group ablation
- model comparison
- freshness score visualization
- failure case analysis

### Key claims to keep
- The project studies whether handcrafted visual cues are useful for fruit freshness assessment.
- The continuous freshness score is exploratory and derived, not a ground-truth physical measurement.
- The project values interpretability, feasibility, and coursework-level rigor.

---

## 18. One-Sentence Project Description

Use this sentence in prompts, reports, or slides:

> This project explores whether handcrafted visual features — especially color, texture, and boundary-related cues — can support not only fresh/rotten classification but also the construction of an exploratory nonlinear fruit freshness score.

---

## 19. Common Pitfalls to Avoid

1. **Overclaiming the freshness score**  
   Do not describe it as real physical freshness ground truth.

2. **Turning the project into a pure CNN benchmark**  
   The main value is feature analysis and interpretability.

3. **Using too many disconnected features**  
   Keep the project organized around three main groups:
   - color
   - texture
   - boundary / edge

4. **Reporting only final accuracy**  
   The coursework value comes from:
   - feature contribution analysis
   - ablations
   - comparisons
   - discussion of limitations

---

## 20. Best Execution Order

1. finalize title and research questions  
2. build dataset loading and preprocessing  
3. implement color features  
4. implement texture features  
5. implement edge / boundary features  
6. train a simple baseline model  
7. improve with a stronger classical model  
8. construct the exploratory freshness score  
9. add one lightweight CNN baseline  
10. run ablations and write analysis

---
