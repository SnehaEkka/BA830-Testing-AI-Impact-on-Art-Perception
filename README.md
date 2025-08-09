# Artificial Impressions: A/B Testing Disclosure Impact on AI Art Perception  
#### "How does knowing 'it's AI' change how we appreciate images?"

## About  
This project investigates, using a randomized A/B testing (RCT) design, whether telling viewers that an image is AI-generated influences their appreciation of artwork. By collecting and analyzing experimental survey data, we quantify perceptual biases and provide actionable insights for the growing field of AI-generated art.

## Data Source

- **Survey Dataset:** Ratings and demographic data from 144 participants, collected via a Qualtrics survey at Boston University and online.
- **Images:** 22 diverse AI-generated artworks (landscape, modern art, realism, etc.).
- **A/B Test Design:** Participants were split into treatment (informed of AI origin) and control (no disclosure) groups via random assignment.

## Survey & Data Collection

Below is the poster and QR code used in our outreach campaign. It was displayed around campus and shared online to recruit a diverse, randomized sample for our A/B testing experiment.

<img src="Causal%20Inference%20Project%20Poster.png" alt="Survey Poster" width="400"/>

*Poster used to recruit survey participants and explain study goals. Scanning the QR code led participants directly to our A/B testing survey on image appreciation.*

## Purpose & Business Context

As AI-generated artwork becomes mainstream, organizations, artists, and platforms need to understand if—and how—disclosure of AI origins changes people's reactions. This project captures experimentally how transparency influences art appreciation, offering evidence for how to present AI art to various audiences.

## Experimental Solution Overview

- **A/B (RCT) Design:** Random assignment to "treatment" (AI origin disclosed) or "control" (no mention of origin) ensured valid identification of the disclosure effect.
- **Survey Implementation:** Each participant rated 10 of 22 images (randomly drawn), with demographic controls and stratified sampling.
- **Analysis Pipeline:** Data cleaning, validation of randomization, exploratory data analysis, power checks, and advanced regression (including image-level fixed effects and conditional average treatment effect estimation).

## Tech Stack & Tools

| Tool/Library         | Purpose                        | Why Chosen                      |
|----------------------|--------------------------------|---------------------------------|
| Python               | Data cleaning, regression      | Flexibility, statistics modules |
| Pandas, NumPy        | Data wrangling                | Tabular EDA & aggregation       |
| Statsmodels, Pyfixest| Regression & fixed effects    | Causal inference, ATE           |
| Matplotlib, Seaborn  | Visualization                 | Plotting group differences      |
| Qualtrics            | Survey tool                   | Reliable randomization, scaling |
| Jupyter Notebook     | Workflow, analysis reporting   | Transparency, reproducibility   |

## Data Pipeline & Workflow

- Collected randomized survey responses (treatment/control) with Qualtrics.
- Cleaned and balanced data; validated group assignment and demographics (proportions_ztest, balance regression).
- Performed regression and fixed effects modeling to quantify treatment effects.
- Explored conditional effects (by gender, BU attendance).
- Conducted power analysis, EDA, and visualization for robust reporting.

## Business Impact & Key Results

- **A/B Testing Methodology:**  
  Randomized Controlled Trial (RCT) design allowed us to isolate the effect of disclosure precisely (AI vs. no disclosure) on art appreciation.

- **Measurable Outcomes:**  
  - **Statistically significant negative effect:** Disclosing AI origin led to a *drop in average appreciation (mean score) of 12–15%* compared to undisclosed images, controlling for demographics and individual image effects.
  - **Subgroup Insights:** BU-affiliated respondents were *even more sensitive*—showing an *up to 18% reduction* in their ratings after disclosure.
  - **No significant skew in randomization:** Extensive balance checks confirmed assignment was random and groups were comparable.
  - **Power analysis limitation:** Achieved 144 valid responses vs. 973 needed for optimal power, so effect detection is robust at medium size, but future work should expand the sample for subtle patterns.

- **Practical Implications:**  
  - Platforms and artists should expect tangible perceptual penalties for full disclosure of AI authorship—a consideration for curation, display, and marketing strategies.
  - The A/B testing approach provides a framework that’s scalable to other domains where transparency/trust is at issue.

## Code & How to Reproduce

- **Highlights:**  
  - Pipelineized data wrangling for messy survey formats.
  - Advanced regression analysis with controls and fixed effects (image, demographic).
  - Modular and annotated Jupyter Notebook for clarity and reusability.

- **To Run:**  
  1. Clone the repository.  
  2. `pip install -r requirements.txt` (pandas, seaborn, matplotlib, statsmodels, pyfixest, jupyter, etc.)
  3. Open and run `BA830-T20-Effect-of-AI-on-Art-Perception.ipynb`.
  4. Follow cell instructions; customize analysis as needed.

## Future Improvements
- Increase respondent pool to fully achieve high statistical power and explore even subtler demographic effects.
- Broaden outreach for greater demographic representativeness (beyond BU).
- Incorporate open-ended feedback to complement the quantitative survey.
- Extend to multi-arm A/B/n tests (e.g., human vs. AI, co-creation disclosures).

## Alignment to Career Vision

This project exemplifies my commitment to analytics engineering, where I design robust experiments, clean and analyze complex data, and generate clear, actionable insights that bridge business, technology, and user perception. It demonstrates mastery of experimental (A/B) design, statistical rigor, and real-world application.

## Coursework & Contributors
- **Coursework:** Built for **BA830 - Causal Inference & Business Experimentation** (Boston University MSBA), with a focus on causal inference, A/B testing, and business-centric research design.
- **Teammates:** Ananya Anand, Jenn Hong, Leonardo Trucios, Lyushen Song, Mauro Wang, Sneha Ekka

## Additional Resources
- **Presentation Deck:** [AI Art Perception](https://www.canva.com/design/DAF-3PBzPO0/CIkWo6oeiDAN9z4DdQj0qQ/view?utm_content=DAF-3PBzPO0&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h87cc299af8)
- **Full Project Report:** `BA830-T20-Project-Report.pdf`
