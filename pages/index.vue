<template>
  <v-container class="mt-5">
    <v-row>
      <v-col cols="12" sm="6" lg="4" v-for="personaje in personajes" :key="personaje.id">
       <v-hover v-slot="{hover}">
        <v-card
          color="cyan darken-4"
          class="mb-5"
          dark
          :elevation="hover ? 12 : 2"
        >
          <v-img
            :src="personaje.imagen"
            height="340px"
          >
          </v-img>

          <v-card-title>
            {{personaje.nombre}}
          </v-card-title>
        </v-card>
       </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  

  export default {
    name: 'Home',

    data: () => ({
      personajes: [
        {
          'id' : 1 ,
          'nombre' : 'Morty' ,
          'imagen' : 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
          'id' : 2 ,
          'nombre' : 'Rick' ,
          'imagen' : 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
          'id' : 3 ,
          'nombre' : 'Summer' ,
          'imagen' : 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
          'id' : 4 ,
          'nombre' : 'Beth' ,
          'imagen' : 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
          'id' : 5 ,
          'nombre' : 'Jerry' ,
          'imagen' : 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        }
      ]
    }),
  }
</script>