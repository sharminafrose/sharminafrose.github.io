---
layout: page
permalink: /papers/
title: Papers
description: Journal articles, conference and workshop papers, book chapters, and thesis, grouped by type in reverse chronological order.
nav: false
---

<!-- _pages/papers.md -->
<!-- Sections are selected by BibTeX entry type (and abbr for articles), so new entries land in the right group automatically. -->

{% include bib_search.liquid %}

<p class="pub-jump">
  <a href="#journal-articles">Journal Articles ({% bibliography_count -f papers -q @article[abbr=Journal] %})</a> ·
  <a href="#conference-papers">Conference and Workshop Papers ({% bibliography_count -f papers -q @inproceedings %})</a> ·
  <a href="#book-chapters">Book Chapters ({% bibliography_count -f papers -q @incollection %})</a> ·
  <a href="#theses">Thesis ({% bibliography_count -f papers -q @phdthesis %})</a>
</p>

<div class="publications">

<h2 class="pub-section" id="journal-articles">Journal Articles</h2>
{% bibliography -f papers -q @article[abbr=Journal] %}

<h2 class="pub-section" id="conference-papers">Conference and Workshop Papers</h2>
{% bibliography -f papers -q @inproceedings %}

<h2 class="pub-section" id="book-chapters">Book Chapters</h2>
{% bibliography -f papers -q @incollection %}

<h2 class="pub-section" id="theses">Thesis</h2>
{% bibliography -f papers -q @phdthesis %}

</div>

<script>
  // The bib search box treats the URL #fragment as a filter term, so plain
  // #section links would filter out every paper. Scroll without touching the hash.
  document.querySelectorAll(".pub-jump a").forEach(function (link) {
    link.addEventListener("click", function (event) {
      var target = document.getElementById(link.getAttribute("href").slice(1));
      if (!target) return;
      event.preventDefault();
      target.scrollIntoView({ block: "start" });
    });
  });
</script>
