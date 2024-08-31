---
title: Home
layout: home
tags: page
modified: 2022-01-09 00:00:00
order: 1
---
<div class="">
  <div class=""><img class="rounded-2xl border border-gray-400 border-2 mb-12" src="/images/rooseveltcover.jpg"></div>
  <h1 class="title mb-12 text-center sm:text-left">
    Welcome to my site!
  </h1>
  <div class="text-xl md:text-2xl">
    <p class="mb-8">
      I'm Luke Andersen, a <span class="highlight">Programmer</span>, <span class="highlight">Game Designer</span>, and <span class="highlight">Narrative Designer</span> with a passion for creating narrative through gameplay mechanics. Though I specialize as a gameplay programmer, I have a generalist knowledge of game development and have experience working on projects with large codebases and collaborating with other disciplines. 
    </p>
    Want to get in touch? Reach me at <a href = "mailto:luke.william.andersen@gmail.com" class = "highlight underline hover:text-red-800"> luke.william.andersen@gmail.com </a>!
  </div>

  <h1 class="title text-center sm:text-left">Featured Project</h1>
  {% for project in projects %}
  {% if project.featured %}
  <a href="/projects/{{project.title | slugify}}">
    <div class="p-4 hover:bg-stone-100 rounded-xl">
      <div class="bg-slate-50 rounded-2xl border border-gray-400 border-2 grid grid-cols-1 grid-rows-2 md:grid-rows-1 md:grid-cols-2 overflow-hidden">
        <div class="bg-no-repeat bg-center bg-cover" style="background-image: url('/images/{{project.image}}');">
        </div>
        <div class="bg-amber-400">
          <div class="m-3 md:m-8 testspace">
            <h2 class="text-4xl font-bold text-slate-800 text-center">{{project.title}}</h2>
            <p class="highlight font-bold text-center text-2xl md:mb-8">{{project.role}}</p>
            <p class="text-slate-800">{{project.summary}}</p>
          </div>
        </div>
      </div>
    </div>
  </a>
  {% endif %}
  {% endfor %}
</div>
