<h2 id="publications">Selected Publications</h2>

<p class="pub-intro"><sup>&dagger;</sup> denotes my advisor. For the full list, please refer to my <a href="{{ site.google_scholar }}"><i class="ai ai-google-scholar-square"></i> Google Scholar page</a>.</p>

{% assign v = site.time | date: "%s" %}
<div class="pubs">
{% for link in site.data.publications.main %}
<div class="pub">
  <div class="pub-media">
    {% if link.video %}
    <video src="{{ link.video }}?v={{ v }}" poster="{{ link.poster }}?v={{ v }}" autoplay muted loop playsinline preload="metadata"></video>
    {% elsif link.image %}
    <a href="{{ link.image }}?v={{ v }}" target="_blank"><img src="{{ link.image }}?v={{ v }}" class="fig" alt="{{ link.nickname | default: link.title }}" loading="lazy"></a>
    {% endif %}
    {% if link.conference_short %}<span class="venue-badge">{{ link.conference_short }}</span>{% endif %}
  </div>
  <div class="pub-body">
    <div class="pub-title"><a href="{{ link.page | default: link.pdf }}">{{ link.title }}</a></div>
    <div class="pub-venue">{{ link.conference }}{% if link.nickname %} <span class="nickname">({{ link.nickname }})</span>{% endif %}</div>
    <div class="pub-authors">{{ link.authors }}</div>
    <div class="pub-links">
      {% if link.pdf %}<a href="{{ link.pdf }}" class="btn" target="_blank">Paper</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}" class="btn" target="_blank">Project Page</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}" class="btn" target="_blank">Code</a>{% endif %}
      {% if link.demo %}<a href="{{ link.demo }}" class="btn" target="_blank">Demo</a>{% endif %}
      {% if link.comfyui %}<a href="{{ link.comfyui }}" class="btn" target="_blank">ComfyUI</a>{% endif %}
      {% if link.hf %}<a href="{{ link.hf }}" class="btn" target="_blank">🤗 Model</a>{% endif %}
      {% if link.dataset %}<a href="{{ link.dataset }}" class="btn" target="_blank">🤗 Dataset</a>{% endif %}
      {% if link.leaderboard %}<a href="{{ link.leaderboard }}" class="btn" target="_blank">Leaderboard</a>{% endif %}
      {% if link.stars %}<a href="https://github.com/{{ link.stars }}" class="star-badge" target="_blank"><img src="https://img.shields.io/github/stars/{{ link.stars }}?style=social" alt="GitHub stars"></a>{% endif %}
    </div>
    {% if link.notes %}<div class="pub-note">{{ link.notes }}</div>{% endif %}
    {% if link.extra %}<div class="pub-extra">{{ link.extra }}</div>{% endif %}
  </div>
</div>
{% endfor %}
</div>
