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

`GPT-3.5-turbo` also showed its deficiency in understanding and generating Chinese, yet the cost of `GPT-4` APIs was prohibitive. I opted instead for iFlytek's API, integrating RAG capabilities and prompt engineering into their model `iFlytekSpark-3.1`, resulting in the **KangEr (康尔) web app**.

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

---
### Technical Updates (2023-06-03)
I am dedicated to continuously perfect the app so that it can reach a larger audience and realistically help people in the underpriviledged areas. Four core features of KangEr have been updated to enhance accuracy and accessiblity.

#### 1. More powerful LLM Backbone
IFlyTeck has just released a new version of their LLM, `iFlyTekSpark-3.5`, which, as announced by the company, has a comparable performace with the state-of-the-art `gpt4-turbo` (although in practice the qualitative result lacks a bit). The new model has been integrated into KangEr. The system prompt ability also comes with the new API, and, by rounds of prompt engineering, I finally managed to make the model generate responses adhering to the healthcare aspect (as previously it will generate irrelevant content). The new backbone is exceptional in generating longer responses and answering multi-round questions, which are foundamental for a more holistic understanding of the problem and for diving deeper into a specific issue.

#### 2. More accessible Speech-to-Text and Text-to-Speech APIs
Since KangEr mainly focuses on rural areas, where the literacy rate is relatively low, voice accessiblity becomes a crucial ability. The previous version handles this issue with two local Flutter packages, `flutter_tts` and `speech_to_text`, which, on most devices, are working fine. However, these packages function through calling the local STT or TSS APIs of the browser or the phone, but many relatively cheaper devices in rural areas would lack these API. Hence, I decide to integrate Baidu's STT and TTS APIs, which are more robust and can be accessed through the web. These cloud-based APIs are not only device-independent but also more able in (i) detecting longer sequences and (ii) generating natural voices. 

Baidu's APIs are the choice I made due to its cost-efficiency and connectivity in China, comparing to the iFlyTeck's and the Azure's. Several tetchnical difficulties should been mentioned when interating the APIs. The documentation doesn't mention that the API endpoints practice CORS policy, and hence I have to set up a proxy server to bypass the restriction. Also, many Flutter packages are not optimized for web, and hence I have to write raw code to query the Media APIs of the browser for playing audio. The Media API doesn't work for audio recording used for STT, as it records in the `.webm` format which is not supported by Baidu's API, yet the conversion is difficult. Hence, I use the `record` package for recording. Notably, the `record` package doesn't work for Flutter web app built with `--web-renderer` set specifically to `canvaskit`, but the `auto` setting works fine even though it still uses `canvaskit` for desktop devices. Another technical detail is that the `flutter-svg` package, when the rendering engine is `html`, will directly use the color specified by the `fill` property in the SVG file for any image, instead of using the color specified by the `color` property in the `SvgPicture` widget. Hence, I have to manually change the color in the SVG file to make the image look good.

Sadly, Safari on MacOS seems to have a bug that doesn't allow voice to be accurately captured and transcribed through STT, yet, fortunately, this bug doesn't occur on any other browser or device. I am still investigating the issue.

#### 3. Variable Font Size
KangEr aims at a diversed user group covering different age groups and education levels. Hence, the font size should be adjustable to cater to the needs of different users (e.g., the elderl who needs large fonts or the visually imparied). The previous version uses a fixed font size and the font size is 12pt for body text and 14 pt for titles, which is not user-friendly. I have updated the app to allow users to adjust the font size, in real time, smoothly with a slider. The font size can be adjusted from 10px to 20px for body texts, as larger fonts will crowd the screen and make it unreadable. The font size is stored in the local storage of the browser, and the app will remember the user's preference when they revisit the app. Users will be directed to the help and setting page immediately when they first visit the app, where they can adjust the font size.

#### 4. Adaptive Rendering Engine
Frankly speaking, the biggest drawback of KangEr is its long initial waiting time for the web app to build, arised due to Flutter Web's inefficiencies. I've always tried to mitigate this issue. Previously, both desktop and mobile devices use the same rendering engine, `canvaskit`, which is not optimized for mobile devices and require a relatively long rendering time, despite better rendering quality and colors. The updated version of KangEr will use `html` as the rendering engine for mobile devices, with `canvaskit` still as the engine for the desktop platform, which is more local and will significantly reduce the initial waiting time. The rendering quality will be slightly reduced (and some components don't even have a right color), yet the deficiency is indetectable for most users as KangEr's UI is relatively straightforward.