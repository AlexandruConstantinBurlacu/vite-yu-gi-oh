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
        
    <li>
        {{ card.name }}
    </li>

</template>


<style lang="scss">

</style>