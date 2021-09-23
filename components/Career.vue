<template>
  <div class="margin-flex-reset">
    <h1 class="uppercase text-xl text-primary font-medium">Career Summary</h1>
    <div v-for="(career, index) in careers" :key="index" class="career-item">
      <h2>{{ career.job_title }}</h2>
      <div class="flex justify-between">
        <h3 class="text-sm flex-grow">{{ career.company }}</h3>
        <h3 class="text-xs">
          {{ career.start.month }} {{ career.start.year }} -
          {{ career.end.month }} {{ career.end.year }}
        </h3>
      </div>
      <div class="career-item-achievements">
          <ul class="list-disc list-inside mt-2">
            <li
              v-for="achievement in career.achievements"
              :key="achievement"
              class="text-sm"
            >
              {{ achievement }}
            </li>
          </ul>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
      const date = new Date();
    return {
      careers: [
          {
          job_title: 'Technology Consultant',
          company: 'Emvigo Technologies',
          start: {
            month: 'Nov',
            year: 2020,
          },
          end: {
            month: date.toLocaleString('default', { month: 'short' }),
            year: date.getFullYear()
          },
          achievements: [
            'Add 1',
            'Add 2',
            'Add 3',
          ],
        },
        {
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
