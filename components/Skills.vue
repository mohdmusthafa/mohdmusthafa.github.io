<template>
  <div class="glass-1 mob-w-75">
      <h1 class="glass-1-title">Skills</h1>
      <h2 class="text-sm">{{ coding_languages[0] }}, {{ coding_languages[1] }} and {{ coding_languages[2] }}</h2>
      <div class="glass-1-description">
          <h2 class="text-sm mt-2">Coding Languages</h2>
          <ul class="list-disc list-inside mt-1 text-sm">
              <li v-for="language in filterLanguages" :key="language">{{ language }}</li>
          </ul>
          <h2 class="text-sm" >Personal Skills</h2>
          <ul class="list-disc list-inside mt-1 text-sm">
              <li v-for="skill in skills" :key="skill">{{ skill }}</li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            skills: [
                'Fast learner',
                'Team Leading',
                'Public Speaking'
            ],
            coding_languages: [
                'JavaScript/TypeScript',
                'HTML/CSS',
                'Python',
                'MYSQL',
                'C',
                'Java'
            ]
        }
    },
    computed: {
        filterLanguages() {
            const filteredLanguages = [...this.coding_languages];
            filteredLanguages.splice(0, 2)
            return filteredLanguages;
        }
    }
}
</script>

<style>

</style>