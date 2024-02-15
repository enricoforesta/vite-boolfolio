<script>
import axios from 'axios';
import AppContent from './components/AppContent.vue';
export default {
  name: 'App',
  data() {
    return {
      projects: [],
      Url: 'http://127.0.0.1:8000',
      apiUrls: {
        projects: '/api/project'
      }
    }
  },
  components: {
    AppContent
  },
  methods: {
    // chiamata axios
    getProjects() {
      axios.get(this.Url + this.apiUrls.projects).then(response => {
        console.log(response.data);
        return this.projects = response.data;
      }).catch(error => {
        console.log(error)
      })
    },
  },
  created() {
    this.getProjects();
  }
}
</script>

<template>
  <AppContent :projects="projects" />
</template>

<style scoped></style>
