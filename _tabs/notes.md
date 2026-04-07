---
icon: fas fa-stream
order: 2
title: Notes
---

{% assign notes = site.notes | sort: 'date' | reverse %}

<div class="post-content">
  <ul class="content ps-0">
    {% for note in notes %}
      <li class="d-flex justify-content-between px-md-3">
        <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
        <span class="dash flex-grow-1"></span>
        <span>{{ note.date | date: "%Y-%m-%d" }}</span>
      </li>
    {% endfor %}
  </ul>
</div>
