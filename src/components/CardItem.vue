<script>

    export default {
        name: 'CardItem',

        data() {
            return {
                
            }
        },

        props: {

            card: Object,

        }

    }

</script>


<template>
        
    <li class="card">
        <img :src="card.card_images[0].image_url" :alt="card.name">
        <h4>
            {{ card.name }}
        </h4>
        <span>
            {{ card.archetype }}
        </span>
    </li>

</template>


<style lang="scss">

    @use '../styles/variables' as *;

    .card {
        display: flex;
        flex-direction: column;
        gap: 20px;

        width: calc(100% / 6 - $cardGap / 6);

        text-align: center;
        background-color: orange;
    }


</style>