---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ site.title }}</title>
</head>
<body>
  <header>
    <h1>Welcome to {{ site.title }}</h1>
    <p>{{ site.description }}</p>
  </header>

  <section>
    <h2>Posts from Content Collection</h2>

    <ul>
      {% for post in site.content %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  </section>
</body>
</html>
