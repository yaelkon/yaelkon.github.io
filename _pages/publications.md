---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---

<style>
  /* Reduce gap between page title and filter bar */
  .post-title {
    margin-bottom: 0.5rem;
  }

  /* Year as heading above each group */
  .publications > h2 {
    font-size: 1rem;
    font-weight: bold;
    margin-top: 1.5rem;
    margin-bottom: 0.5rem;
  }
  .publications > ol.bibliography {
    padding-left: 0;
    list-style: none;
  }
  .publications > ol.bibliography li {
    margin-bottom: 1rem;
  }
</style>

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
