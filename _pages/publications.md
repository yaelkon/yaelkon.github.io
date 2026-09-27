---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---

<style>
  /* Bold Publications title */
  .post-title {
    font-weight: bold;
    margin-bottom: 0.5rem;
  }

  /* Year in left column, paper in right column */
  .publications {
    display: grid;
    grid-template-columns: 3.5rem 1fr;
    column-gap: 2rem;
    align-items: start;
  }
  .publications > h2 {
    grid-column: 1;
    text-align: right;
    font-size: 1rem;
    font-weight: bold;
    margin: 0;
    padding-top: 0.2rem;
    align-self: start;
  }
  .publications > ol.bibliography {
    grid-column: 2;
    padding-left: 0;
    list-style: none;
    margin: 0;
  }
  .publications > ol.bibliography li {
    margin-bottom: 1.5rem;
  }
</style>

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
