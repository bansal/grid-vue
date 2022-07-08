<template>
  <div id="app" class="container">
    <Banner title="front-end" image="https://images.unsplash.com/photo-1510784722466-f2aa9c52fff6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8c3VucmlzZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=800&q=60" heading="valtech_" summary="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt." />
    <DataGrid :items="items" />
  </div>
</template>

<script>
import DataGrid from './components/DataGrid.vue'
import Banner from './components/Banner.vue'

export default {
  name: 'App',
  data(){
    return {
      items: [],
    }
  },
  components: {
    Banner,
    DataGrid
  },
  mounted(){
    this.fetchData();
  },
  methods:{
    async fetchData() {
        const dataUrl = "/data.json"; // can be any rest api url that support get method.
        const data = await fetch(dataUrl);
        this.items = await data.json();
    },
  }
}
</script>