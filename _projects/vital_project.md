---
layout: page
title: Vital
description: Democratizing healthcare with non-invasive disease prediction.
img: assets/img/projects/vital_preview.png
importance: 2
category: Artificial Intelligence
giscus_comments: false
---
*You can access the English version of the web app at [vital-client.web.app](vital-client.web.app).* *The Chinese version can be found at [kanger-vital.web.app](vital-ai.web.app).*

My experiences in exploring several rural Chinese villages highlighted the lack of professional medical knowledge and healthcare services in these areas. While the [KangEr Project](https://zehao.tech/projects/kanger_project/) seeks to bring medical knowledge in the palm of the villager's hand through an accessible LLM chatbot web application, it doesn't actively alert the onset of diseases, but requires the user to phrase their query to the AI doctor.

However, diseases like cardiovascular diseases and diabetes are often asymptomatic in the early stages, and the lack of professional medical resources in rural areas makes it difficult to detect these diseases in time. Indeed, in rural China, cardio diseases accounted for nearly **half** of all deaths, and an **eighty percent** prevalence rate of chronic diseases existed. Yet, preventions like basic medications could have averted the heart attack with early detection. 

***Can we make disease predictions more accessible?*** This is the question that Vital seeks to answer.

Hence, I crafted the Vital app out of scratch, which aims to democratize healthcare by providing a **non-invasive**, **efficient**, and **accessible** way to predict disease risks. Using just a webcam, Vital leverages artificial intelligence to extract and analyze vital signs from a simple 45-second video of the user. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/vital_demo_1.png" title="Vital Recording Interface" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/vital_demo_2.png" title="Vital Disease Page" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/vital_demo_3.png" title="Vital Risk Page" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A glimpse into Vital's web app, showcasing its recording interface, health score page, and risk assessment page. The recording interface guides the user to correct position the head. The health score page displays the user's corresponding health score at each category, while the risk assessment page provides a detailed breakdown of the user's disease risks.
</div>

At first, Vital employs a **facial recognition** model to align the user's position accurately in front of the webcam. This step is crucial to ensure the user's head is stable and correctly oriented, preventing any inaccuracies in data capture that could affect the final disease prediction. 

Then, when blood flows through facial skin, it affects light absorption and reflection due to its varying volume and oxygenation levels. These changes cause subtle variations in skin color that, although not visible to the naked eye, can be detected by advanced imaging techniques. As the heart beats, these color shifts align with the cardiac cycle, providing a pulse signal that allows for non-invasive monitoring of heart rate and other cardiovascular attributes. The process of extracting this signal is named as the **remote-photoplethysmograph (rPPG) technology**. I've trained a custom deep-learning model to analyze these patterns using **1D CNNs** (which actually outperforms larger models like LSTM), achieving **state-of-the-art** accuracy and speed.

The pulse signal is correlated with various vital signs, such as blood pressure (BP), oxygen saturation (SpO2), and heart rate variability (HRV). Hence, I use both literature-backed statistical methods and custom-developed deep learning models, including Long Short-Term Memory (LSTM) networks, to translate PPG signals into **15** distinct vital biometrics accurately and reliably.

Utilizing the biometric data, Vital assesses the risk for **14** diseases, categorized into cardiac, mental, metabolic, and respiratory. The application compares these indicators against normal ranges based on the user’s **age**, **sex**, and **ethnicity**, categorizing disease risks into low, medium, and high levels for intuitive understanding.

Indeed, **Ethical considerations** should be acknowledged in relation to health applications using AI, particularly regarding accountability in cases of misdiagnosis. The AI models that I've trained on professional datasets have been endorsed by academic research and rigorously tested in both experimental and real-world settings and demonstrate high accuracy. For instance, Vital's heart rate measurements exhibit a minimal error margin of only **1 BPM** in controlled environments and **2 BPM** in real-world scenarios, while blood pressure readings are within a mere **5 mmHg margin of error**. Its disease prediction methods are grounded in techniques detailed in PubMed literature, and we maintained track of the literature we alluded to for the app’s validity (an example reference is [here](https://pubmed.ncbi.nlm.nih.gov/20980134/)). 

Vital has been distributed among healthcare professionals, enthusiasts, and novices. Feedback has been overwhelmingly positive from a total of 30 participants, with **24** expressing satisfaction. Notably, healthcare novices report and emphasize our app’s ease of use and enhanced self-awareness of their health conditions, while professionals acknowledge its credibility in practical applications. The less favorable feedback primarily comes from individuals with established health-checking routines or those of skeptics.

Vital is the first time that I've trained my own AI model that serve to help people in a practical way. The training process was smoothly thanks to my years of experience in AI, but the development process was challenging. I decided on using WebRTC for video streaming–because the user's video data needs to be delivered in real-time to the server to check the user's head position constantly–but the inmaturity of the WebRTC technology compared to other data streaming technologies like WebSockets made the development process more difficult. Different browsers have different specifications. Yet, Flutter's `flutter_webrtc` package also led to a lot of debugging. Particularly, I spent three days trying to figure out how to make WebRTC work on Safari while it worked perfectly on Chromium browsers, and it turns out that the only thing I needed to do was to use `"urls"` instead of `"url"` for configuring ICE servers. This was pretty frustrating; I even had a [GitHub issue](https://github.com/flutter-webrtc/flutter-webrtc/issues/1550) that gained some community attention.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/vital_situation.png" title="US Healthcare Situation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/vital_market.png" title="US Vital Market" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Healthcare situation and Vital's potential market in the US.
</div>

Nevertheless, the experience of developing KangEr and Vital famaliarizes me with using **Flutter** to develop cross-platform applications. Yet, I am also equipped with adequate **Nginx**, **Linux**, and **Internet** skills that would power up my future career of development. Most importantly, they prove to me that I could use what I've learnt to pay back the society and achieve my self-actualization of using technolgy to help people.

Currently, I have integrated Vital into KangEr and am looking forward to promote it in person in different villages. I have also created an English version of the app, so that it could reach a wider audience and help more people, starting from the US. Its journey has just begun; it will democratize healthcare globally, step by step.