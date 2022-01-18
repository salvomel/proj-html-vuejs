<template>
    <section>
        <div class="container">
            <!-- Title -->
            <h3>Specialists in Modern Construction</h3>
            <p class="sub-text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati ex quas, non veritatis provident soluta iure fuga, culpa molestias, debitis optio vel ipsa.</p>
            <div class="services">
                <!-- Single card -->
                <div v-for="(card, index) in services" :key="index" class="single-card">
                    <div class="icon">
                        <i :class="card.class"></i>
                    </div>
                    <h4>{{ card.title }}</h4>
                    <p>{{ card.text }}</p>
                    <!-- Card overlay -->
                    <!-- <div class="card-overlay">
                        <h3>ARTFULLY CRAFTED</h3>
                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque ipsum
                            fugiat maxime laudantium perferendis consequatur eligendi corrupt
                        </p>
                        <button><a href="#">GET A QUOTE</a></button>
                    </div> -->
                </div> 
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Specialists',
    props: {
        services: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/specialists';
</style>