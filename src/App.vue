<template>
  <the-header title="Remember Me" />
</template>

<script>

import TheHeader from "@/components/layouts/TheHeader";

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
    TheHeader
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Miriam+Libre:wght@400;700&display=swap');

* {
    box-sizing: border-box;
  }

  html {
    font-family: 'Miriam Libre', sans-serif;
  }

  body {
    margin: 0;
  }

  .mr-5 {
    margin-right: 5px;
  }
</style>
