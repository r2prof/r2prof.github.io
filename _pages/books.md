---
title: "Books"
permalink: /books/
layout: single
author_profile: true
---

Books I've read, with a rating and occasionally a note. Nothing systematic — just what stuck with me.

<div class="books-list">
{% assign books = site.data.books | sort: "date_read" | reverse %}
{% for book in books %}
  <div class="book-entry" style="margin-bottom: 1.75em; padding-bottom: 1.5em; border-bottom: 1px solid #eee;">
    <h3 style="margin-bottom: 0.2em;">{{ book.title }}</h3>
    <p style="margin: 0 0 0.3em 0; color: #666;">{{ book.author }}{% if book.date_read %} · {{ book.date_read }}{% endif %}</p>
    <p style="font-size: 1.2em; letter-spacing: 2px; margin: 0.3em 0;">
      {% for i in (1..5) %}{% if i <= book.rating %}★{% else %}☆{% endif %}{% endfor %}
    </p>
    {% if book.notes %}<p style="margin-top: 0.3em;">{{ book.notes }}</p>{% endif %}
  </div>
{% endfor %}
</div>
