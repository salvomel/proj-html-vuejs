<template>
    <main>
        <Jumbotron_1 />
        <Specialists :services= "cards.services" />
    </main>
</template>

<script>
import Jumbotron_1 from "./Jumbotron_1.vue";
import Specialists from "./Specialists.vue";

export default {
    name: 'Main',
    components: {
        Jumbotron_1,
        Specialists,
    },
     props:{
        cards: Object,
    }
}
</script>

<style scoped lang="scss">
    
</style>

