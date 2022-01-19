<template>
    <section>
        <div class="container">
            <h3>Latest News</h3>
            <p class="sub-text">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati ex quas, non veritatis provident soluta iure fuga, <br>
                culpa molestias, debitis optio vel ipsa.
            </p>
            <!-- Img card -->
            <div class="news">
                <div v-for="(art, index) in news" :key="index" class="single-card">
                    <img :src="require('../assets/img/' + art.image)" :alt="art.title" />
                    <div class="article">
                        <h4>{{ art.title }}</h4>
                        <p class="date">{{ art.date }}</p>
                        <p class="text">{{ art.text }}</p>
                    </div>

                    <!-- <div class="card-overlay">
                        <div class="icon">
                            <div class="circle"><i class="fas fa-link"></i></div>
                            <div class="circle"><i class="fas fa-search"></i></div>
                        </div>
                            <h4>Redeveloping Florida's Remote Southern Coast</h4>
                            <p>Architecture, Buildings, Construction, News</p>
                    </div> -->
                </div>
            </div>
            <div class="more">View all projects</div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'News',
    props: {
        news: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/news';
</style>