<template>
<div>
  <div class="glass-1 mt-2">
      <h1 class="glass-1-title">Tools</h1>
      <h2 class="text-sm">{{ tools[0] }}, {{ tools[1] }} and {{ tools[2] }}</h2>
      <div class="glass-1-description">
          <ul class="list-disc list-inside mt-2 text-sm">
              <li v-for="tool in filterTools" :key="tool">{{ tool }}</li>
          </ul>
      </div>
  </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            tools: [
                'NodeJs',
                'ReactJs',
                'Linux',
                'React Native',
                'ExpressJs',
                'MongoDB',
                'Redux',
                'MySQL',
                'Redis',
                'AWS',
                'Docker/Kubernetes',
            ]
        }
    },
    computed: {
        filterTools() {
            const tools = [...this.tools];
            tools.splice(0, 2)
            return tools;
        }
    }
}
</script>

<style>

</style>