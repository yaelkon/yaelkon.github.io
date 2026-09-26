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

  /* Year aligned with paper title — two-column grid */
  .publications {
    display: grid;
    grid-template-columns: 3.5rem 1fr;
    column-gap: 2rem;
    row-gap: 1.5rem;
    align-items: start;
  }
  .publications > h2 {
    grid-column: 1;
    text-align: right;
    font-size: 1rem;
    font-weight: bold;
    margin: 0;
    padding: 0;
    align-self: start;
  }
  .publications > ol.bibliography {
    grid-column: 2;
    margin: 0;
    padding-left: 0;
    list-style: none;
  }
  .publications > ol.bibliography li {
    margin-bottom: 0;
  }
</style>

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
