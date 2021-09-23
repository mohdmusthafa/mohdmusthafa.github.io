<template>
<div class="glass-1-container">

  <div class="glass-1">
      <h1 class="glass-1-title">Tools</h1>
      <h2 class="text-sm">Node.js, React and Linux</h2>
      <div class="glass-1-description">
          <ul class="list-disc list-inside mt-2">
              <li v-for="tool in tools" :key="tool">{{ tool }}</li>
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
                'React Native',
                'ExpressJs',
                'MongoDB',
                'Redux',
                'MySQL',
                'Redis',
                'AWS',
                'Docker/Kubernetes',
                'Linux'
            ]
        }
    }
}
</script>

<style>

</style>