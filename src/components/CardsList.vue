<script>

    import { store } from '../store'
    import CardItem from './CardItem.vue';

    export default {
        name: 'CardsList',

        data() {
            return {
                store,
            }
        },

        components: {
            CardItem,
        }

    }

</script>


<template>
        
    <h1>Carte Yu Gi Oh</h1>

    <ul>

        <CardItem v-for="currentCard in store.cards" :card="currentCard">
        </CardItem>

    </ul>

</template>


<style lang="scss">

</style>