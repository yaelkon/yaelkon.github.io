---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 3
---

<style>
  /* Hide page title on CV page */
  .post-title { display: none; }

  .cv-wrapper {
    position: relative;
  }
  .cv-download-btn {
    position: absolute;
    top: 0;
    right: 0;
    z-index: 10;
    display: inline-block;
    padding: 0.4rem 0.8rem;
    border: 1.5px solid currentColor;
    font-size: 0.85rem;
    text-decoration: none;
    cursor: pointer;
  }
  .cv-download-btn:hover {
    background-color: rgba(0,0,0,0.06);
    text-decoration: none;
  }
</style>

<div class="cv-wrapper">
  <a href="/assets/pdf/cv.pdf" download class="cv-download-btn" role="button">Download CV</a>
  <div style="width: 100%; height: 90vh; padding-top: 2.5rem;">
    <iframe
      src="https://docs.google.com/viewer?url=https://yaelkon.github.io/assets/pdf/cv.pdf&embedded=true"
      width="100%"
      height="100%"
      style="border: none;"
    ></iframe>
  </div>
</div>
