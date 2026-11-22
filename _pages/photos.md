---
layout: page
permalink: /photos/
title: photos
description: Outside of work.
nav: true
nav_order: 7

# Gallery images live in assets/img/photos/ (resized to <=1080px, metadata stripped).
# Click a photo to enlarge it. A gallery is either:
#   photos: a flat list, shown three per row as equal-size (square) tiles; or
#   rows:   explicit rows for mixed aspect ratios. Give each photo its width/height
#           ratio (1.5 = 3:2, 0.6667 = 2:3, 1.3333 = 4:3, 0.75 = 3:4, 1 = square);
#           photos in a row are scaled to the same height and fill the full width.
galleries:
  - title: united kingdom
    rows:
      - photos:
          - file: harlaxton-manor.jpg
            ratio: 1.5
            alt: The front of Harlaxton Manor under a deep blue sky
          - file: harlaxton-lavender.jpg
            ratio: 0.6667
            alt: Lavender in the foreground with a domed building beyond at dusk
          - file: harlaxton-evening.jpg
            ratio: 1.5
            alt: Harlaxton Manor and its gardens in evening light
      - photos:
          - file: cambridge-thistles.jpg
            ratio: 1.5
            alt: Blue globe thistles and yellow flowers in front of a stone building in Cambridge
          - file: cambridge-street.jpg
            ratio: 1.5
            alt: Black-and-white Cambridge street with a cyclist and a college chapel tower
          - file: edinburgh-castle.jpg
            ratio: 1.5
            alt: Edinburgh Castle on its rock behind tall golden grass
      - photos:
          - file: london-eye.jpg
            ratio: 1.3333
            alt: Looking up at the spokes and capsules of the London Eye
          - file: thames-from-eye.jpg
            ratio: 1.3333
            alt: The Thames and the Houses of Parliament seen from a London Eye capsule
          - file: estate-sunset.jpg
            ratio: 1.3333
            alt: Fiery sunset over ornate stone gates and a long tree-lined drive
  - title: japan
    rows:
      - photos:
          - file: kinkakuji.jpg
            ratio: 1.3333
            alt: Kinkaku-ji, the Golden Pavilion, above its pond in Kyoto
          - file: pagoda.jpg
            ratio: 0.6667
            alt: Five-story wooden pagoda against a pale blue sky
          - file: miyajima-torii.jpg
            ratio: 1.5
            alt: The red torii at Miyajima at low tide, with visitors and umbrellas on the wet sand
      - photos:
          - file: round-windows.jpg
            ratio: 1.3333
            alt: Two round windows framing green maple trees
          - file: ginkakuji.jpg
            ratio: 1.5
            alt: Ginkaku-ji, the Silver Pavilion, across a garden pond
          - file: temple-roof.jpg
            ratio: 1
            alt: Sweeping tiled temple roof under a blue sky with clouds
      - photos:
          - file: lanterns.jpg
            ratio: 1.5
            alt: Rows of glowing paper lanterns at a shrine at night
          - file: sushi-bar.jpg
            ratio: 1
            alt: Chefs at work behind a busy sushi counter
          - file: udon.jpg
            ratio: 0.75
            alt: Bowl of udon topped with an egg yolk, bonito flakes, tempura bits, and scallions
      - photos:
          - file: torii-steps.jpg
            ratio: 0.6667
            alt: Black-and-white stone torii at the foot of a staircase through the woods
          - file: shrine-lanterns.jpg
            ratio: 1.5
            alt: Black-and-white shrine with rows of paper lanterns and a stone guardian
          - file: miyajima-walkway.jpg
            ratio: 1.5
            alt: Black-and-white shrine walkway looking out to the distant torii across wet tidal flats
          - file: pagoda-eaves.jpg
            ratio: 0.6667
            alt: Black-and-white view looking up at the layered eaves of a pagoda
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
{% if gallery.rows %}
{% for row in gallery.rows %}
<div class="photo-row mt-3">
{% for photo in row.photos %}
  {% capture photo_path %}assets/img/photos/{{ photo.file }}{% endcapture %}
  <div style="flex: {{ photo.ratio | default: 1 }} 1 0%;">
    {% include figure.html path=photo_path class="img-fluid rounded z-depth-1" alt=photo.alt zoomable=true %}
  </div>
{% endfor %}
</div>
{% endfor %}
{% else %}
<div class="row">
{% for photo in gallery.photos %}
  {% capture photo_path %}assets/img/photos/{{ photo.file }}{% endcapture %}
  <div class="col-4 mt-3">
    {% include figure.html path=photo_path class="img-fluid rounded z-depth-1" alt=photo.alt zoomable=true %}
  </div>
{% endfor %}
</div>
{% endif %}
{% endfor %}
