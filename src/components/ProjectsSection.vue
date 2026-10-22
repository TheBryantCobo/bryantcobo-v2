<script setup lang="ts">
import scansearchImg from '../assets/scansearch.png';
import bryantcoboImg from '../assets/bryantcobo.png';
import edtechCafeImg from '../assets/edtech-cafe.png';

const projects = [
  {
    id: 1,
    title: 'ScanSearch',
    url: 'https://www.scansearch.com',
    img: scansearchImg,
    desc: 'ScanSearch provides full-text storage and retrieval on all your scanned documents. A long-time friend and former boss approached me with this product idea.',
    links: [
      {
        id: 'link-1-1',
        icon: 'icon-external-link',
        url: 'https://www.scansearch.com',
        title: 'ScanSearch',
      },
    ],
    techs: ['ASP.NET/C#', 'JQuery', 'JSON/REST', 'SQL'],
  },
  {
    id: 2,
    title: 'BryantCobo.com',
    url: 'https://github.com/TheBryantCobo/bryantcobo',
    img: bryantcoboImg,
    desc: "I created the website you're viewing now. The goal was to create a fast and simple site using only HTML, CSS, and Vue. This site was built from scratch, without a template.",
    links: [
      {
        id: 'link-2-1',
        icon: 'icon-github',
        url: 'https://github.com/TheBryantCobo/bryantcobo',
        title: 'GitHub',
      },
    ],
    techs: ['Vue', 'HTML/CSS'],
  },
  {
    id: 3,
    title: 'EdTech Cafe',
    url: 'https://www.youtube.com/c/edtechcafe',
    img: edtechCafeImg,
    desc: 'I was a technology director for a public school district when the pandemic hit. My immediate challenge was to help teachers, students, and parents navigate learning online. To help our learning community I created tutorial videos and shared them on YouTube.',
    links: [
      {
        id: 'link-3-1',
        icon: 'icon-youtube',
        url: 'https://www.youtube.com/c/edtechcafe',
        title: 'EdTech Cafe Channel',
      },
    ],
    techs: ['Camtasia', 'YouTube'],
  },
];
</script>

<template>
  <section
    id="projects"
    class="page-section projects-section"
    aria-labelledby="projects-heading"
  >
    <h1 id="projects-heading">Projects</h1>
    <p>
      Below are some of the projects I have worked on. Most of my professional
      projects are not publicly available, but these showcase a variety of my
      work.
    </p>
    <div class="project-list">
      <article v-for="project in projects" :key="project.id" class="project">
        <a
          :href="project.url"
          class="project-img-link"
          target="_blank"
          rel="noreferrer"
        >
          <img
            :src="project.img"
            :alt="project.title"
            :title="project.title"
            class="project-img"
          />
        </a>
        <div class="project-info">
          <h2 class="project-title">
            <a :href="project.url" target="_blank" rel="noreferrer">
              {{ project.title }}
            </a>
          </h2>
          <p class="project-desc">{{ project.desc }}</p>
          <ul class="project-techs">
            <li v-for="tech in project.techs" :key="tech">{{ tech }}</li>
          </ul>
          <div class="project-links">
            <a
              v-for="link in project.links"
              :key="link.id"
              :href="link.url"
              class="project-link"
              :aria-label="link.title"
              :title="link.title"
              target="_blank"
              rel="noreferrer"
            >
              <span class="icon" :class="link.icon" aria-hidden="true"></span>
            </a>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>
