# LLM Prompt for Screening and Extracting Data from Research Articles

## Role and Objective

You are reviewing a research article about the relationship between **child temperament** and **language ability or language disorder**.

Complete the review in three stages:

1. Screen the article against the inclusion criteria.
2. Extract study characteristics, measures, descriptive statistics, and temperament-language associations.
3. Assess study quality using the NIH Quality Assessment Tool for Observational Cohort and Cross-Sectional Studies.

Use only information explicitly reported in the article, including its tables, figures, appendices, footnotes, and supplementary materials. Do not infer missing information from general knowledge.

## General Rules

- For screening questions, use only these values:
  - `1` = Yes
  - `0` = No
  - `?` = Uncertain
- Use `?` whenever you are less than 90% confident.
- For extraction fields:
  - Use `NR` when information is not reported.
  - Use `NA` when a field is not applicable.
  - Do not calculate missing values unless the article provides enough information and the calculation is straightforward. Clearly label any calculated value as `Calculated`.
- Preserve the terminology used by the authors.
- Include the page number, table number, figure number, or section for every important answer whenever possible.
- Quote only short phrases when needed to justify a classification.
- If the manuscript contains multiple studies, report the study number and focus on the study or studies that examine an association between temperament and language.

---

# Stage 1: Inclusion Screening

Evaluate each criterion independently. For each item, provide:

- `Decision`: `1`, `0`, or `?`
- `Evidence`: a concise explanation based on the article
- `Location`: page, table, figure, supplement, or section

## 1A. Eligible Child Age Range

**Question:** Does any relevant study sample include human children between **12 months and 7 years 11 months** of age?

### Decision rules

- `1` = At least part of the relevant sample is 12 months through 7 years 11 months old. This may include children in kindergarten, first grade, and sometimes second grade when their reported ages are below 8 years.
- `0` = Every participant is younger than 12 months, or every participant is 8 years or older. A sample consisting entirely of children in third grade or above should normally be coded `0`, unless reported ages show that eligible children are included.
- `?` = Age is missing, reported too vaguely, or cannot be determined with at least 90% confidence.

## 1B. Measure of Child Temperament

**Question:** Does the study measure a relatively stable child temperament, personality, self-regulation, or dispositional trait?

Temperament may include, but is not limited to:

- Surgency
- Effortful control
- Negative affect or negative affectivity
- Positive affect
- Behavioral inhibition
- Inhibitory control
- Shyness
- Attentional abilities
- Self-regulation
- Executive function, when treated as a broader dispositional trait

### Decision rules

- `1` = The study measures temperament, personality, or a specific trait-like facet. Parent, caregiver, or teacher questionnaires usually qualify. A laboratory task qualifies only when the authors explicitly use it to represent a broader, relatively stable trait.
- `0` = The study measures only an immediate state or task-specific response, such as reaction time or one-time performance, without treating it as a stable trait. Internalizing problems, externalizing problems, psychiatric symptoms, or behavior problems alone do not count as temperament.
- `?` = A child characteristic is measured, but it is unclear whether it represents temperament or a stable disposition.

## 1C. Measure of Language Ability or Language Disorder

**Question:** Does the study measure child language ability or identify a language-related disorder or delay?

Qualifying constructs include:

- Vocabulary
- Word learning
- Expressive language
- Receptive language
- General communication ability or impairment
- Mean length of utterance, or MLU
- Late talking
- Developmental Language Disorder, or DLD
- Specific Language Impairment, or SLI
- Language delay
- Verbal expression difficulties, including stuttering when treated as a language or communication outcome

### Decision rules

- `1` = The study includes at least one qualifying language measure, language diagnosis, or general communication measure.
- `0` = The study focuses only on speech production, articulation, grammar, pragmatics, literacy, reading, phonological processing, hearing loss, Deafness, or a speech-specific disorder, with no qualifying language measure.
- `?` = The construct is language-related, but the article does not provide enough detail to determine whether it qualifies.

## 1D. Typically Developing, Monolingual Population

**Question:** Does the study include monolingual children without major developmental or neurological disorders, apart from language delay or language disorder?

### Decision rules

- `1` = The article states that the children are typically developing or do not have major developmental or neurological disorders, and the sample is monolingual. The language spoken does not need to be English.
- `0` = The entire relevant sample consists of bilingual or multilingual children, or the entire sample has autism, Down syndrome, a major neurological condition, or another major developmental disorder.
- `?` = The article does not clearly report monolingual status, developmental status, or both.

If the article contains both eligible and ineligible subgroups, describe them separately rather than automatically assigning `0`.

## 1E. Empirical Study and English Availability

**Question:** Does the article report original empirical data, and is the article available in English?

### Decision rules

- `1` = The article reports original data from a correlational, experimental, longitudinal, observational, survey, or similar empirical study, and the article is available in English.
- `0` = The article is a literature review, theoretical paper, book chapter overview, systematic review, or meta-analysis; or the full article is not available in English.
- `?` = The article type or English availability cannot be determined confidently.

