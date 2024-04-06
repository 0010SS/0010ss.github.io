---
layout: page
title: TwoStep
description: An all-in-one travel companion that makes your journeys easier.
img: assets/img/projects/twostep_1.jpg
importance: 1
category: Development
related_publications: false
---
I attended LaunchX in the summer of 2023, aiming to acquire business skills to market my existing technologies. It was my first time traveling outside Asia and flying solo internationally. The experience was exhilarating yet daunting: mavigating a foreign airport, especially the labyrinth of Detroit's, was a challenge due to unfamiliar procedures and cultural nuances (although I did manage to arrive safely at UMich).

This adventure inspired the creation of TwoStep, a travel companion app designed with my LaunchX team to simplify journeys, particularly in unfamiliar airports. The name **TwoStep** signifies the streamlined process of departing your home and arriving at your destination.

Interestingly, even my U.S.-based teammates found the Detroit airport bewildering. We could have based the app's features on our experiences, but I had learned from past failures that sometimes *what you think is the best solution might not be the best solution for others*. It is important to understand the real needs of users, since we were aiming to build an app that could help as more as we can (helping me to somewhat achieve my self-actualization), which couldn't have been done without extensive market research.

Hence, we embarked on the tiring journey of research. I could still remember the five of us tiredlessly striked up a conversation on the street of UMich, asking people about their travel experiences and, specifically, their pain points. Our orange LaunchX t-shirts were as bright as the sun, so did our enthusiasm. It was amazed to see how people were willing to share their stories with us, and we did carry out **more than 60** insightful interviews in an afternoon.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_market_2.png" title="Market Research results" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_market_1.png" title="Market Research Doc Demo" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_market_3.jpeg" title="Me and my teammates" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The results of our market research, an example of our market research document, and a photo of me and my teammates wearing the LaunchX T-shirts for interviews.
</div>

This was my first foray into customer segmentation and market interviews. It was tired physically, but mentally, it was a rewarding experience. I learned how to talk in a way that could make people feel comfortable sharing their stories, and how to direct the conversation that could lead to the most insightful answers. Surprisingly, it also helped me to know more about the United States, and its divered population. I even met a college professor who was willing to share, and when I found out that he was looking at computing servers, I recommended to him the IBM Quantum Lab, which interested him so much that he even came back to me when we've done another round of interview at Starbucks to say a big thank you.

Common pain points we discovered were the **lack of clear directions in airports**, the **lack of information about the destination** (e.g., culture and immigration policies), the **language barrier**, and the **transportation problem**. These were a superset of the problems we faced in Detroit, and we couldn't have noticed them without the interviews.

We decided to tackle them all. Yet, I didn't jump right into coding but listing out a detailed plan of what features we should have in the app and their justifications. Thinking before doing was a lesson I learned from my previous failures; it would actually make the implementation process much smoother and more efficient. 

The final features of the app are listed with the cool visuals below. **FlyMate AI**, in particular, is an AI chatbot that answers any of your queries, even specific to the location of Starbucks in an airport. This was the crystalization of my previous experiences with Large Language Models.

<div class="row">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_3.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_4.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_5.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_6.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_7.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_8.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_9.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_10.jpg" title="TwoStep Features" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The ten core features of the app <b>TwoStep</b>, helping you to nabigate smoothly through both an unknown airport and a foreign country.
</div>

With a clear feature set, it was time to code. Though I was skilled in Python for AI and Blazor for web development, mobile app development was new to me. It was challenging, requiring me to learn mobile development step by step while advancing the prototype. Thankfully, my proficiency in using ChatGPT did save me a lot of time in development, and it even became my GF (stands for "GPT friend").

The development journey was arduous, yet it honed my problem-solving skills and taught me to swiftly find solutions online. <u>I learned SwiftUI from scratch, implementing the ten core features in just two weeks.</u> I believed that even years later, I would still cherish this experience, where I had the chance to immerge myself whole-heartedly to the progamming world. I was with my computer, wearing my bucket hat all day along, coding at the hallway, the cafeteria, the classroom, everywhere. My teammates and I could be found at anytime at the study room after lunch or dinner; people even thought that we've "conquered" that room (shout out to my equally motivated teammates, we couldn't have crafted the app without the great team spirit and atmosphere that we had). *It was such a pleasure and probably a once-in-a-lifetime opportunity to do something that you love, without any distractions.*

Again, this couldn't have been done without my teammate, who helped manage all the UX, marketing, branding and financials stuff so that I could focus solely on my code. It taught me the importance of teamwork in terms of a start up: everyone has their own expertise, and it is pivotal to trust each other and work together to achieve the common goal.

<div class="row">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_code_1.jpeg" title="TwoStep Code" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_code_3.jpeg" title="TwoStep Code" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_code_2.jpeg" title="TwoStep Code" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Instagram stories that I've posted during LaunchX and a showcase of the code.
</div>

Our hard work did pay off: TwoStep generated $1130 in revenue at the end of the progam, capturing the attention of a panelist who offered mentorship post-pitch. My performance at LaunchX earned me the **Best Developer** and **Most Driven** awards among a cohort of 75, as endorsed by peers and faculty. 

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="assets/img/projects/twostep_demo.mp4" height='30%' width='30%' controls=1 title="TwoStep Demo"%}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="assets/img/projects/twostep_3d.mp4" height='30%' width='30%' controls=1 title="TwoStep 3D video"%}
    </div>
<div class="caption">
    A walkthrough of <b>TwoStep</b> and a 3D video of the app's features.
</div>

When I uploaded the final prototype to GitHub, my emotions were mixed. Reviewing the **8,000** lines of code I crafted over two weeks, I didn’t feel the expected relief of completing a major project. Instead, a **growing sense of confidence** emerged. Reflecting on the LaunchX experience, it was a journey of self-affirmation. Physically, I proved to myself that I could survive and thrive alone in a foreign country for a month, working tirelessly regardless of time. Mentally, I demonstrated my ability to learn quickly and achieve my goals, crafting a fully functional app with impressive features in just two weeks. It reinforced that the **only limits are those we impose on ourselves.**

Beyond coding, LaunchX taught me the full spectrum of launching a business, from market research and prototyping to marketing and building a startup. It was where I captured the essence of combining technology with entrepreneurship. Entrepreneurship isn't just about making money; merchants make money. Only through entrepreneurship can one identify appropriate market needs for technology, build prototypes that directly address these needs rather than unused technologies, and market the final product to those who truly need it. This is a process that allows technology to effectively serve society.

However, the most valuable aspects were the experiences and connections forged. Scrolling through my photo library, I always pause at the LaunchX photos, reminiscent of those formative times. I’d love to share these memories with you.

<div class="row">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_memory_3.jpeg" title="TwoStep Memories" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_memory_1.jpeg" title="TwoStep Memories" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_memory_4.jpeg" title="TwoStep Memories" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_memory_5.jpeg" title="TwoStep Memories" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_memory_2.jpeg" title="TwoStep Memories" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/twostep_memory_6.jpeg" title="TwoStep Memoris" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    LaunchX memories.
</div>