---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Jauhal.org</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@2/css/pico.min.css">
  <style>
    /* Custom tweaks */
    header { padding-top: 2rem; padding-bottom: 2rem; }
    article { margin-bottom: 2rem; }
  </style>
</head>
<body>
  <main class="container">
    <header>
      <hgroup>
        <h1>Jauhal.org</h1>
        <p>Welcome to my automated blog</p>
      </hgroup>
      <hr>
    </header>

    <section>
      {% for post in site.posts %}
        <article>
          <header>
            <p><strong><a href="{{ post.url }}">{{ post.title }}</a></strong></p>
          </header>
          <!-- Display the excerpt (first paragraph) of the post -->
          <p>
            {{ post.excerpt | strip_html | truncatewords: 40 }}
          </p>
          <footer>
             <small>{{ post.date | date_to_string }}</small>
             {% if post.categories %}
               • <small>Tags: {{ post.categories | join: ', ' }}</small>
             {% endif %}
          </footer>
        </article>
      {% endfor %}
    </section>
    
    <footer>
      <hr>
      <p>
        <small>Connect with me on X: <a href="https://x.com/JauhalPeter" target="_blank">@JauhalPeter</a></small><br>
        <small>Powered by n8n & GitHub Pages</small>
      </p>
    </footer>
  </main>
</body>
</html>
