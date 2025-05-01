---
layout: default
title: "Move 37 Podcast - All Episodes"
description: "Podcast on how Generative AI is transforming the future. Interviews with startup founders, philosophers, and computer scientists"
---

<main>
<section id="popular-episodes" class="py-16 px-4 bg-white">
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-3xl font-bold text-gray-800 mb-10">All Episodes</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
{% for episode in site.data.episodes %}
  <div class="border rounded-lg shadow hover:shadow-lg transition overflow-hidden relative">
    <!-- Episode Number Badge -->
    <div class="absolute top-2 left-2 bg-gray-800 bg-opacity-75 text-white rounded-full text-xs px-2 py-1">
      #{{ episode.episode }}
    </div>
    <!-- Thumbnail -->
    <a href="/episodes/{{ episode.id }}" class="block aspect-video bg-gray-100">
      <img class="w-full h-full object-cover" 
           src="https://img.youtube.com/vi/{{ episode.youtube_id }}/hqdefault.jpg" 
           alt="{{ episode.title }}">
    </a>
    <!-- Episode Details -->
    <div class="p-4 text-left">
      <h3 class="text-xl font-semibold text-orange-500 mb-2">{{ episode.title }}</h3>
      <p class="text-gray-600 text-sm mb-4">Featuring {{ episode.guest_name }}, {{ episode.guest_affiliation }}</p>
      <a href="/episodes/{{ episode.id }}" class="text-orange-500 font-semibold hover:text-orange-600">
        View Episode &rarr;
      </a>
    </div>
  </div>
{% endfor %}
    </div>
  </div>
</section>
</main>
