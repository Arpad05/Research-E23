# Simulation of Fake News Propagation Across Social Media Platforms

> **Independent research project completed during undergraduate studies at Université de Montréal**  
> *October 2023 | Computer Science & Operations Research Department*

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## 📋 Overview

This independent research project models the cross-platform propagation of misinformation on social media using epidemiological models and Graph Convolutional Networks (GCN). Unlike traditional single-platform studies, this work examines how fake news spreads **across multiple social media platforms** (Facebook, Twitter, Reddit) with different feed algorithms and user demographics.

### Key Innovation

The proposed **multi-platform propagation model** accounts for:
- Platform-specific feed algorithms (scoring, ranking, filtering)
- Cross-platform account linking and information flow
- User behavior modeling (trustworthiness, closeness, impulsivity)
- Content type effects on propagation speed

## 🎯 Research Objectives

1. **Model fake news spread** using epidemiological frameworks (Susceptible-Incubator-Spreader-Stifler)
2. **Simulate multi-platform propagation** considering algorithm differences
3. **Analyze cross-platform dynamics** and their impact on misinformation spread
4. **Support fake news detection** by understanding propagation patterns

## 🔬 Methodology

### Epidemiological Model

The project adapts traditional epidemic models to social media context with four agent states:

- **Susceptible**: Users not yet exposed to the information
- **Incubator**: Users who received information but haven't decided whether to believe/share
- **Spreader**: Active users propagating information (true or false)
- **Stifler**: Users who lost interest or chose not to spread

### Platform-Specific Modeling

#### Facebook
- Scoring algorithm based on user interests and social graph
- Interest calculation: `prob_interest = Σ(social_activity × topic_prob) / Σsocial_activity`
- Factors: closeness, time elapsed, feedback count

#### Twitter  
- Mixed feed: 50% In-Network + 50% Out-Network
- Real Graph for engagement prediction
- Ranking based on retweets, likes, replies

#### Reddit
- Four recommendation modes: Home, Popular, All, Latest
- Community (Subreddit) based filtering
- Upvote/downvote temporal analysis

### Graph Neural Networks (GCN)

- Multi-platform graph representation with cross-platform edges
- Node features: platform type, user demographics, engagement metrics
- Edge weights: trust, closeness, interaction frequency

## 📊 Key Components

### Agent Modeling
- **Demographic profiles** based on real platform statistics
- **Behavioral parameters**: impulsivity, topic preferences, trust levels
- **Multi-account support**: Same user across different platforms

### Content Classification
- **Twinword API** integration for text topic analysis
- Probabilistic topic scoring for targeted propagation
- URL and text content tagging

### Cross-Platform Propagation
- Account linkage between platforms (e.g., Twitter account linked to Facebook)
- Platform choice modeling for spreaders
- Message type effects (post, private message, group)

## 📈 Results & Insights

The model demonstrates:
- **Algorithm impact**: Different platforms show varying propagation speeds due to feed algorithms
- **Cross-platform amplification**: Linked accounts accelerate overall spread
- **Demographic targeting**: Content naturally reaches aligned user groups
- **Temporal dynamics**: Time lags between platforms affect total reach

## 🛠️ Technologies & Tools

- **Graph Neural Networks (GCN)** - Network relationship modeling
- **Twinword API** - Text classification and topic scoring
- **Python** - Primary implementation language
- **Statistical modeling** - Probabilistic user behavior
- **Multi-agent simulation** - Epidemiological framework

## 📚 Academic Context

This project was conducted as **independent research** at **Université de Montréal** during undergraduate studies. The research explores advanced topics in:
- Social network analysis
- Misinformation detection
- Computational epidemiology
- Machine learning on graphs

The work utilized a formal research template and methodology to develop a comprehensive theoretical framework for understanding multi-platform fake news propagation.

### Research Motivation

The COVID-19 pandemic saw a **20% increase** in social media usage (54→65 min/day in the US), making fake news propagation a critical area of study. This research contributes to:
- Understanding multi-platform dynamics
- Supporting detection algorithms
- Informing content moderation policies

## 📖 Full Paper

The complete research paper with literature review, methodology details, and mathematical formulations is available in [`Fake_News_Propagation.pdf`](./Fake_News_Propagation.pdf).

### Key Sections:
- **Chapter 1**: Literature Review on epidemic models and social media algorithms
- **Chapter 2**: Proposed multi-platform solution and agent modeling
- **Chapter 3**: Conclusions and future work
- **Appendix A**: Scoring system implementation details

## 📄 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

## 🔗 References

Selected key references:
- Raponi et al. (2022) - "Fake news propagation: A review of epidemic models"
- Meta (2023) - Facebook content distribution documentation
- Twitter (2023) - Recommendation algorithm open source release

Full bibliography available in the research paper.

## 👤 Author

**Arpad Botond Rigo**  
Département d'informatique et de recherche opérationnelle  
Université de Montréal

*This independent research was completed in October 2023 as part of undergraduate studies in Computer Science, exploring advanced topics in social network analysis and misinformation propagation.*

---

## 🚀 Future Work

Potential extensions and improvements:
- [ ] Implementation of complete simulation environment
- [ ] Real-world data collection and validation
- [ ] Integration with existing fake news detection systems
- [ ] Expansion to additional platforms (TikTok, Instagram)
- [ ] Temporal analysis of propagation patterns
- [ ] Bot detection and impact modeling

---

**Note**: This is a theoretical framework and research paper. Implementation code for the simulation environment is under development and will be added to this repository in future updates.
