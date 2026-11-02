# Awesome-Differential-Privacy-Data-Anonymization

# Awesome-Differential-Privacy-Data-Anonymization

**Top Differential Privacy Data Anonymization (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Synthetic Data Generation, Differential Privacy Guarantees, PII Redaction & Self-Hosted Anonymization Libraries*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Differential Privacy & Data Anonymization**. These tools enable organizations to share, test, and analyze data without exposing individuals—using synthetic data generation, noise injection, and privacy-preserving transformations—from fully managed enterprise platforms to open-source libraries that give teams control over their anonymization pipeline.



**Examples** include Gretel.ai, Mostly AI, Tonic.ai, Hazy, Statice, Synthesized, Snowflake Differential Privacy, Privitar, K2View, and LeapYear (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted anonymization, differential privacy libraries, and open synthetic data generation. **Critical note**: The open-source landscape is rich in libraries—**IBM Diffprivlib** and **OpenDP Tumult Analytics** provide production-grade differential privacy primitives, **Opacus** enables DP training in PyTorch, and **SecretFlow** offers a unified privacy-preserving framework. No open-source project matches Gretel's managed synthetic data workflows, but for teams building custom privacy pipelines, the foundational libraries are mature.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global data anonymization, privacy-enhancing technologies (PETs), and synthetic data market is estimated between **$1.3B to $5.5B** in 2025–2026, expanding at an aggressive CAGR of 30%+ driven by generative AI training and tightening privacy mandates (GDPR, EU AI Act). The sector is **moderately to highly fragmented** rather than winner-take-all, characterized by niche specialists across data modalities (tabular, unstructured text, healthcare/relational data) and deployment boundaries (cloud SaaS vs. on-premises sovereign enclaves), alongside strategic acquisitions by cloud data warehouses and governance giants (e.g., Snowflake, Informatica, Nvidia).

## SaaS/Hosted Platforms

| Platform | Company Scale / Valuation / Revenue | Starting Pricing Tier | Free Tier Limits / Trial Limits | Description & Best For |
| :--- | :--- | :--- | :--- | :--- |
| **Snowflake Differential Privacy** | **$55B–$65B+ Market Cap** (~$3.6B ARR) | **$2.00–$3.00/credit** (Standard/Enterprise compute tiers, consumption-based) | **30-day free trial** with **$400 in free usage credits** (whichever expires first) | Native DP within Snowflake Data Clean Rooms. Best for Snowflake customers requiring entity-level differential privacy in multi-party clean room analytics. |
| **Privitar** *(Informatica)* | **Acquired by Informatica** (~$8B Salesforce deal; $1.6B+ ARR; Privitar was valued at ~$250M–$400M) | Enterprise contract via sales (historically custom scoping; typically starting at tens of thousands annually) | **Demo on request** (no self-serve free tier or public trial period; 14-to-30 day scoped enterprise pilot upon request) | Sensitive data provisioning, de-identification, and privacy governance. Best for large enterprises requiring policy-driven compliance and data masking. |
| **Gretel.ai** *(Nvidia)* | **Acquired by Nvidia** for **>$320M+ Valuation** (~$14.6M ARR; $67M+ VC raised) | **Team tier at $295/month** (pooled credits, 10 concurrent jobs); **$2.00/credit** pay-as-you-go | **Free forever plan**: **15 credits/month** (refreshed monthly, max 2 concurrent workers; ~100K synthetic records or ~2M PII detection records) | Managed synthetic data generation with DP and PII redaction for tabular, text, and time-series data. Best for teams wanting full-lifecycle synthetic data APIs. |
| **Tonic.ai** | **$100M–$250M Valuation** (~$16M–$18M ARR; $45M raised) | **Starter tier from $29/month** (includes $25 usage credits); pay-as-you-go metering for additional compute | **Free forever plan**: **$5 in monthly usage credits** (~9 complex synthesis sessions; no credit card required) | Realistic test data generation, relational synthesis, and differential privacy de-identification for developer databases. Best for test data management. |
| **K2View** | **$100M–$250M Valuation** (~$20M–$36M ARR; $43M+ growth capital raised) | **From £1,000/year (~$1,300/yr)** starting tier per catalog listing; enterprise custom tiers | **30-day free trial** (for cloud iPaaS / data integration platform evaluation) | Operational data product platform featuring micro-databases and built-in anonymization/tokenization. Best for real-time customer data synthesis. |
| **Mostly AI** | **~$50M–$100M Est. Valuation** (~$15M–$17M ARR; $25M+ raised) | Enterprise plans require sales quote; credit packs starting from pay-as-you-go tiers | **Free forever plan**: **2 credits refreshed daily** (auto top-up every 24h, designed for persistent developer experimentation) | High-fidelity tabular synthetic data generation with differential privacy guarantees. Best for BFSI and healthcare tabular dataset generation. |
| **Hazy** | **~$50M–$100M Est. Valuation** (~$3M ARR; $11.3M raised) | **Developer tier from $100/month**; enterprise licensing for on-prem/private cloud | **Free forever tier**: up to **100,000 rows/day** for developer experimentation | Synthetic data replicas built for regulated banking, telecom, and insurance institutions. Best for teams with predictable, mid-scale daily generation. |
| **Synthesized** | **~$30M–$60M Est. Valuation** (~$3M–$5M ARR; $30M+ raised including 2025 Series A) | **Free SDK / Solo Edition** ($0); Enterprise platform custom licensing | **Free forever SDK & Solo Edition**: unlimited generative models, datasets, and built-in DP guarantees for solo/dev workloads | Synthetic data SDK and agentic test infrastructure with mathematical differential privacy guarantees. Best for developers wanting self-hosted DP generation. |
| **Statice** *(PwC Germany)* | **Strategic acquisition by PwC Germany** (~$1M ARR; $6M+ early funding) | Custom enterprise licensing / pilot scoping | **Trial upon request**: Scoped POC pilot (typically 14 to 30 days guided evaluation, no self-serve free tier) | Irreversible synthetic data generation and data anonymization adhering to European GDPR standards. Best for enterprise compliance workflows. |
| **LeapYear** *(Acquired by Snowflake)* | **Acquired by Snowflake** (prior $35M+ funding; technology integrated into Snowflake DP) | Integrated into Snowflake platform consumption pricing | **Integrated into Snowflake**: 30-day trial with $400 credits via Snowflake | Pioneer in differential privacy algorithms; standalone platform sunsetted post-acquisition and embedded directly into Snowflake Data Clean Rooms. |

## Open-Source GitHub Projects



- **IBM Diffprivlib**

  **IBM Differential Privacy Library** (MIT, ~500+ stars) — **the most mature open-source differential privacy library**, built on top of Google's differential-privacy library . **Features**: **DP mechanisms** (Laplace, Gaussian, exponential); **DP machine learning** (logistic regression, naive Bayes, clustering); **DP statistics** (mean, median, histogram); **budget tracking** for privacy accounting; scikit-learn compatible APIs . **Tech stack**: Python. **Deploy**: `pip install diffprivlib`. **Trade-off**: **Library, not a platform**—no synthetic data generation; you implement the pipeline. **Best for**: developers wanting production-grade DP primitives for statistical queries and ML training.



- **OpenDP Tumult Analytics**

  **Python library for privately computing aggregate queries** (Apache 2.0) — **the most practical open-source DP tool for data analysts**, built atop Tumult Core . **Features**: **DP aggregate queries** on tabular data; **privacy budget accounting**; **Spark integration** for large datasets; **sensible defaults** for noise calibration; designed for analysts without DP expertise . **Tech stack**: Python. **Deploy**: `pip install tumult-analytics`. **Trade-off**: **Aggregate queries only**—not for synthetic data or row-level anonymization. **Best for**: data teams wanting to publish DP aggregate statistics without deep DP expertise.



- **Opacus**

  **PyTorch library for training with differential privacy** (Apache 2.0) — **the standard for DP machine learning**, maintained by Meta . **Features**: **DP-SGD** implementation; **privacy accounting** (RDP, Gaussian); **gradient clipping and noise injection**; **compatible with standard PyTorch training loops**; **memory-efficient** for large models . **Tech stack**: Python, PyTorch. **Deploy**: `pip install opacus`. **Trade-off**: **ML training only**—not for tabular anonymization or synthetic data. **Best for**: ML engineers wanting to train models with formal DP guarantees—especially those already in PyTorch.



- **SecretFlow**

  **Unified framework for privacy-preserving data analysis and ML** (Apache 2.0) — **the most comprehensive open-source privacy framework**, covering DP, MPC, and federated learning . **Features**: **Differential privacy**; **secure multi-party computation (MPC)**; **federated learning**; **split learning**; **TEE integration**; designed for enterprise privacy-preserving analytics . **Tech stack**: Python, C++. **Deploy**: Self-hosted. **Trade-off**: **Complex framework**—steep learning curve; not a turnkey anonymization tool. **Best for**: enterprises building comprehensive privacy-preserving data platforms—willing to invest in framework adoption.



- **DPMM**

  **Synthetic tabular data generation with DP guarantees** (open source, from SAS) . **Features**: **DP synthetic tabular data**; **end-to-end DP guarantees**; rich functionality for synthetic data generation . **Tech stack**: Python. **Deploy**: Self-hosted. **Trade-off**: **Narrower than Gretel**—synthetic tabular data only; smaller community. **Best for**: teams wanting open-source DP synthetic tabular data without managed platform costs.



### Additional Strong Open-Source Options



- **Microsoft DPSDA** — Private Evolution for generating DP synthetic data without training (ICLR 2024) . **Note**: Research implementation; not production-hardened. **Best for**: researchers exploring DP synthetic data generation.

- **SAP SPRINT** — DP fine-tuning and inference for transformers via MPC . **Note**: Specialized for transformer models; complex setup. **Best for**: teams needing DP fine-tuning of LLMs.

- **OpenMined PyDP** — Python DP library built on Google's differential-privacy . **Note**: Alternative to Diffprivlib; smaller community. **Best for**: teams wanting Google-backed DP primitives.



**Frameworks for building custom systems**: Combine **IBM Diffprivlib** for DP primitives with **Opacus** for DP ML training and **Tumult Analytics** for DP aggregates—creating a complete open-source DP stack. **For synthetic data**, **DPMM** and **SecretFlow** provide generation capabilities. **None of these match Gretel's managed workflows**, but for teams building custom pipelines, the libraries are production-capable.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Differential privacy and anonymization tools handling sensitive data must comply with data protection regulations (GDPR, CCPA, HIPAA, etc.). **Differential privacy provides formal guarantees, but implementation errors can void them**—validate configurations with privacy experts.

- **The "managed synthetic data" vs. "DP library" vs. "DP ML training" vs. "privacy framework" distinction is critical.** **Gretel.ai, Mostly AI, Tonic.ai, Hazy, Statice, and Synthesized** are **managed synthetic data platforms**—they generate privacy-safe datasets with managed infrastructure . **Snowflake Differential Privacy** provides **native DP** within clean rooms—entity-level noise injection for aggregate queries . **IBM Diffprivlib and Tumult Analytics** are **DP libraries**—primitives for building custom DP pipelines . **Opacus** is **DP ML training**—DP-SGD for PyTorch models . **SecretFlow** is a **privacy framework**—combining DP, MPC, and federated learning . **Choose based on whether you need synthetic data, DP aggregates, DP models, or a comprehensive framework.**

- **Gretel's free tier is the most generous for synthetic data**—15 credits/month covers ~100K synthetic records . **The trade-off**: no credit rollover; 2 concurrent workers on free tier.

- **Mostly AI's 2 credits/day** is designed for experimentation, not production—**daily top-up, no rollover** . **For sustained use, contact sales.**

- **Tonic.ai's free tier is $5 credits/month**—sufficient for ~9 complex sessions . **The $29/month plan adds $25 credits.**

- **Hazy's free tier up to 100K rows/day** is the most generous daily allowance in this category . **Developer tier at $100/month is accessible for small teams.**

- **Synthesized's SDK is free with DP guarantees built in**—including self-hosting on private cloud/on-premise . **For teams wanting self-hosted synthetic data with DP, it is the most accessible entry point.**

- **Snowflake Differential Privacy is Clean Room-only**—it cannot be used outside clean room queries . **Do not evaluate it as a standalone anonymization tool.**

- **Statice and Privitar have no free tier**—Statice offers trial only; Privitar is quote-only . **Evaluation requires sales engagement.**

- Self-hosted open-source solutions require proper setup and privacy expertise. **DP guarantees depend on correct epsilon selection and budget accounting**—ensure your deployment includes privacy review before publishing DP results or synthetic data.



---



**Made for privacy engineers, data scientists, and organizations building transparent anonymization solutions.**

Let's make Differential Privacy & Data Anonymization more open, data-driven, and privacy-safe.