## 1F. Rothbart-Based Temperament Measure

**Question:** Did the study use a Rothbart-based temperament framework or instrument?

Qualifying instruments include:

- Infant Behavior Questionnaire, or IBQ
- Early Childhood Behavior Questionnaire, or ECBQ
- Children's Behavior Questionnaire, or CBQ
- Revised, short-form, teacher-report, translated, or culturally adapted versions of these measures

### Decision rules

- `1` = The article identifies an IBQ, ECBQ, CBQ, or a recognized version of one of these. It may also be coded `1` when the study reports only the three broad Rothbart dimensions—surgency, effortful control, and negative affect—and the framework is clearly Rothbart-based.
- `0` = No temperament measure is used; temperament is measured only through laboratory tasks; or the article uses a different personality framework such as extraversion or neuroticism without a Rothbart measure.
- `?` = Temperament is measured, but the instrument or framework is unclear.

## 1G. Reports a Core Rothbart Dimension

**Question:** Does the study report at least one of the following dimensions?

- Surgency
- Effortful control
- Negative affect or negative affectivity

### Decision rules

- `1` = At least one of these dimensions is reported.
- `0` = None of these dimensions is reported.
- `?` = The article uses related terminology, but equivalence cannot be determined confidently.

## 1H. Reports a Temperament-Language Association

**Question:** Does the study report a statistical association between at least one temperament variable and at least one qualifying language variable?

Qualifying evidence may include:

- Pearson or Spearman correlation
- Regression coefficient or beta
- Group comparison
- Odds ratio
- Structural equation model path
- Mediation or moderation result
- Another statistical test directly linking temperament and language

### Decision rules

- `1` = The article reports a direct statistical relationship between a temperament construct and a language construct. The result may appear in the main text, a table, a supplement, a footnote, or an exploratory analysis.
- `0` = Both temperament and language are measured, but no direct association between them is reported.
- `?` = The article appears to test the relationship, but the result is not clearly reported or cannot be located.

## Stage 1 Output Table

| Criterion | Decision | Evidence | Location |
|---|---:|---|---|
| 1A. Eligible age range |  |  |  |
| 1B. Child temperament measure |  |  |  |
| 1C. Language ability or disorder measure |  |  |  |
| 1D. Typically developing, monolingual population |  |  |  |
| 1E. Empirical study and English availability |  |  |  |
| 1F. Rothbart-based temperament measure |  |  |  |
| 1G. Core Rothbart dimension reported |  |  |  |
| 1H. Temperament-language association reported |  |  |  |

### Overall Screening Recommendation

Report one of the following:

- `Include`
- `Exclude`
- `Manual review required`

Explain the recommendation briefly. Do not exclude solely because one or more items are coded `?`; instead, recommend manual review.

---

# Stage 2: Study and Data Extraction

Complete this section for each relevant study within the manuscript. If the manuscript contains multiple studies, create a separate subsection for each study that reports a temperament-language association.

## 2A. Citation Verification

Extract and verify:

- Article title
- Authors
- Publication year
- Journal
- DOI, if reported

## 2B. Relevant Study Number

- Identify the study number, experiment number, cohort, wave, or analysis sample.
- Explain why this study is relevant to the temperament-language review.

## 2C. Study Design and Data Source

Report:

- Study design, such as cross-sectional, longitudinal, experimental, observational, or parent-report survey
- Number and timing of assessment waves
- Whether the data are part of a larger study, cohort, registry, intervention, or archived dataset
- Name and citation of the parent study or dataset, when reported
- Recruitment setting and location

## 2D. Sample Size

Report:

- Total enrolled sample
- Final analytic sample
- Sample size for each relevant analysis, when different
- Subgroup sizes, if the sample contains multiple groups
- Reasons for exclusions or missing data, when reported

## 2E. Demographic Characteristics

Extract the following, using the units and labels reported by the authors:

| Characteristic | Result | Location |
|---|---|---|
| Child age: mean |  |  |
| Child age: standard deviation |  |  |
| Child age: range |  |  |
| Child age: unit |  |  |
| Gender or sex distribution |  |  |
| Race |  |  |
| Ethnicity |  |  |
| Parent education |  |  |
| Household income |  |  |
| Other socioeconomic-status measure |  |  |
| Monolingual or multilingual status |  |  |
| Developmental or diagnostic status |  |  |

## 2F. Measures

### Temperament Measures

For every temperament variable, report:

- Construct or facet
- Instrument or task name
- Informant, such as parent, caregiver, teacher, child, or observer
- Number of items or subscale, if reported
- Response scale, if reported
- Reliability, such as Cronbach's alpha or omega
- Assessment time point
- Whether the measure is Rothbart-based

### Language Measures

For every language variable, report:

- Construct measured
- Instrument or task name
- Expressive, receptive, vocabulary, communication, word learning, diagnosis, or other category
- Raw, standardized, percentile, age-equivalent, or categorical score
- Reliability or validity information, if reported
- Assessment time point

### Comparison Type

State which type of comparison is used:

