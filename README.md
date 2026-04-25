

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
  }

  .gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 1px; /* optional */
}

.gallery img {
  flex: 0 1 auto;   /* grow and shrink proportionally */
  height: auto;     /* preserve aspect ratio */
  max-height: 300px; /* optional: limit height */
  width: auto;      /* adjust width automatically */
  display: block;
}
  
</style>
</head>
<body>

<b>China, September 2025</b><br>
<div class="gallery">  
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-china/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>
  
<br><b>Amsterdam, September 2025</b><br>
<div class="gallery">  
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-amsterdam/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Giethoorn and Zaan, September 2025</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-giethoorn-zaan/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Brussels, September 2025</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-brussels/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Barcelona, September 2025</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-barca/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>New York, August 2025</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-nyc/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Hoboken, July 2025</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-7-hoboken/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Chicago, October 2019</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-10-chicago/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Italy, September 2019</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-9-italy/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Yunnan, August 2019</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-8-yunnan/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Peru and Bolivia, March 2019</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-3-peru/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

<br><b>Yunnan, August 2012</b><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2012-8-yunnan/images/'" %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}">
  {% endfor %}
</div>

</body>
</html>
