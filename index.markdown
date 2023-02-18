---
layout: splash
permalink: /
hidden: true
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/unsplash1.jpg
  caption: Photo by <a href="https://unsplash.com/@sincerelymedia?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Sincerely Media</a> on <a href="https://unsplash.com/wallpapers/colors/green?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

  actions:
    - label: "<i class='fas fa-book-reader'></i> All posts"
      url: "/posts/"
excerpt: >
  Tools, tips, and tricks to take the "Motherboarder!" out of your coding. <br />
#   <small><a href="https://github.com/mmistakes/minimal-mistakes/releases/tag/4.24.0">Latest release v4.24.0</a></small>
# feature_row:
#   - image_path: /assets/unsplash-image-6.jpg
#     alt: "customizable"
#     title: "Super customizable"
#     excerpt: "Everything from the menus, sidebars, comments, and more can be configured or set with YAML Front Matter."
#     url: "/docs/configuration/"
#     btn_class: "btn--primary"
#     btn_label: "Learn more"
#   - image_path: /assets/unsplash-image-6.jpg
#     alt: "fully responsive"
#     title: "Responsive layouts"
#     excerpt: "Built with HTML5 + CSS3. All layouts are fully responsive with helpers to augment your content."
#     url: "/docs/layouts/"
#     btn_class: "btn--primary"
#     btn_label: "Learn more"
#   - image_path: /assets/unsplash-image-6.jpg
#     alt: "100% free"
#     title: "100% free"
#     excerpt: "Free to use however you want under the MIT License. Clone it, fork it, customize it... whatever!"
#     url: "/docs/license/"
#     btn_class: "btn--primary"
#     btn_label: "Learn more"
---

<!-- {% include feature_row %} -->

<div class="grid__wrapper">
  {% for post in site.posts limit:4 %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
