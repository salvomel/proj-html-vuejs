<template>
    <main>
        <Jumbotron />
        <Specialists :services= "cards.services" />
        <Numbers :numbers= "cards.numbers" />
        <Works :works= "cards.works" />
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import Specialists from "./Specialists.vue";
import Numbers from "./Numbers.vue";
import Works from "./Works.vue";

export default {
    name: 'Main',
    components: {
        Jumbotron,
        Specialists,
        Numbers,
        Works,
    },
     props:{
        cards: Object,
    }
}
</script>

<style scoped lang="scss">
    
</style>

