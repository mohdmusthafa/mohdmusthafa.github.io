<template>
  <div class="margin-flex-reset">
    <h1 class="uppercase text-xl text-primary font-medium">Education</h1>
    <div class="glass mt-2 mob-w-75">
      <div v-for="education in educations" :key="education.id" class="education-items">
        <h2>{{ education.name }}</h2>
        <h3 class="text-xs">
          {{ education.start.month }} {{ education.start.year }} -
          {{ education.end.month }} {{ education.end.year }}
        </h3>
        <ul class="list-disc list-inside mt-2">
          <li v-for="achievement in education.achievements" :key="achievement" class="text-sm">
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
    return {
      educations: [
      {
          id: 1,
          name: 'Indira Gandhi National Open University',
          start: {
            year: 2022,
            month: 'January',
          },
          end: {
            year: 2025,
            month: 'January',
          },
          achievements: [
            'Bachelor of Computer Applications (BCA)'
          ],
        },
        {
          id: 2,
          name: 'Kalladi Higher Secondary School',
          start: {
            year: 2018,
            month: 'June',
          },
          end: {
            year: 2020,
            month: 'March',
          },
          achievements: [
            'Studied Computer Science',
            'Built a voting application for the school election',
          ],
        }
      ],
    }
  },
}
</script>
