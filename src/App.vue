<template>
  <ul>
    <stored-resource
      v-for="res in storedResources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></stored-resource>
  </ul>
</template>

<script>
import StoredResource from './components/learning-resources/StoredResource.vue';
export default {
  components: {
    StoredResource,
  },
  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue.js documentation',
          link: 'https://vuejs.org/',
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn to google...',
          link: 'https://google.com/',
        },
      ],
    };
  },
};
</script>
