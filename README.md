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
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Gretel.ai**
  **Synthetic data platform** for tabular, text, and time-series data. **Pricing**: **Free tier with 15 monthly credits** (enough for ~100K synthetic records via Workflows, ~2M Transform records, or ~2M PII detection records); **$2.00/credit** beyond free tier; **Team $295/month** (10 concurrent jobs, 99.5% API SLA, pooled credits) . **Free tier**: Yes, 15 credits/month (no rollover). **Best for**: teams wanting managed synthetic data with PII detection—**trade-off**: credit consumption scales with data complexity; free tier limits concurrency to 2 workers.

- **Mostly AI**
  **Synthetic data platform** for high-fidelity tabular data. **Pricing**: **Free tier with 2 new credits daily** (enough for experimentation); heavier usage requires purchasing credits or contacting sales . **Free tier**: Yes, 2 credits/day (auto top-up). **Best for**: teams wanting daily free experimentation with synthetic tabular data—**trade-off**: daily credit limit restricts production use.

- **Tonic.ai**
  **Data de-identification and synthesis** platform. **Pricing**: **Free tier with $5 monthly credits** (~9 complex generation sessions); **$29/month plan** with $25 usage credits; additional usage metered; no credit card required for free tier . **Free tier**: Yes, $5 credits/month. **Best for**: developers wanting to try relational synthetic data generation—**trade-off**: token-based metering; complex schemas consume more credits.

- **Hazy**
  **Synthetic data for banking, finance, and telecom**. **Pricing**: **Free forever tier up to 100K rows/day**; **Developer tier from $100/month**; enterprise custom licenses . **Free tier**: Yes, 100K rows/day. **Best for**: regulated industries wanting synthetic data with generous free tier—**trade-off**: enterprise pricing for production scale.

- **Statice**
  **Anonymous synthetic data** for enterprises. **Pricing**: **No free version**; **free trial available**; starting price not provided by vendor . **Free tier**: Trial only. **Best for**: enterprises wanting irreversibly anonymous synthetic datasets—**trade-off**: no free tier; quote-only pricing.

- **Synthesized**
  **Synthetic data SDK with differential privacy**. **Pricing**: **Free SDK** with unlimited generative models and datasets; **default in-built differential privacy guarantees**; **Solo Edition free** adds production sensitive data support, private cloud/on-premise self-hosting, Docker images . **Free tier**: Yes, generous SDK with DP guarantees. **Best for**: developers wanting self-hosted synthetic data with DP built in—**trade-off**: Platform Enterprise requires demo.

- **Snowflake Differential Privacy**
  **Native DP within Snowflake Data Clean Room**. **Pricing**: Included with Snowflake Clean Rooms; consumption-based credits. **Free tier**: Trial credits. **Best for**: Snowflake customers wanting entity-level privacy in clean room queries—**trade-off**: requires Clean Room configuration; DP not available outside clean rooms .

- **Privitar**
  **Data privacy platform** for sensitive data provisioning. **Pricing**: **Quote-only**; pricing available upon request; no free version listed . **Free tier**: None. **Best for**: enterprises wanting policy-driven data de-identification—**trade-off**: no self-serve; sales-led.

- **K2View**
  **Data product platform** with anonymization capabilities. **Pricing**: **From £1,000/year** per Capterra listing . **Free tier**: None. **Best for**: teams wanting data products with built-in anonymization—**trade-off**: broader platform; anonymization is one capability.

- **LeapYear (Snowflake)**
  **Differential privacy for Snowflake** (acquired by Snowflake). **Note**: LeapYear's technology is now integrated into Snowflake's Differential Privacy offering; standalone availability no longer exists. **Best for**: historical reference—evaluate Snowflake Differential Privacy instead.

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
