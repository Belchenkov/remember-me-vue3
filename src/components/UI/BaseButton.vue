<template>
  <button :type="type" :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "BaseButton",
  props: [
      'type',
      'mode'
  ]
}
</script>

<style scoped>
  button {
    padding: 0.75rem 1.5rem;
    font-family: inherit;
    background-color: #a52939;
    border: 1px solid #a52939;
    color: white;
    cursor: pointer;
  }

  button:hover,
  button:active {
    background-color: #e0102a;
    border-color: #e0102a;
  }

  .flat {
    background-color: transparent;
    color: #e0102a;
    border: none;
  }

  .flat:hover,
  .flat:active {
    background-color: #edd2ff;
  }
</style>