<template>
    <section>
        <div class="jumbotron2">
            <div v-for="(card, index) in numbers" :key="index" class="single-card">
                <i :class="card.class"></i>
                <div>{{ card.number }}</div>
                <p>{{ card.role }}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Jumbotron_2',
    props: {
        numbers: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/jumbotron2';
</style>