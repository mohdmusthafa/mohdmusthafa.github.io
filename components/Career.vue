<template>
  <div>
    <h1 class="uppercase text-xl text-primary font-medium">Career Summary</h1>
      <div v-for="career in careers" :key="career.id" class="career-item">
        <h2>{{ career.job_title }}</h2>
        <div class="flex justify-between">
          <h3 class="text-sm flex-grow">{{ career.company }}</h3>
          <h3 class="text-xs">
            {{ career.start.month }} {{ career.start.year }} -
            {{ career.end.month }} {{ career.end.year }}
          </h3>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      careers: [
        {
          id: 1,
          job_title: 'MERN Stack Developer',
          company: 'Packapeer',
          start: {
            month: 'July',
            year: 2020,
          },
          end: {
            month: 'Nov',
            year: 2020,
          },
          achievements: [
            'Conducted planning, designing, prototyping, and launched en entire web application as team and individual',
            'Designed databases and API Documentations',
            'Discovered patches for API Servers and achieved a perfomance boost of 60%',
          ],
        },
        {
          id: 2,
          job_title: 'Freelance Web Developer',
          company: 'Freelancer',
          start: {
            month: 'Jun',
            year: 2018,
          },
          end: {
            month: 'Mar',
            year: 2020,
          },
          achievements: [
            'Managed complex projects from start to finish',
            'Collaborated with other two developers',
            'Built high-perfomance micro services',
          ],
        },
      ],
    }
  },
}
</script>
