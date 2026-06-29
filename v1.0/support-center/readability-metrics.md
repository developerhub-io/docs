---
type: page
title: Readability Metrics
listed: true
slug: readability-metrics
description: 
index_title: Readability Metrics
hidden: 
keywords: 
tags: 
---

## What Are Readability Metrics?

Readability metrics are algorithms designed to evaluate the complexity of written text. These metrics assess factors such as sentence length, word difficulty, and syllable count to determine how easily a piece of text can be read and understood.

### Why Are They Important?

- **Accessibility**: Ensuring your content is understandable by the target audience.
- **User Engagement**: Simplifying text improves readability, which keeps readers engaged.
- **SEO Benefits**: Readable content ranks better in search engines.
- **Education**: Helps educators match texts to student reading levels.

## Readability Metrics Used

We use six commonly recognised readability metrics to assess text complexity. Each method evaluates different aspects of text readability:

### 1. Flesch-Kincaid Reading Ease

- Scale: 0–100 (higher = easier to read).
- Focus: Sentence length and syllables per word.

### 2. Flesch-Kincaid Grade Level

- Scale: U.S. school grade levels (e.g., 6 = 6th grade).
- Focus: Similar to Reading Ease but mapped to grades.

### 3. Gunning Fog Index

- Scale: Years of education required.
- Focus: Sentence complexity and polysyllabic words.

### 4. SMOG Index

- Scale: Years of education required.
- Focus: Counts polysyllabic words, ideal for health and legal texts.

### 5. Coleman-Liau Index

- Scale: U.S. grade levels.
- Focus: Average sentence length and letters per word.

### 6. Automated Readability Index (ARI)

- Scale: U.S. grade levels.
- Focus: Character count and word count.

## Grade Levels and Age Groups

The table below maps the grade levels and their associated age groups for each readability metric:

{% table layout="auto" %}
{% row %}
{% cell header=true %}
**Metric**
{% /cell %}
{% cell header=true %}
**Grade Level**
{% /cell %}
{% cell header=true %}
**Age Group (Years)**
{% /cell %}
{% cell header=true %}
**Meaning**
{% /cell %}
{% /row %}
{% row %}
{% cell %}
**Flesch-Kincaid Reading Ease**
{% /cell %}
{% cell %}
90–100 (4th grade)
{% /cell %}
{% cell %}
9–10
{% /cell %}
{% cell %}
Very easy to read (e.g., children's books).
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
60–70 (8th–9th grade)
{% /cell %}
{% cell %}
13–15
{% /cell %}
{% cell %}
Standard readability (e.g., newspapers).
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
0–30 (College)
{% /cell %}
{% cell %}
18+
{% /cell %}
{% cell %}
Very difficult, complex texts.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
**Flesch-Kincaid Grade Level**
{% /cell %}
{% cell %}
4 (4th grade)
{% /cell %}
{% cell %}
9–10
{% /cell %}
{% cell %}
Simple texts for young readers.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
8–12 (High school)
{% /cell %}
{% cell %}
14–18
{% /cell %}
{% cell %}
Suitable for high school students.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
\>12 (College)
{% /cell %}
{% cell %}
18+
{% /cell %}
{% cell %}
Advanced, academic-level texts.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
**Gunning Fog Index**
{% /cell %}
{% cell %}
7–8
{% /cell %}
{% cell %}
12–14
{% /cell %}
{% cell %}
Ideal for general audiences.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
10–12 (High school)
{% /cell %}
{% cell %}
14–18
{% /cell %}
{% cell %}
Requires more effort to read.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
\>12 (College)
{% /cell %}
{% cell %}
18+
{% /cell %}
{% cell %}
Difficult, technical writing.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
**SMOG Index**
{% /cell %}
{% cell %}
4–6
{% /cell %}
{% cell %}
9–11
{% /cell %}
{% cell %}
Easy-to-read, suitable for children.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
8–12 (High school)
{% /cell %}
{% cell %}
14–18
{% /cell %}
{% cell %}
Moderate difficulty.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
\>12 (College)
{% /cell %}
{% cell %}
18+
{% /cell %}
{% cell %}
Complex, technical texts.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
**Coleman-Liau Index**
{% /cell %}
{% cell %}
4 (4th grade)
{% /cell %}
{% cell %}
9–10
{% /cell %}
{% cell %}
Simple and accessible.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
8–12 (High school)
{% /cell %}
{% cell %}
14–18
{% /cell %}
{% cell %}
Challenging for younger audiences.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
\>12 (College)
{% /cell %}
{% cell %}
18+
{% /cell %}
{% cell %}
Requires higher education.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
**Automated Readability Index (ARI)**
{% /cell %}
{% cell %}
3–6
{% /cell %}
{% cell %}
8–11
{% /cell %}
{% cell %}
Basic readability, suitable for kids.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
8–12 (High school)
{% /cell %}
{% cell %}
14–18
{% /cell %}
{% cell %}
Standard for educated adults.
{% /cell %}
{% /row %}
{% row %}
{% cell %}
{% p /%}
{% /cell %}
{% cell %}
\>12 (College)
{% /cell %}
{% cell %}
18+
{% /cell %}
{% cell %}
Technical or professional texts.
{% /cell %}
{% /row %}
{% /table %}

## Interpreting Results

The six metrics provide a comprehensive view of text complexity. Their combined analysis ensures that:

- Content is suitable for the intended audience.
- Texts with higher education requirements can be identified and simplified if necessary.

## Viewing Readability Metrics

Readability metrics are available from the right sidebar.

{% image url="asset:f9lu4pqa4u0w" %}
The Readability panel
{% /image %}

The average reading level is calculated by averaging all the metrics and its score determines the colour of the readability metrics icon.

Three colours are used to identify the difficulty of reading the page:

- Green: Easy.
- Orange: Moderate.
- Red: Advanced.

## Bias in Readability Metrics

Most readability metrics were developed based on the **U.S. education system**, making their grade levels and age group mappings culturally specific. While these tools are helpful globally, their interpretations may not perfectly align with educational systems outside the U.S. Additionally:

- Non-English texts may not be accurately assessed without localisation.
- Complex sentence structures common in non-Western languages can skew results.

Readability scores are based on algorithms that assess the complexity of text using factors like sentence structure and word choice. These metrics are calibrated against the average literacy levels of the general population in the U.S. education system.

For technical documentation, the target audience (such as developers and product managers) often has a higher-than-average familiarity with specialised terminology and complex concepts. Therefore, an “advanced” readability score does not necessarily mean the content is inappropriate. Instead, it reflects the advanced nature of the subject matter, which is expected for technical audiences.

Writers should prioritise clarity, precision, and audience needs over trying to simplify content excessively. Technical accuracy often takes precedence, even if it results in a higher complexity score.

### Limitations

- Readability metrics is only available on documentation sections that are set to an English locale.