- Continuous language ability compared with continuous temperament scores
- Language-disorder group compared with a typically developing group on temperament
- Temperament used to predict later language
- Language used to predict later temperament
- Another design, described precisely

## 2G. Descriptive Statistics

Extract the mean, standard deviation, and range for every reported variable below. Also include the sample size used to calculate each statistic.

| Variable | N | Mean | SD | Minimum | Maximum | Score type or unit | Location |
|---|---:|---:|---:|---:|---:|---|---|
| Effortful control |  |  |  |  |  |  |  |
| Surgency |  |  |  |  |  |  |  |
| Negative affect |  |  |  |  |  |  |  |
| Language measure 1 |  |  |  |  |  |  |  |
| Language measure 2 |  |  |  |  |  |  |  |

Add rows for all additional language measures and relevant temperament variables.

## 2H. Temperament-Language Associations

Extract every reported association between each temperament facet and each qualifying language measure.

For each result, report:

- Study number or sample
- Temperament variable
- Language variable
- Analysis type
- Direction of association
- Effect estimate, such as `r`, `rho`, `b`, `beta`, odds ratio, mean difference, path coefficient, or test statistic
- Standard error, if reported
- p-value
- Confidence interval
- Whether the estimate is unadjusted or adjusted
- Covariates included in the adjusted model
- Sample size for the analysis
- Time points of predictor and outcome
- Whether the association is statistically significant according to the authors
- Page, table, figure, or supplement location

Use the following table:

| Study | Temperament variable | Language variable | Analysis | Estimate type | Estimate | SE | 95% CI | p-value | Adjusted? | Covariates | N | Direction | Significant? | Location |
|---|---|---|---|---|---:|---:|---|---:|---|---|---:|---|---|---|
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |

### Important extraction rules

- Extract nonsignificant as well as significant associations.
- Do not report a model coefficient as a simple correlation.
- Distinguish standardized from unstandardized regression coefficients.
- If a result is shown only in a figure, state that it was extracted from a figure and avoid estimating an exact value unless the value is labeled.
- If several models are reported, extract each relevant model or clearly identify the primary and fully adjusted models.
- If the same sample appears in multiple articles or studies, identify the shared cohort or dataset so duplicates can be reviewed.

---

# Stage 3: NIH Study Quality Assessment

Use the NIH Quality Assessment Tool for Observational Cohort and Cross-Sectional Studies:

<https://www.nhlbi.nih.gov/health-topics/study-quality-assessment-tools>

For each item, use only one of these ratings:

- `Yes`
- `No`
- `CD` = Cannot Determine
- `NR` = Not Reported
- `NA` = Not Applicable

For each rating, provide a concise justification and the article location.

## Quality Questions

1. Was the research question or objective clearly stated?
2. Was the study population clearly specified and defined?
3. Was the participation rate of eligible persons at least 50%?
4. Were participants selected or recruited from the same or similar populations, including the same time period? Were inclusion and exclusion criteria prespecified and applied uniformly?
5. Was a sample-size justification, power analysis, variance estimate, or effect-size estimate provided?
6. For the analyses in this paper, were the exposures of interest measured before the outcomes were measured?
7. Was the timeframe sufficient to reasonably expect an association between exposure and outcome, if one existed?
8. For exposures that can vary in amount or level, did the study examine different exposure levels in relation to the outcome, such as categories or a continuous measure?
9. Were exposure measures clearly defined, valid, reliable, and implemented consistently across participants?
10. Were exposures assessed more than once over time?
11. Were outcome measures clearly defined, valid, reliable, and implemented consistently across participants?
12. Were outcome assessors blinded to participants' exposure status?
13. Was loss to follow-up after baseline 20% or less?
14. Were key potential confounding variables measured and statistically adjusted for their impact on the exposure-outcome relationship?

## Stage 3 Output Table

| NIH Item | Rating | Justification | Location |
|---:|---|---|---|
| 1 |  |  |  |
| 2 |  |  |  |
| 3 |  |  |  |
| 4 |  |  |  |
| 5 |  |  |  |
| 6 |  |  |  |
| 7 |  |  |  |
| 8 |  |  |  |
| 9 |  |  |  |
| 10 |  |  |  |
| 11 |  |  |  |
| 12 |  |  |  |
| 13 |  |  |  |
| 14 |  |  |  |

## Overall Quality Rating

Assign one overall rating:

- `Good`
- `Fair`
- `Poor`

Provide a short justification based on the pattern of NIH item ratings. Do not calculate the rating from a simple numerical score unless a predefined scoring rule has been provided.

---

# Final Response Structure

Return the completed review in this order:

1. **Article citation**
2. **Stage 1: Inclusion screening table**
3. **Overall screening recommendation**
4. **Stage 2: Study and data extraction**
5. **Stage 2 association table**
6. **Stage 3: NIH quality assessment table**
7. **Overall quality rating**
8. **Missing or unclear information requiring manual review**

At the end, include a concise list of every field coded as `?`, `NR`, or `CD` so a human reviewer can verify those items.
