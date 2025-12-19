---
# Variables for page.*
layout: default

title: Home
description: Main page with contents
---

<section class="intro">
    <div class="intro-box">
        <h2>Hi... </h2>
        <p>My Name is... </p>
    </div>
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
