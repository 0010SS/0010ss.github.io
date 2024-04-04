---
layout: page
title: KangEr (康尔)
description: Accessible healthcare Q&A with LLMs
img: assets/img/12.jpg
importance: 1
category: Artificial Intelligence
related_publications: true
---
*You can access the web app at [kanger-ai.web.app](kanger-ai.web.app).*

Despite claims made by those AI pioneers, like Sam Altman, that AI can narrow wealth disparities by boosting the productivity of the underprivileged, it appears that these communities lack both awareness and access to AI technologies. This situation is **paradoxical**, as AI should ideally serve as a catalyst for inclusive societal and economic advancement, reminiscent of past industrial revolutions. Therefore, I decided to promote the accessibility of AIinto thoese underprivileged communities myself, and the Chinese rural village becomes a great starting point.

Due to my family origins, I've always been visiting different distant villages in China-some of them even take a 2 hours mountain ride to reach from the nearest city. Hence, due to geographical and economic reasons, these communities often lack access to healthcare and medical knowledge - only a few, i.e., one, rural doctors are in the village to provide basic healthcare services for the residents. 

This realization comes to me at the time I was doing research on Large Language Models(LLMs)–why can't these text giants be used as doctors? The large training data (and with some healthcare domain-specific data) provides LLMs with sufficient knowledge to understand healthcare-related queries, and its natural language interface lowers the barrier of knowledge acquisition, making it easier for people with less education experience to understand than obscure textbooks or blogs. LLMs also provide a customized interaction where you can ask any specific questions that you'd like

Hence, I did tons of experiments with medical Q&A with ChatGPT (GPT-3.5-turbo) in Chinese, aiming to test the quality and authenticity of this LLM's output. However, the problem of hallucination does exist, as illustrated by the picture below:

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_hallucination.png" title="ChatGPT Hallucination" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/kanger_hallucination.png" title="ChatGPT Hallucination" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    When I queried GPT-3.5-turbo about the Reiter's syndrome in Chinese, it replies me with a completely wrong description. However, RAG solves this, as shown by the response of KangEr to the right.
</div>

This is unacceptable for a medical related application. Luckily, the concept of Retrieval-Augmented Generation (RAG) appears at the time, which solves the hallucination issue by prompting LLMs with the correct information searched from the internet, as evident by the graph above. Yet, GPT-3.5-turbo does not have this ability then.

GPT-3.5-turbo also shows its deficiency in understanding and generating Chinese, yet I can't bear the cost of GPT-4 APIs, and therefore I switched on using the API provided by iFlyTek, a Chinese AI company, and crafted the app based on the API.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
