<template>
  <header>
    <img class="mr-5" src="https://img.icons8.com/emoji/31/000000/memo-emoji.png"/>
    <h1>
      {{ title }}
    </h1>
  </header>
</template>

<script>
export default {
  props: [
      'title'
  ],
  name: "TheHeader"
  }
</script>

<style scoped>
  header {
    width: 100%;
    height: 5rem;
    display: flex;
    background-color: #322486;
    justify-content: center;
    align-items: center;
    box-shadow: 0 0 10px rgba(0, 0, 0, .93);
  }

  header h1 {
    font-weight: bold;
    color: rgba(255, 255, 255, .85);
    margin: 0;
    text-shadow: 0 2px 4px rgba(0, 0, 0, .93);
  }
</style>