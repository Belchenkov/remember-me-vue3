<template>
  <base-card>
    <base-button @click="setSelectedTab('stored-resources')">
      <i class="far fa-save"></i>
      Stored Resources
    </base-button>
    <base-button @click="setSelectedTab('add-resources')">
      <i class="fas fa-plus"></i>
      Add Resources
    </base-button>
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredResource from "./StoredResource";
import AddResource from "./AddResource";

export default {
  name: "TheResource",
  data() {
    return {
      selectedTab: 'stored-resource'
    }
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    }
  },
  components: {
    StoredResource,
    AddResource
  }
}
</script>

<style scoped>

</style>