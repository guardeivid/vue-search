<template >
  <div v-if="!results.length">No hay resultados</div>
  <div v-else>
    <ul class="ListResults">
      <ListItem 
        :key="result4.id" 
        :result7="result4" 
        v-for="result4 in results" 
      />
    </ul>
  </div>
</template>

<script>
  import { ListItem } from '@/components'
  export default {
    components: {
      ListItem
    },
    props: {
      results: Array
    }
  }
</script>

<style scoped>
  .ListResults {
    padding:0;
    list-style: none;
  }
  @media (min-width: 576px) {
    .ListResults { column-count: 2; }
  }
  @media (min-width: 768px) {
    .ListResults { column-count: 3; }
  }
  @media (min-width: 992px) {
    .ListResults { column-count: 4; }
  }
  @media (min-width: 1200px) {
    .ListResults { column-count: 5; }
  }
</style>
