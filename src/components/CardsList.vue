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

    <ul class="cardsList">

        <CardItem v-for="currentCard in store.cards" :card="currentCard">
        </CardItem>

    </ul>

</template>


<style lang="scss">

    @use '../styles/variables' as *;

    .cardsList {
        display: flex;
        flex-wrap: wrap;
        gap: $cardGap;
    }

</style>