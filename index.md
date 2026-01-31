---
# Variables for page.*
layout: default

title: Personal Portfolio
description: Main page with contents
---

<section class="main-content">
    <h2> Hi there, this is Adrian, a Physics Engineer with a deep love for Computer Science.</h2>
    <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
    <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
</section>



<section class="projects-overview">
    <h2>My Personal Projects</h2>
    <div class="projects-grid">
        {% for project in site.projects %}
            <a href="{{ project.url }}" class="project-card">
                <img src="{{ project.image }}">
                <span>{{ project.title }}</span>
            </a>
        {% endfor %}
    </div>
</section>

<section class="section-about">
    <div class="page-padding">
        <div id="about" class="container">
            <div class="about-grid">
                <div class="about-image"></div>
                <div>
                    <h2 class="text-large">Who am I?</h2>
                    <p class="text-default">
                        I'm a Physics Engineer...
                    </p>
                    <p class="text-default">
                        I'm currently...
                    </p>
                    <div class="about-links">
                        {% for item in site.data.accounts %}
                            <a class="about-link" href={{ item.href }} target="_blank">
                                <div class="about-link-icon"><svg fill="none"></svg></div>
                                <div>{{ item.text }}</div>
                            </a>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="experience">
    <h2>Experience & Education</h2>
    <table>
        <tr>
            <th>Role / Education</th>
            <th>Place / Institution</th>
            <th>Year</th>
        </tr>
        {% for item in site.data.experience %}
            <tr>
                <td>{{ item.role }}</td>
                <td>{{ item.place }}</td>
                <td>{{ item.year }}</td>
            </tr>
        {% endfor %}
    </table>
</section>
