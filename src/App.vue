<script>

  import axios from 'axios';

  export default {
    data() {
      return {
        
      }
    },

    created() {

      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(res => {

      })
      
    },

    mounted() {
      
    },

    components: {

    },

    methods: {
      
    },

  }

</script>

<template>
  prova
</template>

<style lang="scss">

</style>
