---
layout: about
title: about
permalink: /
# subtitle: Postdoc at FAIR, Meta. Trustworthy Machine Learning. Privacy & LLMs.

profile:
  align: right
  image: hongyan-2026.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <div class="social" style="font-size: 1.5em; margin-top: 10px;">
      <a href="mailto:changhongyan0530@gmail.com" title="Email" style="margin-right: 15px;"><i class="fa-solid fa-envelope"></i></a>
      <a href="https://github.com/changhongyan123" title="GitHub" style="margin-right: 15px;"><i class="fa-brands fa-github"></i></a>
      <a href="https://scholar.google.com/citations?user=5d1AHgIAAAAJ" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
    </div>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am **Hongyan Chang (常红燕)**, a postdoctoral researcher at FAIR, Meta, in the [Content Seal team](https://facebookresearch.github.io/content-seal/). My research focuses on **AI security**, particularly **agentic security**, **data and model distillation**, and **model provenance**. I study how AI systems can be attacked, how training data and model capabilities are reused, and how we can detect and mitigate these risks.

Before joining Meta, I was a postdoctoral researcher at MBZUAI working with [Prof. Ting Yu](https://mbzuai.ac.ae/study/faculty/ting-yu/). I obtained my Ph.D. in Computer Science from the National University of Singapore, advised by [Prof. Reza Shokri](https://www.comp.nus.edu.sg/~reza/). I received my bachelor's degree in 2018 from the University of Electronic Science and Technology of China (UESTC), and was an exchange student at National Chiao Tung University in 2016.

I was a research intern at **Brave** (2024), mentored by [Ali Shahin Shamsabadi](https://alishahin.github.io/), [Kleomenis Katevas](https://minoskt.github.io/), and [Hamed Haddadi](https://haddadi.github.io/about/), and at **[Intel's Security and Privacy Lab](https://www.intel.com/content/www/us/en/research/security.html)** (2022), mentored by [Brandon Edwards](https://www.usenix.org/conference/usenixsecurity24/speaker-or-organizer/brandon-edwards-intel-corporation) and [Anindya S. Paul](https://medicine.ufl.edu/profile/paul-anindya/).

### Research

My work is organized around the following research questions. See also [publications by year]({{ '/publications/' | relative_url }}) and [Google Scholar](https://scholar.google.com/citations?user=5d1AHgIAAAAJ).

{% for theme in site.data.research_themes %}
#### {{ theme.title }}

**{{ theme.question }}** {{ theme.description }}

<ul>
{% assign theme_papers = site.data.research_papers | where: 'theme', theme.id | sort: 'sort_date' | reverse %}
{% for paper in theme_papers %}
{% include research-paper.liquid paper=paper %}
{% endfor %}
</ul>
{% endfor %}

---

### PC services
<!-- - External Reviewer for VLDB 2026
- PC member for ICLR 2025, NeurIPS 2025, ICLR 2026 
- AE PC member of NDSS 2025, USENIX 2025, NDSS 2026
- Reviewer of IEEE Security & Privacy 2024 ([Certificate]({{ site.url }}{{ site.baseurl }}/assets/pdf/certificate.pdf))
- PC member of ACM FAccT Conference 2022, 2023
 -->

- 2026: VLDB (External Reviewer), ICLR (Reviewer), NDSS (AE Reviewer), USENIX (AE Reviewer), CCS (Reviewer)
- 2025: ICLR (Reviewer), NeurIPS (Reviewer), NDSS (AE Reviewer), USENIX Security (AE Reviewer)  
- 2024: IEEE Security & Privacy (Reviewer, [Certificate]({{ site.url }}{{ site.baseurl }}/assets/pdf/certificate.pdf))  
- 2023: ACM FAccT (Reviewer)  
- 2022: ACM FAccT (Reviewer)


---

### Selected Awards
- [Distinguished Reviewer Awards](https://secartifacts.github.io/usenixsec2025/awards#-distinguished-reviewer-awards:~:text=Hongyan%20Chang%2C%20National%20University%20of%20Singapore) in USENIX 2025 (Artifact Evaluation)
- [Notable Reviewer](https://iclr.cc/Conferences/2025/Reviewers) in ICLR 2025
- Best paper award at FAccT in 2023 ([Certificate]({{ site.url }}{{ site.baseurl }}/assets/pdf/facct_award.pdf))
- Research Achievement Award in 2023 by NUS School of Computing
- Funded participant of the [IPAM Graduate Summer School on Algorithmic Fairness](https://www.ipam.ucla.edu/programs/summer-schools/graduate-summer-school-on-algorithmic-fairness/?tab=overview) in 2022
  - Organized by Noa Dagan, Cynthia Dwork, and Guy N. Rothblum
- National University of Singapore Research Scholarship (2018–2022)
- First Prize of the 10th National Information Security Competition (2017) on fake news detection for WeiBo
- National Scholarship (2015 & 2016, top 1%)


---


### Open-source Projects

- **TextSeal @ Meta**: Text watermarking for provenance and distillation detection. [GitHub](https://github.com/facebookresearch/textseal).<br>
  **My role**: contributing to the research, including the watermark-based distillation detection study in TextSeal.

- **Privacy Meter @ NUS**: A system for evaluating the privacy risks of machine learning models. <i class="fa-brands fa-github"></i> [GitHub](https://github.com/privacytrustlab/ml_privacy_meter)<br>
  **My role**: leading the development team and spearheading the initial [1.0.1 release](https://pypi.org/project/Privacy-Meter/).

- **OpenFL @ Intel**: Auditing privacy risks in real-time. <i class="fa-brands fa-github"></i> [GitHub](https://github.com/securefederatedai/openfederatedlearning/tree/develop/openfl-tutorials/experimental/workflow/Privacy_Meter). [Blogpost](https://www.intel.com/content/www/us/en/developer/articles/technical/how-openfl-and-privacy-meter-empower-data-privacy.html).<br>
  **My role**: leading the integration of privacy meter into OpenFL.

---

### Teaching Experience

- Teaching Assistant for Trustworthy Machine Learning (Summer 2021, 2022, 2023)
- Teaching Assistant for Computer Security (Spring and Summer 2020)
- Teaching Assistant for Introduction to Artificial Intelligence (Spring 2019)


---


### Talks

**Watermark in Large Language Models**
- WMARK@ICLR, 2025 (poster)

**Privacy in Federated Learning**
- USENIX, 2024

**Fairness in Federated Learning**
- FL@FM-Singapore, 2024
- Brave, 2024
- ICLR, 2024 (poster)
- N-CRiPT, 2023

**Trade-off in Privacy and Fairness**
- Private AI Collaborative Research Institute held by Intel, 2022
- CyberSec&AI, 2021
- PrivacyCon, 2021 by the **US Federal Trade Commission (FTC)**


---

<div style="text-align: center; margin-top: 30px; font-size: 0.9em; color: #666;">
  <img src="https://hits.sh/changhongyan123.github.io.svg?style=flat&label=visitors&color=2698ba" alt="Visitor counter">
</div>
