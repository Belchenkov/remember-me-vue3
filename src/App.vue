<template>
  <ul>
    <learning-resource
        v-for="res in storedResources"
        :key="res.id"
        :title="res.title"
        :description="res.description"
        :link="res.link"
    />
  </ul>
</template>

<script>

import LearningResource from "@/components/learning-resources/LearningResource";

export default {
  name: 'App',
  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue.js documentation',
          link: 'https://vuejs.org'
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn to google...',
          link: 'https://google.org'
        },
        {
          id: 'mozilla',
          title: 'Mozilla',
          description: 'Learn to developer mozilla...',
          link: 'https://developer.mozilla.org'
        }
      ]
    }
  },
  components: {
    LearningResource
  }
}
</script>

<style>
</style>
