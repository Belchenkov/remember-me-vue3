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
    background-color: #374051;
    border: 1px solid #374051;
    color: white;
    cursor: pointer;
    font-weight: bold;
    text-shadow: 0 0 2px rgba(0, 0, 0, .7);
    transition: all .2s ease-in-out;
  }

  button:hover,
  button:active {
    background-color: #e0102a;
    border-color: #e0102a;
  }

  .danger {
    background-color: #a52939;
    border: 1px solid #a52939;
  }

  button:hover.danger,
  button:active.danger {
    background-color: #e0102a;
    border-color: #e0102a;
  }

  .save {
    background-color: #b9ca15;
    border: 1px solid #b9ca15;
  }

  button:hover.save,
  button:active.save {
    background-color: #d1e50a;
    border-color: #d1e50a;
  }

  .add {
    background-color: #28702a;
    border: 1px solid #28702a;
  }

  button:hover.add,
  button:active.add {
    background-color: #19b31d;
    border-color: #19b31d;
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