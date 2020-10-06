<template>
  <the-header title="Remember Me" />
  <the-resource />
</template>

<script>
import TheHeader from "@/components/layouts/TheHeader";
import TheResource from "@/components/learning-resources/TheResources";

export default {
  name: 'App',
  components: {
    TheResource,
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
