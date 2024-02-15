<script>
import axios from 'axios';
import AppContent from './components/AppContent.vue';
export default {
  name: 'App',
  data() {
    return {
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
    getProjects() {
      axios.get(this.Url + this.apiUrls.projects).then(response => {
        console.log(response)
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
  <AppContent />
</template>

<style scoped></style>
