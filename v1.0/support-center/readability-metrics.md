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

### **1. Flesch-Kincaid Reading Ease**

- Scale: 0–100 (higher = easier to read).
- Focus: Sentence length and syllables per word.

### **2. Flesch-Kincaid Grade Level**

- Scale: U.S. school grade levels (e.g., 6 = 6th grade).
- Focus: Similar to Reading Ease but mapped to grades.

### **3. Gunning Fog Index**

- Scale: Years of education required.
- Focus: Sentence complexity and polysyllabic words.

### **4. SMOG Index**

- Scale: Years of education required.
- Focus: Counts polysyllabic words, ideal for health and legal texts.

### **5. Coleman-Liau Index**

- Scale: U.S. grade levels.
- Focus: Average sentence length and letters per word.

### **6. Automated Readability Index (ARI)**

- Scale: U.S. grade levels.
- Focus: Character count and word count.

## **Grade Levels and Age Groups**

The table below maps the grade levels and their associated age groups for each readability metric:

{% table %}
| **Metric** | **Grade Level** | **Age Group (Years)** | **Meaning** | 
| ---- | ---- | ---- | ---- | 
| **Flesch-Kincaid Reading Ease** | 90–100 (4th grade) | 9–10 | Very easy to read (e.g., children's books). | 
|  | 60–70 (8th–9th grade) | 13–15 | Standard readability (e.g., newspapers). | 
|  | 0–30 (College) | 18+ | Very difficult, complex texts. | 
| **Flesch-Kincaid Grade Level** | 4 (4th grade) | 9–10 | Simple texts for young readers. | 
|  | 8–12 (High school) | 14–18 | Suitable for high school students. | 
|  | &gt;12 (College) | 18+ | Advanced, academic-level texts. | 
| **Gunning Fog Index** | 7–8 | 12–14 | Ideal for general audiences. | 
|  | 10–12 (High school) | 14–18 | Requires more effort to read. | 
|  | &gt;12 (College) | 18+ | Difficult, technical writing. | 
| **SMOG Index** | 4–6 | 9–11 | Easy-to-read, suitable for children. | 
|  | 8–12 (High school) | 14–18 | Moderate difficulty. | 
|  | &gt;12 (College) | 18+ | Complex, technical texts. | 
| **Coleman-Liau Index** | 4 (4th grade) | 9–10 | Simple and accessible. | 
|  | 8–12 (High school) | 14–18 | Challenging for younger audiences. | 
|  | &gt;12 (College) | 18+ | Requires higher education. | 
| **Automated Readability Index (ARI)** | 3–6 | 8–11 | Basic readability, suitable for kids. | 
|  | 8–12 (High school) | 14–18 | Standard for educated adults. | 
|  | &gt;12 (College) | 18+ | Technical or professional texts. | 
{% /table %}

## Interpreting Results

The six metrics provide a comprehensive view of text complexity. Their combined analysis ensures that:

- Content is suitable for the intended audience.
- Texts with higher education requirements can be identified and simplified if necessary.

## Viewing Readability Metrics

Readability metrics are available from the right sidebar.

{% image url="https://uploads.developerhub.io/prod/02/tqc3a9e8w57kic79eviqtq9xv2hbnsgq7h7eqi01n3v37rm1lpokwmc6wp5p14sd.png" mode="responsive" height="303" width="487" %}
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

For technical documentation, the target audience—such as developers and product managers—often has a higher-than-average familiarity with specialised terminology and complex concepts. Therefore, an “advanced” readability score does not necessarily mean the content is inappropriate. Instead, it reflects the advanced nature of the subject matter, which is expected for technical audiences.

Writers should prioritise clarity, precision, and audience needs over trying to simplify content excessively. Technical accuracy often takes precedence, even if it results in a higher complexity score.

### Limitations

- Readability metrics is only available on documentation sections that are set to an English locale.