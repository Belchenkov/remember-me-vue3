<template>
  <base-card>
    <div class="flex-around">
      <base-button
          mode="save"
          @click="setSelectedTab('stored-resource')"
      >
        <i class="far fa-save"></i>
        Stored Resources
      </base-button>
      <base-button
          mode="add"
          @click="setSelectedTab('add-resource')"
      >
        <i class="fas fa-plus"></i>
        Add Resources
      </base-button>
    </div>
  </base-card>
  <keep-alive>
    <component :is="selectedTab"></component>
  </keep-alive>
</template>

<script>
import StoredResource from "./StoredResource";
import AddResource from "./AddResource";

export default {
  name: "TheResource",
  data() {
    return {
      selectedTab: 'stored-resource',
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
  provide() {
    return {
      resources: this.storedResources,
      addResource: this.addResource,
      deleteResource: this.removeResource
    }
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
    addResource(title, description, link) {
      const newResource = {
        id: new Date().toISOString(),
        title,
        description,
        link
      };

      this.storedResources.unshift(newResource);
      this.selectedTab = 'stored-resource';
    },
    removeResource(resId) {
      const resIndex = this.storedResources.findIndex(res => res.id === resId);
      this.storedResources.splice(resIndex, 1);
    }
  },
  components: {
    StoredResource,
    AddResource
  }
}
</script>

<style scoped>
  .flex-around {
    display: flex;
    justify-content: space-around;
  }
</style>