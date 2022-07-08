<template>
  <div class="grid">
    <GridItem v-for="item in items" :key="item.id" :item="item" />
  </div>
</template>

<script>
import GridItem from './GridItem.vue';
export default {
  name: 'DataGrid',
  components:{
    GridItem
  },
  props: {
    items: Array,
  }
}
</script>