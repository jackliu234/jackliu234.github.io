<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Photo Gallery</title>
<style>
  html, body {
    margin: 0;
    padding: 20px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    background: #f5f5f5;
  }

  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 30px;
  }

  .gallery-section {
    background: white;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 30px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .gallery-section h2 {
    margin-top: 0;
    color: #444;
    font-size: 1.2em;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
  }

  .gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .gallery img {
    flex: 0 1 calc(25% - 6px); /* 4 images per row */
    height: 200px;
    object-fit: cover;
    border-radius: 4px;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
  }

  .gallery img:hover {
    transform: scale(1.03);
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  }

  /* Lightbox */
  .lightbox {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.9);
    z-index: 1000;
    justify-content: center;
    align-items: center;
  }

  .lightbox.active {
    display: flex;
  }

  .lightbox img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 4px;
  }

  .lightbox-close {
    position: absolute;
    top: 20px;
    right: 30px;
    color: white;
    font-size: 40px;
    cursor: pointer;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .gallery img {
      flex: 0 1 calc(50% - 4px); /* 2 images per row on mobile */
      height: 150px;
    }
  }
</style>
</head>
<body>

<!-- Galleries sorted newest to oldest -->

<br><b>China, September 2025 TEST</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery">  
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-china/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>
  
<br><b>Amsterdam, September 2025</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery">  
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-amsterdam/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Giethoorn and Zaan, September 2025</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-giethoorn-zaan/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Brussels, September 2025</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-brussels/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Barcelona, September 2025</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-9-barca/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>New York, August 2025</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-8-nyc/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Hoboken, July 2025</b>
<br><i>Fujifilm X100VI</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2025-7-hoboken/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Chicago, October 2019</b>
<br><i>Nikon F100</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-10-chicago/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Italy, September 2019</b>
<br><i>Nikon D5600</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-9-italy/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Yunnan, August 2019</b>
<br><i>Nikon D5600</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-8-yunnan/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Peru and Bolivia, March 2019</b>
<br><i>Nikon D5600</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2019-3-peru/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<br><b>Yunnan, August 2012</b>
<br><i>Canon 900Ti</i><br>
<div class="gallery"> 
  {% assign images = site.static_files | where_exp:"file","file.path contains '/2012-8-yunnan/images/'" | sort: "path" | reverse %}
  {% for img in images %}
    <img src="{{ img.path | relative_url }}" alt="{{ img.name }}" loading="lazy" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

<!-- Lightbox -->
<div class="lightbox" id="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="Full size">
</div>

<script>
function openLightbox(src) {
  document.getElementById('lightbox-img').src = src;
  document.getElementById('lightbox').classList.add('active');
}

function closeLightbox() {
  document.getElementById('lightbox').classList.remove('active');
}

// Close on Escape key
document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') closeLightbox();
});
</script>

</body>
</html>