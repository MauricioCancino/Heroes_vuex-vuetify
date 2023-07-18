<template>
  <div class="about">
    <div class="contenedor">
      <v-data-table
        :headers="headers"
        :items="heroes"
        class="elevation-1 table"
        dark
        
      >
      <template v-slot:[`item.imagen`]="{ item }"
      >
        <img :src="item.imagen" alt="">
      </template>
      </v-data-table>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';

export default {
  name: 'heroes-view',
  data() {
    return {
      headers: [
        { text: 'Heroe', align: 'start', value: 'imagen',},
        { text: 'Name', value: 'nombre' },
        { text: 'Function', value: 'funcion' },
        { text: 'Title', value: 'titulo' },
        { text: 'Atack', value: 'ataque' },
      ],
    };
  },
  computed: {
    ...mapState(['heroes']),
    
  },
};
</script>

<style scoped>
  .about{ 
    background-image: url(https://images.hdqwalls.com/wallpapers/heroes-of-the-storm-10k-2i.jpg);
    background-size:100%;
    background-attachment: fixed;
    
    backdrop-filter: 2px;

  }
  
  .contenedor {
    margin: 0 auto;
    margin-top: 63px;
    padding: 10px;
    width: 70%;
  }
  .table {
    overflow: auto;
    max-height: 90vh;
  }
  img {
    width: 75px;
    height: 75px;
  }
</style>
