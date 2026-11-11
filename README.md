<div align="center">

# Fake News Detection: Current Trends and Innovative Methodologies

**A review of manual, machine-learning, NLP and LLM-based fake news detection, and a proposed methodology for propaganda-aware detection**

![Field](https://img.shields.io/badge/field-NLP%20%7C%20Misinformation-2f6db5)
![Topics](https://img.shields.io/badge/topics-Transformers%20%7C%20LLM%20Agents%20%7C%20Fact--Checking-7b4fb5)
![Security](https://img.shields.io/badge/threats-Phishing%20%7C%20Botnets%20%7C%20Deepfakes-c0394f)
![Type](https://img.shields.io/badge/type-seminar%20paper-2e8b45)
![Year](https://img.shields.io/badge/year-2024-d9822b)

[Read the paper (PDF)](paper/Fake_News_Detection_Current_Trends_and_Innovative_Methodologies.pdf)

Farhan Ali Arshad
Advanced Topics in Computational Text and Media Science (NLP Seminar) · Universität Trier · Summer Semester 2024

</div>

---

## Overview

False information spreads faster than it can be checked, and it harms both social trust and cybersecurity. This
paper reviews how fake news detection has developed, from manual fact-checking to transformer models and
LLM agents that consult external knowledge. It also examines how cyber threats such as phishing, botnets and
deepfakes are used to spread misinformation.

Building on the review, the paper proposes a **propaganda-aware detection methodology**: a model trained on data
enriched with propaganda techniques, supported by dedicated sub-models for emotional language and logical
fallacies.

> **Main finding:** combining machine learning, NLP and network analysis is the most promising way to fight the
> spread of misinformation.

## What the paper covers

![Landscape](assets/landscape.png)

| Section | Content |
|---|---|
| **Literature review** | Transformer-based detection with content and social context, the FaKnow library, the Teller framework, an LLM agent for fake news detection, classical ML comparisons, dual-evidence graph models and sentiment-aware detection |
| **Detection approaches** | Manual fact-checking (expert websites, crowdsourcing) versus automatic content-based detection |
| **Security threats** | Phishing, social engineering, botnets, malware, DDoS attacks and deepfakes as channels for misinformation |
| **Current trends** | Machine learning classifiers, NLP methods (sentiment, topic modelling, BERT, GPT), network traffic analysis and automated fact-checking |
| **Proposed method** | An end-to-end, propaganda-aware pipeline from problem definition to model refinement |

## Related work at a glance

| Work | Approach | Key features | Data | Finding |
|---|---|---|---|---|
| Raza & Ding (2022) | Transformer-based detection | Content and social context analysis | Online news datasets | Automated methods scale where manual fact-checking cannot |
| **FaKnow** (Zhu et al., 2024) | Unified library | Many models and datasets on a PyTorch backend | Fake news benchmarks | Makes research faster and reproducible |
| **Teller** (Liu et al., 2024) | Explainable, generalisable detection | Logic templates combined with LLMs | News datasets | Transparent, interpretable verdicts |
| Prabha et al. (2024) | Classical ML comparison | Logistic Regression, Random Forest, Decision Tree | Benchmark datasets | Decision Tree most accurate; data quality is decisive |
| Dual evidence perception | Graph neural networks + semantics | Structural and semantic evidence | News and social media data | Fixes methods that ignore semantic content |
| Sentiment-based detection | Sentiment analysis | Emotional tone of content | ISOT, LIAR | Sentiment features raise accuracy |
| **LLM agent** (Li et al., 2024) | LLM agent | Expert workflow, domain knowledge, web search | Snopes, PolitiFact, GossipCop | External search improves detection |

## Proposed methodology

![Proposed methodology](assets/proposed_methodology.png)

| Stage | Details |
|---|---|
| **1. Problem definition** | Detect fake news with a model trained on a dataset enriched with propaganda |
| **2. Data collection** | Balanced verified real and confirmed fake news; propaganda-annotated or synthetic data that mimics real propaganda |
| **3. Preprocessing and features** | Noise removal, then four feature groups (below) |
| **4. Model selection** | Baselines (Logistic Regression, SVM, Decision Trees) and advanced models (LSTM, BERT, Transformers) fine-tuned on the propaganda-loaded data |
| **5. Propaganda sub-models** | Emotion detection for emotionally loaded words, fallacy recognition for typical logical fallacies, translation-bias identification |
| **6. Training and validation** | Supervised learning with propaganda labels as input features; paraphrasing and back-translation augmentation; k-fold cross-validation |
| **7. Testing** | Pilot testing and user feedback; accuracy, precision, recall, F1 and AUC-ROC, with emphasis on detecting propaganda |
| **8. Refinement** | Iterate on errors and feedback |

**Feature groups**

| Textual | Metadata | Social context | Graph-based |
|---|---|---|---|
| TF-IDF | Source reliability | User engagement metrics | Propagation graphs |
| N-grams | Publishing date and time | User profile information | Network structure |
| Sentiment | Author reputation | | Centrality measures |

<details>
<summary><b>Original methodology figure from the paper</b></summary>
<br>
<p align="center"><img src="assets/proposed_method_original.png" width="80%" alt="Original methodology figure"></p>
</details>

## Key takeaways

1. **Manual fact-checking does not scale.** It is accurate but slow, costly and open to bias; crowdsourcing adds
   inconsistency.
2. **Transformers and LLMs lead current research.** Models such as BERT and GPT capture subtle linguistic cues,
   and LLM agents improve accuracy by consulting external search engines.
3. **Explainability is becoming a requirement.** Frameworks like Teller show why a claim is judged false, which
   builds trust in automated systems.
4. **Misinformation is also a security problem.** Botnets, phishing, malware and deepfakes are delivery channels,
   so network and propagation analysis complements text analysis.
5. **Propaganda techniques are a missing signal.** Modelling emotional manipulation and logical fallacies
   explicitly is a promising direction for more robust detectors.

## Related project

The ideas in this paper were later put into practice in
[German Harmful Content Detection](https://github.com/farhanaliarshad1/german-harmful-content-detection), which
compares transformers, a multi-task model and LLM prompting for German fake news, hate speech and toxicity.

## Citation

```bibtex
@misc{arshad2024fakenews,
  title  = {Fake News Detection: Current Trends and Innovative Methodologies},
  author = {Arshad, Farhan Ali},
  year   = {2024},
  note   = {Seminar paper, Advanced Topics in Computational Text and Media Science, Universit{\"a}t Trier}
}
```

## License

The paper and figures are shared for portfolio and educational purposes. Please cite the paper if you use its
content.
