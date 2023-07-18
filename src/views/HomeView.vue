<template>
  <div class="home">
    <v-container>
      <v-row no-gutters justify="center">
        <v-col cols="12" sm="4" md="6" class="box text-center " >
          <h1>Desafía las expectativas de los MOBA</h1>
          <span></span>
          <p>Épicos héroes y acción sin cesar en múltiples campos de batalla.</p>
          <div class="d-flex justify-center">
          <v-btn
          @click="$router.push(`/heroes`)"
          color='orange darken-3'
          class="mb-5"
          
          >Ver héroes</v-btn>
          </div>
        </v-col>
      </v-row>
      </v-container>
      <v-alert
      border='left'
      color='purple darken-1'
      dark
      class='py-6'
      >Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum minima vitae perferendis officiis itaque dolore reiciendis iusto, numquam error tempora nam facere sed quasi adipisci, excepturi rerum. Cum, labore similique?
      </v-alert>
    

  </div>
</template>

<script>
  

  export default {
    name: 'home-view',

    components: {
      
    },
  }
</script>

<style scoped>
  .home {
    
    background-image: url(https://images.hdqwalls.com/wallpapers/heroes-of-the-storm-88.jpg);
    background-size:120%;
    background-attachment: fixed;
    height: 100%;
    
  }
  .box{
        border:2px solid whitesmoke;
        margin-top: 250px;
        color: whitesmoke;
    }
  
</style>
