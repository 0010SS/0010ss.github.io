---
layout: page
permalink: /education/
title: Education
description: My education journey and resources.
nav: true
nav_order: 2
---

I am currently a senior at [Shenzhen College of International Education](https://scie.com.cn), where I've been deeply involved in both academic and extracurricular activities. As the co-founder of the **Machine Learning X Artificial Intelligence (MLXAI)** club, one of the biggest club at SCIE, I've spearheaded efforts to bring AI knowledge to our student body, growing the club to over 210 members in three years. Additionally, I lead the [**SCIE Developers club**](https://scie.dev), our school's most prestigious computer science club, where we have engaged over 130 students in hands-on software development projects and contribute to maintaining the school’s digital infrastructure.

Beyond academics, I co-founded the **SCIE Tai-Chi Club** to introduce the ancient practice of Tai Chi, which has significantly benefited my physical and mental well-being in the past 4 years, to our international school community. My commitment to school life extends to my role on the **Student Executive Leadership Team**, where I will collaborate with the school's management to enhance the campus environment and student life, overseeing the **Student Leadership Body** of more than 300 student prefects and members.

My academic journey reached a milestone when I received the **Top in China** award for IGCSE Computer Science, an achievement made possible through years of sharing my study resources with classmates. Below are the notes and resources I've created that cover several IG and AS subjects. Hope you find them helpful!

### Resources

[You may click the card below to download the `zip` file for each note collection.]()

<div class="note-section">
    {% assign counter = 0 %}
    <div class="row">
        {% for note in site.data.selected_notes %}
            <div class="col-sm-4">
                <a href="{{ note.url | relative_url }}" download>
                    <div class="card hoverable">
                        <div class="card-body">
                            <h3 class="card-title">{{ note.name }}</h3>
                            <p class="card-text">{{ note.description }}</p>
                        </div>
                    </div>
                </a>
            </div>
            {% assign counter = counter | plus: 1 %}
            {% if counter == 3 %}
                </div>
                <div class="row mt-3">
            {% endif %}
        {% endfor %}
    </div>
</div>