<template>
    <section>
        <div class="container">
            <h3>Trusted Partners</h3>
            <p class="sub-text">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                Eum obcaecati ex quas, non veritatis provident soluta iure fuga, culpa molestias, debitis optio vel ipsa.
            </p>
            <!-- Partners -->
            <div class="partners">
                <div v-for="(partner, index) in partners" :key="index" class="single-card">
                    <img :src="require('../assets/img/' + partner.image)" alt="Partner Logo">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Partners',
    props: {
        partners: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/partners';
</style>