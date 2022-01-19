<template>
    <section>
        <div class="container">
            <h3>Explore Recent Work</h3>
            <p class="sub-text">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati ex quas, non veritatis provident soluta iure fuga, <br>
                culpa molestias, debitis optio vel ipsa.
            </p>
            <!-- Img card -->
            <div class="works">
                <!-- Single card -->
                <div v-for="(work, index) in works" :key="index" class="single-card">
                    <div class="top-card">
                        <img :src="require('../assets/img/' + work.image)" :alt="work.name" />
                    </div>
                    <!-- Card overlay -->
                    <div class="card-overlay">
                        <div>
                            <span class="icon"><i class="fas fa-link"></i></span>
                            <span class="icon"><i class="fas fa-search"></i></span>
                        </div>
                        <h4>{{ work.name }}</h4>
                        <p>{{ work.type }}</p>
                    </div>
                </div>
            </div>
            <div class="more">View all projects</div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Works',
    props: {
        works: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/works';
</style>