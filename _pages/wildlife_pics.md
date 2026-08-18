---
layout: page
permalink: /wildlife/
title: Wildlife
description: Wildlife photography from national parks and reserves across India.
nav: true
nav_order: 6
photos:
  - 1.jpg
  - 2.jpg
  - 3.jpg
  - 4.jpg
  - 6.jpg
  - 7.jpg
  - 8.jpg
  - 10.jpg
  - 11a.jpg
  - 12.jpg
  - 13.jpg
  - 15.jpg
  - 16.jpg
  - Bhraminy Starling.jpg
  - Black Kite.jpg
  - Black Napped Monarch Flycatcher Sm.jpg
  - Blue Throated Barbet Sm.jpg
  - Cormorand with Kill Sm.jpg
  - Cormorand.jpg
  - Dear Sample.jpg
  - Elephant Sm.jpg
  - IMG_0077_02.jpg
  - IMG_0125_02.jpg
  - IMG_0342_03.jpg
  - IMG_0740_03.jpg
  - IMG_0827_03.jpg
  - IMG_1013_03.jpg
  - IMG_1297_03.jpg
  - IMG_1616_03.jpg
  - IMG_2073_03.jpg
  - IMG_2479_03.jpg
  - IMG_2562.jpg
  - IMG_3264_03.jpg
  - IMG_3972_03.jpg
  - IMG_7511_03.jpg
  - IMG_7620_03.jpg
  - IMG_7641_03.jpg
  - IMG_7771_03.jpg
  - IMG_7869_01.jpg
  - IMG_7993_01.jpg
  - IMG_8104_01.jpg
  - IMG_8209_01.jpg
  - IMG_8238_01.jpg
  - IMG_8498_01.jpg
  - IMG_8556_01.jpg
  - IMG_8711_01.jpg
  - IMG_8758_01.jpg
  - IMG_9005_01.jpg
  - IMG_9026_01.jpg
  - IMG_9094_01.jpg
  - IMG_9247_01.jpg
  - IMG_9335_01.jpg
  - IMG_9470_01.jpg
  - IMG_9501_01.jpg
  - IMG_9741_01.jpg
  - IMG_9987_01.jpg
  - IMG_9988_01.jpg
  - Koel Sm.jpg
  - Leppy Bandipur Apr sm.jpg
  - Monitor Lizard.jpg
  - Owl.jpg
  - Peacock Sm.jpg
  - pied Bushchat-2.jpg
  - Rufous Treepie 1 Sm.jpg
  - Ser  Juv Sz 1.jpg
  - Serpant Eagle.jpg
  - Slot Bear.jpg
  - Sparrow Sm.jpg
  - Swallow.jpg
  - Swift2.jpg
  - Tiger Bandipur Apr.jpg
  - Tiger Jiju1.jpg
  - Tiger Price Sm.jpg
  - Tiger Rolling.jpg
  - White Bellied Eagle Owl Sm full.jpg
  - White Bellied Eagle Owl Sm.jpg
  - White Browed Bulbull.jpg
  - wood-pecker.jpg
---

I am a wildlife photographer and conservationist. A selection of my favorite shots — click any image to view it full size:

<style>
  .wildlife-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 10px;
  }
  .wildlife-thumb-wrap {
    aspect-ratio: 1 / 1;
    overflow: hidden;
    border-radius: 6px;
  }
  .wildlife-thumb {
    width: 100%;
    height: 100%;
    object-fit: cover;
    cursor: zoom-in;
    display: block;
  }
  /* medium-zoom clones this <img> for the zoomed view (cloneTarget() in
     its source) and pins the clone's box, via inline style, to the
     original thumbnail's on-page pixel size (e.g. 220x220 here) — its
     scale-to-fit-viewport transform is computed specifically against
     that box size. Leave width/height alone (forcing them to "auto"
     lets the box balloon to the image's full natural size *after* the
     scale factor was already computed for the small box, making the
     zoomed image render enormously oversized). object-fit: contain is
     enough on its own: the image letterboxes to show its full,
     uncropped, undistorted content within that correctly-sized box. */
  .wildlife-thumb.medium-zoom-image--opened {
    object-fit: contain !important;
  }
</style>

<div class="wildlife-grid">
{% for photo in page.photos %}
  <div class="wildlife-thumb-wrap">
    <img
      class="wildlife-thumb"
      src="{{ '/assets/wildlife_clicks/' | append: photo | relative_url }}"
      alt="Wildlife photograph"
      loading="lazy"
      data-zoomable>
  </div>
{% endfor %}
</div>
