---
title: "Home"
layout: homelay
sitemap: false
permalink: /
---

### About me

I am a Ph.D. student at the National University of Singapore’s School of Computing working under the supervision of [Reza Shokri](https://www.comp.nus.edu.sg/~reza/). My research interests are in the privacy and fairness of machine learning, federated learning and Large Language Models. 



<style>
.jumbotron{
    padding:3%;
    padding-bottom:10px;
    padding-top:10px;
    margin-top:10px;
    margin-bottom:30px;
}
</style>

<div class="jumbotron">
<h4>Publications</h4>
{% bibliography%}
</div>

<div class="jumbotron">
  <h4>Open Source Library</h4>
  - [Privacy Meter @ NUS](https://github.com/privacytrustlab/ml_privacy_meter): A valuable resource for privacy research and deployment. 500+ stars on GitHub.
    - Leading the development team and spearheading the initial 1.0.1 release.    
  - [OpenFL @ Intel](https://github.com/intel/openfl/): Auditing privacy risks in real-time. 
    - Leading the integration of privacy meter into OpenFL ([Blogpost](https://www.intel.com/content/www/us/en/developer/articles/technical/how-openfl-and-privacy-meter-empower-data-privacy.html)).
</div>

<div class="jumbotron">
  <h4>Talks</h4>
  - Fairness in Federated Learning.
    - FL@FM-Singapore, 2024.
    - Brave, 2024.
    - N-CRiPT, 2023.
  - Trade-off in Privacy and Fairness.
    - Private-AI, 2022.
    - Chaspark by Huawei, 2022.
    - CyberSec&AI, 2021. 
    - PrivacyCon, 2021 by the US Federal Trade Commission (FTC).
</div>


{% if site.data.services %}
<div class="jumbotron">
  <h4>Service</h4>
  <ul>
    {% for service in site.data.services %}
      <li>{{ service.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}


{% if site.data.awards %}
<div class="jumbotron">
  <h4>Awards</h4>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}



{% if site.data.awards %}
<div class="jumbotron">
  <h4>Teaching Assistantships</h4>
  <ul>
    {% for ta in site.data.teaching %}
      <li>{{ ta.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

