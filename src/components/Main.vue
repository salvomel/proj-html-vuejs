<template>
    <main>
        <Jumbotron />
        <Specialists :services= "cards.services" />
        <Numbers :numbers= "cards.numbers" />
        <Works :works= "cards.works" />
        <Values :values= "cards.values"/>
        <Owners />
        <News :news= "cards.news"/>
        <Partners :partners= "cards.partners"/>
        <Building />
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import Specialists from "./Specialists.vue";
import Numbers from "./Numbers.vue";
import Works from "./Works.vue";
import Values from "./Values.vue";
import Owners from "./Owners.vue";
import News from "./News.vue";
import Partners from "./Partners.vue";
import Building from "./Building.vue";

export default {
    name: 'Main',
    components: {
        Jumbotron,
        Specialists,
        Numbers,
        Works,
        Values,
        Owners,
        News,
        Partners,
        Building
    },
     props:{
        cards: Object,
    }
}
</script>

<style scoped lang="scss">
</style>

