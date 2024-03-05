<script>

  import axios from 'axios';

  import { store } from './store';

  import CardsList from './components/CardsList.vue';


  export default {
    data() {
      return {

        cards: [],

        store,
        
      }
    },

    created() {

      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(res => {
        console.log(res.data.data),
        this.store.cards = res.data.data
      })
      
    },

    mounted() {
      
    },

    components: {
      CardsList,
    },

    methods: {
      
    },

  }

</script>

<template>

  <div class="container">

    <ul>
    <li v-for="currentCard in cards">
    
      {{ currentCard.name }}

      
    
    </li>
  </ul>

  </div>

  

</template>

<style lang="scss">

</style>
