<script setup lang="ts">
import { ref } from 'vue';

const jobs = [
  {
    id: 1,
    company: 'CDS Logistics',
    title: 'Senior Software Engineer',
    term: '2022-Present',
    description:
      'Design, develop, and maintain software solutions for logistics operations. Products include web applications and data integration automation.',
  },
  {
    id: 2,
    company: 'ScanSearch',
    title: 'CTO',
    term: '2021-2022',
    description:
      'Design and develop online document imaging and workflow solutions for a SaaS environment. Deploy and manage systems using the Microsoft Azure platform.',
  },
  {
    id: 3,
    company: 'School District of Manawa',
    title: 'Technology Director',
    term: '2017-2021',
    description:
      'Technology leader and part of the school district administration team. Responsible for all aspects of technology including network administration, server management, systems integration, training, and maintenance.',
  },
  {
    id: 4,
    company: 'Manitowoc School District',
    title: 'Data & Technology Specialist',
    term: '2014-2017',
    description:
      'Serve as technology advisor to administrators and educators. Trusted on projects involving classroom technology, communications, professional development, assessment, and custom software design. Collaborate with others to build consensus, plan, and implement technology goals.',
  },
  {
    id: 5,
    company: 'Open Scan Technologies',
    title: 'Senior Software Engineer',
    term: '2011-2013',
    description:
      'Designed enterprise document imaging and workflow management solutions to streamline and automate accounts payable processes. Developed using .NET, Microsoft SQL Server, and AJAX technologies.',
  },
  {
    id: 6,
    company: 'DocEdge',
    title: 'Owner',
    term: '2004-2011',
    description:
      'Developed, marketed, and maintained custom accounts payable solutions. Consulted with clients to understand goals and tailor solution to fit their needs. Integrated disparate systems to create unified solutions.',
  },
];

const selectedJob = ref(jobs[0]);
</script>

<template>
  <section
    id="experience"
    class="page-section experience-section"
    aria-labelledby="experience-heading"
  >
    <h1 id="experience-heading">Experience</h1>
    <div class="experience-widget">
      <div class="job-list" role="tablist" aria-label="Experience">
        <button
          v-for="job in jobs"
          :id="`job-tab-${job.id}`"
          :key="job.id"
          class="job-option"
          :class="{ 'job-selected': selectedJob.id === job.id }"
          type="button"
          role="tab"
          :aria-selected="selectedJob.id === job.id"
          aria-controls="job-details"
          @click="selectedJob = job"
        >
          {{ job.company }}
        </button>
      </div>
      <div
        id="job-details"
        class="job-details"
        role="tabpanel"
        :aria-labelledby="`job-tab-${selectedJob.id}`"
        tabindex="0"
      >
        <h2 class="job-title">{{ selectedJob.title }}</h2>
        <p class="job-company">@ {{ selectedJob.company }}</p>
        <p class="job-term">{{ selectedJob.term }}</p>
        <p class="job-description">{{ selectedJob.description }}</p>
      </div>
    </div>
  </section>
</template>
