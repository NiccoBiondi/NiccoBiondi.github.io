---
layout: page
permalink: /publications/
title: publications
description: publications in reversed chronological order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->
{% include bib_search.liquid %}

<!-- Year filter buttons -->
<div id="year-filter" style="margin-bottom: 1.5rem; display: flex; flex-wrap: wrap; gap: 0.4rem; align-items: center;">
  <span style="font-size: 0.85rem; color: var(--global-text-color-light); margin-right: 0.3rem;">Filter:</span>
</div>

<div class="publications">

{% bibliography %}

</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
  var container = document.getElementById('year-filter');
  var h2s = Array.from(document.querySelectorAll('.publications h2.bibliography'));

  // Build "All" button
  var allBtn = document.createElement('button');
  allBtn.textContent = 'All';
  allBtn.className = 'year-filter-btn active';
  allBtn.setAttribute('data-year', 'all');
  container.appendChild(allBtn);

  // Build one button per year
  h2s.forEach(function (h2) {
    var btn = document.createElement('button');
    btn.textContent = h2.textContent.trim();
    btn.className = 'year-filter-btn';
    btn.setAttribute('data-year', h2.textContent.trim());
    container.appendChild(btn);
  });

  function applyFilter(year) {
    h2s.forEach(function (h2) {
      var ol = h2.nextElementSibling;
      var visible = (year === 'all' || h2.textContent.trim() === year);
      h2.style.display = visible ? '' : 'none';
      if (ol) ol.style.display = visible ? '' : 'none';
    });
    container.querySelectorAll('.year-filter-btn').forEach(function (b) {
      b.classList.toggle('active', b.getAttribute('data-year') === year);
    });
  }

  container.addEventListener('click', function (e) {
    if (e.target.classList.contains('year-filter-btn')) {
      applyFilter(e.target.getAttribute('data-year'));
    }
  });
});
</script>

<style>
.year-filter-btn {
  padding: 0.25rem 0.75rem;
  border: 1px solid var(--global-theme-color);
  border-radius: 999px;
  background: transparent;
  color: var(--global-theme-color);
  font-size: 0.82rem;
  cursor: pointer;
  transition: background 0.15s, color 0.15s;
}
.year-filter-btn:hover,
.year-filter-btn.active {
  background: var(--global-theme-color);
  color: #fff;
}
</style>
