---
layout: default
title: Главная
---

<div class="min-h-screen rounded-3xl border border-white/5 bg-slate-950/70 p-6 shadow-2xl shadow-slate-950/40 backdrop-blur-sm">
  <!-- Hero Section -->
  <section class="relative overflow-hidden rounded-3xl bg-gradient-to-br from-cyan-700/10 via-slate-900/60 to-slate-950/90 px-6 py-16 text-center shadow-xl shadow-cyan-500/10">
    <div class="absolute inset-0 bg-[radial-gradient(circle_at_top,_rgba(56,189,248,0.22),_transparent_35%)]"></div>
    <div class="relative z-10">

      <h1 class="text-4xl md:text-6xl font-extrabold tracking-tight text-white mb-4">Привет, я Nskdima</h1>
      <p class="mx-auto max-w-2xl text-lg text-slate-300 sm:text-xl">Разработчик, администратор и энтузиаст компьютерного железа. Добро пожаловать на мой сайт-портфолио.</p>
      <div class="mt-10 flex flex-col items-center gap-4 sm:flex-row sm:justify-center">
        <a href="/about" class="inline-flex items-center justify-center rounded-full bg-cyan-500 px-8 py-3 text-sm font-semibold uppercase tracking-wide text-slate-950 transition hover:bg-cyan-400">
          Узнать обо мне
        </a>
        <a href="#projects" class="inline-flex items-center justify-center rounded-full border border-cyan-500/30 bg-white/5 px-8 py-3 text-sm font-semibold text-cyan-200 transition hover:border-cyan-300/60 hover:bg-white/10">
          Мои проекты
        </a>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="mt-16 px-2 py-4">
    <div class="flex flex-col gap-4 md:flex-row md:items-end md:justify-between">
      <div>
        <h2 class="text-3xl md:text-4xl font-bold text-white">Мои Проекты</h2>
        <p class="mt-2 max-w-xl text-sm text-slate-400">Проекты, над которыми я работал, демонстрируют мои навыки в веб-разработке, администрировании и дизайне.</p>
      </div>
    </div>

    <div class="mt-10 grid gap-8 md:grid-cols-2 lg:grid-cols-3">
      {% for project in site.data.projects %}
      <div class="group rounded-3xl border border-white/10 bg-slate-900/90 p-6 shadow-2xl shadow-slate-950/40 transition duration-300 hover:-translate-y-1 hover:border-cyan-500/40 hover:bg-slate-900">
        <div class="mb-4 flex items-center justify-between">
          <span class="inline-flex rounded-full bg-cyan-500/10 px-3 py-1 text-sm font-medium text-cyan-200">Проект</span>
          <span class="text-xs uppercase tracking-[0.2em] text-slate-500">#{{ forloop.index }}</span>
        </div>
        <h3 class="text-2xl font-semibold text-white mb-3">{{ project.title }}</h3>
        <p class="text-slate-300 mb-5 leading-relaxed">{{ project.description }}</p>
        <div class="mb-5 flex flex-wrap gap-2">
          {% for tech in project.technologies %}
          <span class="rounded-full border border-slate-700/80 bg-slate-950/70 px-3 py-1 text-xs font-medium text-slate-200">{{ tech }}</span>
          {% endfor %}
        </div>
        <div class="flex flex-wrap gap-3">
          <a href="{{ project.github }}" target="_blank" class="inline-flex items-center justify-center rounded-full bg-cyan-500 px-5 py-3 text-sm font-semibold uppercase tracking-[0.15em] text-slate-950 transition hover:bg-cyan-400">
            GitHub
          </a>
          {% if project.demo %}
          <a href="{{ project.demo }}" target="_blank" class="inline-flex items-center justify-center rounded-full border border-cyan-500/30 bg-white/5 px-5 py-3 text-sm font-semibold uppercase tracking-[0.15em] text-cyan-200 transition hover:border-cyan-300/60 hover:bg-white/10">
            Live Demo
          </a>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- About Link -->
  <section class="mt-16 text-center">
    <a href="/about" class="inline-flex items-center justify-center rounded-full border border-cyan-500/30 bg-white/5 px-8 py-4 text-sm font-semibold uppercase tracking-[0.15em] text-cyan-200 transition hover:border-cyan-300/60 hover:bg-white/10">
      Узнать больше обо мне
    </a>
  </section>
</div>