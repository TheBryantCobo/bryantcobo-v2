<script setup lang="ts">
import SkillsSection from './SkillsSection.vue';
import ExperienceSection from './ExperienceSection.vue';
import ProjectsSection from './ProjectsSection.vue';
import ContactSection from './ContactSection.vue';
</script>

<template>
  <span id="top"></span>
  <header class="site-header">
    <a class="site-brand" href="#top" aria-label="Bryant Cobarrubias, home">
      <span>B</span>
      <span>C</span>
    </a>
    <nav class="site-nav" aria-label="Main navigation">
      <a href="#skills">Skills</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <aside class="social-container" aria-label="Social links">
    <ul>
      <li>
        <a href="mailto:me@bryantcobo.com" aria-label="Email">
          <span class="icon icon-envelope" aria-hidden="true"></span>
        </a>
      </li>
      <li>
        <a
          href="https://github.com/TheBryantCobo/"
          target="_blank"
          rel="noreferrer"
          aria-label="GitHub"
        >
          <span class="icon icon-github" aria-hidden="true"></span>
        </a>
      </li>
      <li>
        <a
          href="https://www.youtube.com/c/edtechcafe"
          target="_blank"
          rel="noreferrer"
          aria-label="YouTube"
        >
          <span class="icon icon-youtube" aria-hidden="true"></span>
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/bryantcobo"
          target="_blank"
          rel="noreferrer"
          aria-label="Twitter"
        >
          <span class="icon icon-twitter" aria-hidden="true"></span>
        </a>
      </li>
      <li>
        <a
          href="https://www.linkedin.com/in/bryantcobarrubias/"
          target="_blank"
          rel="noreferrer"
          aria-label="LinkedIn"
        >
          <span class="icon icon-linkedin" aria-hidden="true"></span>
        </a>
      </li>
    </ul>
  </aside>

  <main class="page-content">
    <section id="about" class="page-section" aria-labelledby="about-heading">
      <div class="about-text">
        <h1 id="about-heading">
          <span class="light-green">Bryant</span>&nbsp;
          <span class="dark-green">Cobarrubias</span>
        </h1>
        <h2>Senior Full-Stack Developer</h2>
        <p>
          I’m an full-stack developer based in Wisconsin. I’ve been creating
          software for almost 30 years, working for a variety of customers and
          industries.
        </p>
        <p>I am not presently seeking new employment opportunities.</p>
      </div>
      <img
        src="../assets/bryant-cobarrubias.png"
        alt="Bryant Cobarrubias"
        class="about-picture"
      />
    </section>

    <SkillsSection />

    <ExperienceSection />

    <ProjectsSection />

    <ContactSection />
  </main>

  <footer class="site-footer">
    <p>&copy; {{ new Date().getFullYear() }} Bryant Cobarrubias</p>
  </footer>
</template>
