<template>
    <main>
        <Jumbotron />
        <Specialists :services= "cards.services" />
        <Numbers :numbers= "cards.numbers" />
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import Specialists from "./Specialists.vue";
import Numbers from "./Numbers.vue";

export default {
    name: 'Main',
    components: {
        Jumbotron,
        Specialists,
        Numbers,
    },
     props:{
        cards: Object,
    }
}
</script>

<style scoped lang="scss">
    
</style>

