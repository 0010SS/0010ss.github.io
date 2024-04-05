---
layout: page
title: Optiway
description: Finding the optimal route to your next class.
img: assets/img/projects/optiway_1.png
importance: 1
category: Personal Development
related_publications: false
---
*The code is open-sourced on [Github](https://github.com/micfong-z/OptiWay.)*

### Introduction

As a student in [SCIE](scie.com.cn), the most suffering part of my daily life is to see the crowd of **2000 student** in the hallway during class breaks, moving forward as slow as a snail, colliding each other and making the hallway a mess. Hallways, classes, students... These entities immediately hinted me at the graph theory and the path optimization algorithms that I've learnt by enrolling in the USA Computing Olympiad. I then realized that the problem of congestion in SCIE is a perfect example of the graph theory problem, and I, together with my groupmate for my AS Level Computer Science class, decided to solve it by developing a software that can optimize the routes of students in SCIE to their next class, which fostered the emergence of OptiWay.

Existing methods (those presented in the previous Computer Science Fair in my school) for optimizing routes primarily focus on the shortest distances, often overlooking the practicality of these paths given student traffic. OptiWay introduces an innovative algorithm that not only considers distance but also accounts for congestion, ensuring more efficient and practical routing. The project stands out with its user-friendly, minimalistic interface, enhancing accessibility and ease of use. Our work not only offers technical insights into algorithmic route planning but also offers substantial practical benefits, potentially transforming day-to-day navigation in the busy SCIE campus.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/optiway_1.png" title="OptiWay image 1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The best path OptiWay gives to a (simulated) student between two particular periods.
</div>

### Project Description

Our software includes a few major parts: **map data source conversion**, **timetable generation**, **timetable validation**, **cross-language communication**, **visual representations**, **route time minimization**, and **map-timetable input-output**. The most attractive ones are our dedicated User-Interface-and-Map designs with intuitive 3D sense, and optimization algorithm making use of mathematical theories to swiftly deal with large amounts of calculations. Timetable validations also ensure the software to handle erroneous manipulation while cross-language communication maximizes the efficiency of the entire process, which also gives a chance for us to better divide our work based on the languages we are good at. 


### Technical Implementation

Taking timetable as input, OptiWay first finds out the shortest path for each student using **Floyd's algorithm**, and also evaluates the congestion in the shortest-path scenario. This leads to an overall performance index, which measures the overall time taken for an average student to change rooms between lessons, including the effect of congestion. Then, OptiWay uses multithreading to iteratively attempt to reduce the performance index (which indicates better performance), and hence computes a better plan with less congestion for all 2000 students in SCIE for each period in a single week. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/optiway_2.png" title="OptiWay image 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Congestion evaluation of OptiWay.
</div>

### Learning Experience

Developing OptiWay **exposed us to advanced concepts** such as multi-threading for enhanced performance, asynchronous operations for improved user experiences, and the necessity of integrating multiple languages – a realization we made when Python alone proved insufficient for algorithmic efficiency. The project also underscored **the distinct dynamics of frontend and backend development**, teaching us the importance of aesthetic design in user interface creation. This experience broadened our perspective of computer science from mere code-writing to encompassing vital aspects like UX (User Experience) design, app optimization, and demand identification. 

Moreover, OptiWay highlighted the power of **teamwork** in app development. By dividing responsibilities across algorithm design, backend, and frontend development, each team member could focus and excel in their area, allowing for efficient module development and seamless integration. This approach not only streamlined our workflow but also emphasized the significance of specialized roles in a collaborative project. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/optiway_3.png" title="OptiWay image 3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Optimization of performance index in OptiWay..
</div>

### Successes and Challenges

OptiWay boasts a **minimalistic, modern** UI (User Interface), with a **robust** app design that includes thorough testing of edge cases. It leverages **multi-threading** and **asynchronous operations** for optimization, and its visualization of congestion and paths is both straightforward and impressive. The app incorporates both a baseline and a customized route-finding algorithm, offering clear insights into the advancements of our approach. We maintain detailed [technical documentation](https://github.com/micfong-z/OptiWay/blob/main/TECHNICAL_NOTES.md) for further study and demonstrations. 

Challenges include the lack of access to actual SCIE student timetables, which affects real-world applicability. To mitigate this, we simulated timetable allocation patterns to generalize our algorithm. Initially, the app may seem complex, but this can be addressed through specialized training for teacher users, our primary audience. A key assumption in our congestion model is students follow the calculated paths; while this might not always reflect real-life scenarios, it is valid for demonstrating our algorithm and can be refined in the future by incorporating data outliers. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/optiway_4.png" title="OptiWay image 4" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overall congestion in SCIE between two particular periods if everyone follows the shortest path.
</div>

### Future Improvements and Recommendations

OptiWay’s model for addressing the problem of SCIE students’ daily transportation on campus is comprehensive and detailed. However, there are areas where the model can be improved. The model can be enhanced in three dimensions: software performance, algorithm design and UI/UX. To improve software performance and stability, we need to define our requirements in more detail to align with our goals and the problem we are trying to solve. This will allow us to test our prototypes more thoroughly with real-world scenarios. We can also consider using more advanced algorithms to improve the model’s accuracy and efficiency. We can also consider gathering feedback from users and stakeholders to identify areas for improvement. This feedback can be used to enhance the system further. 

For future research directions related to the project’s domain, we can explore the use of machine learning algorithms to optimize the model’s performance. We can also investigate the feasibility of integrating the model with other systems to provide a more comprehensive solution for students’ daily transportation needs.

### Conclusion

In conclusion, the project is well-developed and user-friendly. By testing in real scenes, we find it highly useful and significantly reduce the time we need to reach our next class, although the timetables are simulated ones. In future we hope we can cooperate with the school to utilize the program.
