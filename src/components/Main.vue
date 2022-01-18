<template>
    <main>
        <Jumbotron1 />
        <Specialists :services= "cards.services" />
        <Jumbotron2 :numbers= "cards.numbers" />
    </main>
</template>

<script>
import Jumbotron1 from "./Jumbotron1.vue";
import Specialists from "./Specialists.vue";
import Jumbotron2 from "./Jumbotron2.vue";

export default {
    name: 'Main',
    components: {
        Jumbotron1,
        Specialists,
        Jumbotron2,
    },
     props:{
        cards: Object,
    }
}
</script>

<style scoped lang="scss">
    
</style>

