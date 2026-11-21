---
layout: page
permalink: /photos/
title: photos
description: Outside of work.
nav: true
nav_order: 7

# Gallery images live in assets/img/photos/ (resized to <=1080px, metadata stripped).
# Each gallery is shown three photos per row, in this order. Click a photo to enlarge it.
galleries:
  - title: black & white
    photos:
      - file: fittonia.jpg
        alt: Fittonia leaves with bright white veins
      - file: glass-dome.jpg
        alt: Looking up through a geodesic glass dome beside a concrete wall
      - file: jellyfish.jpg
        alt: Spotted jellyfish against a black background
      - file: espresso.jpg
        alt: Espresso machine on a kitchen counter
      - file: ramp.jpg
        alt: Concrete ramp and railing under a cloudy sky
      - file: pine-road.jpg
        alt: Sandy road through a pine forest
      - file: park-bench.jpg
        alt: Bench under the trees in a park
      - file: geodesic.jpg
        alt: Triangular panels of a geodesic sphere
      - file: coffee.jpg
        alt: Pour-over coffee, a mug, and a scone on a café table
  - title: coast & sky
    photos:
      - file: beach-sunset.jpg
        alt: Sunset over the ocean with two people sitting on the beach
      - file: boardwalk.jpg
        alt: Wooden boardwalk leading over the dunes to the beach at dawn
      - file: dune-sunset.jpg
        alt: Pink and orange sunset over dune grass
      - file: pier-sunset.jpg
        alt: Orange sunset over the water with a covered pier
      - file: evening-sky.jpg
        alt: Purple and pink clouds above silhouetted trees
      - file: dusk.jpg
        alt: Deep blue dusk sky with a band of orange at the horizon
---

<div class="row align-items-center">
  <div class="col-sm-5 mt-3 mt-md-0">
    {% include figure.html path="assets/img/IMG_1234.jpeg" class="img-fluid rounded z-depth-1" alt="Brian Larkins by the water at sunset" zoomable=true %}
  </div>
  <div class="col-sm-7 mt-3 mt-md-0" markdown="1">

When I'm not teaching or wrangling supercomputers, I'm usually behind a camera,
tending my reef tank, cooking, or making coffee.

Here are a few of my favorite photographs.

  </div>
</div>

{% for gallery in page.galleries %}
<h2 class="mt-5">{{ gallery.title }}</h2>
<div class="row">
{% for photo in gallery.photos %}
  {% capture photo_path %}assets/img/photos/{{ photo.file }}{% endcapture %}
  <div class="col-4 mt-3">
    {% include figure.html path=photo_path class="img-fluid rounded z-depth-1" alt=photo.alt zoomable=true %}
  </div>
{% endfor %}
</div>
{% endfor %}
