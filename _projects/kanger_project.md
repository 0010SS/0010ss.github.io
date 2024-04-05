---
layout: page
title: KangEr (康尔)
description: Accessible healthcare Q&A with Large Language Models.
img: assets/img/projects/kanger_preview.jpeg
importance: 1
category: Artificial Intelligence
related_publications: false
---
*You can access the web app at [kanger-ai.web.app](kanger-ai.web.app).*

It's ironic that despite the promises of AI pioneers like Sam Altman that AI could narrow wealth disparities by boosting the productivity of the underprivileged, many communities lack both awareness of and access to AI technologies. This paradox highlights the missed potential for AI to act as a catalyst for inclusive societal and economic advancement, akin to past industrial revolutions. Therefore, I decided to champion AI accessibility in underprivileged communities, starting with rural Chinese villages.

My family roots have led me to explore numerous remote villages in China, some requiring a two-hour journey through mountains from the nearest city. These communities, due to geographical and economic constraints, often lack access to healthcare and medical knowledge, relying on just one rural doctor for basic services.

This realization struck me while researching **Large Language Models (LLMs)** and pondering why these text giants couldn't serve as virtual doctors. LLMs, with their extensive training data, seemed like ideal candidates. Their natural language interface also promised to bridge the gap for those with limited education, making complex medical knowledge more accessible than dense textbooks or obscure blogs. Moreover, LLMs offered personalized interactions, allowing users to ask specific questions.

Hence, I conducted numerous experiments with medical Q&A using ChatGPT (GPT-3.5-turbo) in Chinese to evaluate its authenticity and quality. However, I encountered a significant issue: **hallucination**, where the AI generated inaccurate responses, as illustrated below.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/chatgpt_hallucination.png" title="ChatGPT Hallucination" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_rag.png" title="KangEr with RAG" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    When I asked GPT-3.5-turbo about Reiter's syndrome in Chinese, it provided a completely inaccurate description. However, RAG solves this, as shown by the response of KangEr to the right.
</div>

This is unacceptable for a healthcare-related application. Fortunately, a solution emerged thanks to **Retrieval-Augmented Generation (RAG)**, which addressed the hallucination problem by prompting LLMs with correct information searched from the internet, as demonstrated by KangEr's accurate response to Reiter's syndrome above.

`GPT-3.5-turbo` also showed its deficiency in understanding and generating Chinese, yet the cost of `GPT-4` APIs was prohibitive. I opted instead for iFlytek's API, integrating RAG capabilities and prompt engineering into their model `iFlytekSpark-3.5`, resulting in the **KangEr (康尔) web app**.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_demo_1.png" title="KangEr Chat Interface" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_demo_2.png" title="KangEr History Page" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_demo_3.png" title="KangEr Help Section" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   A glimpse into KangEr's web app, showcasing its clean chat interface, a detailed history page with dates, and an intuitive help section.
</div>

This app allows users to **voice their questions and receive spoken answers**, overcoming literacy barriers in rural areas. Its **web-based** nature ensures accessibility across devices without requiring downloads, leveraging China's high mobile penetration rate of 99.8%.

I'm currently collaborating with rural health organizations to promote KangEr and plan to visit various villages to gather user feedback. This iterative process will tailor the app to real-life situations faced in rural areas. I believe KangEr has the potential to enhance both healthcare and AI accessibility in the often-overlooked parts of China's vast landscape, spanning 3,705,000 mi².