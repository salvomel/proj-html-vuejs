<template>
    <section>
        <div class="numbers-background">
            <div v-for="(card, index) in numbers" :key="index" class="single-card">
                <i :class="card.class"></i>
                <div>{{ card.number }}</div>
                <p>{{ card.name }}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Numbers',
    props: {
        numbers: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/numbers';
</style>