# Child-Centric Risk Taxonomy

27 risk categories across 7 domains, each instantiated separately for two developmental stages: **ages 6–12** (concrete-operational) and **ages 13–17** (adolescent). Machine-readable form: [`taxonomy.json`](taxonomy.json).

The taxonomy is not only a labelling scheme but the backbone of data generation: each category is recursively decomposed top-down into 40–50 narrow sub-scenarios, and every sub-scenario seeds a fixed generation budget of single messages and multi-turn conversations, split evenly across the two age bands. Because a minor's threat model differs from an adult's, a topic that is merely sensitive for an adult is treated as harmful for a child, and the task is strictly binary (harmful vs. safe).

## Overview

| Domain | Categories |
|---|---|
| [Behavioral and Social Developmental Risks](#behavioral-and-social-developmental-risks) | 3 |
| [Mental Wellbeing and Safety](#mental-wellbeing-and-safety) | 5 |
| [Toxicity, Cyberbullying and Inappropriate Content](#toxicity-cyberbullying-and-inappropriate-content) | 7 |
| [Privacy, Identity and Data Exploitation](#privacy-identity-and-data-exploitation) | 2 |
| [Bias, Stereotyping and Discrimination](#bias-stereotyping-and-discrimination) | 2 |
| [Cognitive and Educational Impact](#cognitive-and-educational-impact) | 3 |
| [Misuse and Exploitation Risk](#misuse-and-exploitation-risk) | 5 |
| **Total** | **27** |

## Behavioral and Social Developmental Risks

| ID | Category |
|---|---|
| `CAT_BEH_01` | Emotional Manipulation & Social Isolation |
| `CAT_BEH_02` | Anthropomorphism & False Trust |
| `CAT_BEH_03` | Promotion of Risky Behaviors |

## Mental Wellbeing and Safety

| ID | Category |
|---|---|
| `CAT_MEN_01` | Self-Harm and Psychological Distortion |
| `CAT_MEN_02` | Grooming & Predatory Behaviour |
| `CAT_MEN_03` | Inadequate Crisis Detection and Response |
| `CAT_MEN_04` | Unhealthy Emotional Attachment and Addiction |
| `CAT_MEN_05` | AI as Unregulated "Free Therapy" and Support Overreliance |

## Toxicity, Cyberbullying and Inappropriate Content

| ID | Category |
|---|---|
| `CAT_TOX_01` | Exposure to Age-Inappropriate and General Harmful Content |
| `CAT_TOX_02` | Cyberbullying and Harassment |
| `CAT_TOX_03` | Toxic, Abusive and Offensive Language |
| `CAT_TOX_04` | Illegal Acts and Drugs |
| `CAT_TOX_05` | Violence, Gore and Weapons |
| `CAT_TOX_06` | Sexual Content and Boundary Violations |
| `CAT_TOX_07` | Hate Speech and Dehumanization |

> The grooming and sexual-boundary categories are represented solely through predatory manipulation dynamics and boundary-testing language — the behavioural patterns a safeguard must recognise. No sexually explicit content depicting minors was generated, stored, or released.

## Privacy, Identity and Data Exploitation

| ID | Category |
|---|---|
| `CAT_PRV_01` | Privacy Violations & Sensitive Data Sharing |
| `CAT_PRV_02` | Identity Abuse & Impersonation |

## Bias, Stereotyping and Discrimination

| ID | Category |
|---|---|
| `CAT_BIA_01` | Bias Reinforcement |
| `CAT_BIA_02` | Stereotyping and Discrimination |

## Cognitive and Educational Impact

| ID | Category |
|---|---|
| `CAT_COG_01` | Cognitive Overload |
| `CAT_COG_02` | Over-reliance & Cognitive Atrophy |
| `CAT_COG_03` | Misinformation & Hallucinations |

## Misuse and Exploitation Risk

| ID | Category |
|---|---|
| `CAT_MIS_01` | Academic Dishonesty and Automated Plagiarism |
| `CAT_MIS_02` | Social Engineering and Manipulation |
| `CAT_MIS_03` | Circumvention of Safeguards (Jailbreaking) |
| `CAT_MIS_04` | Content Generation for Harassment |
| `CAT_MIS_05` | Financial Exploitation |

## Safe baseline and hard negatives

The safe class combines everyday benign interactions (education, hobbies, curiosity, age-appropriate entertainment), generated top-down over 25–30 autonomously-derived topic categories, with 2,940 hard negatives: benign conversations that deliberately contain sensitive trigger words (e.g. discussing "shooting" in basketball, or "something sharp" in a kitchen context). Hard negatives force classifiers to rely on intent and context rather than surface keywords.

## Licence and citation

Taxonomy released under CC BY 4.0. If you use it, please cite:

```bibtex
WILL BE UPDATED AFTER RELEASE
```
