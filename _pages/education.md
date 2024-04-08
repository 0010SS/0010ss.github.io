---
layout: page
permalink: /education/
title: Education
description: My education journey and resources.
nav: true
nav_order: 2
---

I am currently a junior at [Shenzhen College of International Education](scie.com.cn), where I've been deeply involved in both academic and extracurricular activities. As the co-founder of the **Machine Learning X Artificial Intelligence (MLXAI)** club, one of the biggest club at SCIE, I've spearheaded efforts to bring AI knowledge to our student body, growing the club to over 150 members in just two years. Additionally, I lead the [**SCIE Developers club**](scie.dev), our school's most prestigious computer science club, where we engage over 70 students in hands-on software development projects and contribute to maintaining the school’s digital infrastructure.

Beyond academics, I co-founded the **SCIE Tai-Chi Club** to introduce the ancient practice of Tai Chi, which has significantly benefited my physical and mental well-being in the past 4 years, to our international school community. My commitment to school life extends to my upcoming role on the **Student Executive Leadership Team**, where I will collaborate with the school's management to enhance the campus environment and student life, overseeing the **Student Leadership Body** of more than 100 vibrant student leaders.

My academic journey reached a milestone when I received the **Top in China** award for IGCSE Computer Science, an achievement made possible through years of sharing my study resources with classmates. Below are the notes and resources I've created that encompass several IG and AS subjects. Hope you find them helpful!

### Resources

You may click the name to download.

<div class="row">
    {% for note in site.data.selected_projects %}
        <div class="col-sm-3">
            <a href="{{ note.url | relative_url }}" download>
                <div class="card hoverable">
                    <img src="{{ project.image | relative_url }}" loading="eager" sizes="200px" alt="project thumbnail">
                    <div class="card-body">
                        <h3 class="card-title">{{ project.name }}</h3>
                        <p class="card-text">{{ project.description }}</p>
                    </div>
                </div>
            </a>
        </div>
    {% endfor %}
</div>