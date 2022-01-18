<template>
    <section>
        <div class="container">
            <h3>Explore Recent Work</h3>
            <p class="sub-text"> 
                Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Aliquid doloribus aut, fugiat veniam quo id sequi magni et distinctio ipsum
                facilis quasi, vitae tenetur, minima iste? Nihil ab quisquam autem?
            </p>
            <!-- Img card -->
            <div class="works">
                <div v-for="(work, index) in works" :key="index" class="single-card">
                    <img :src="require('../assets/img/' + work.image)" :alt="work.name" />
            
                    <!-- <div class="card-overlay">
                        <div class="icon">
                            <div class="circle"><i class="fas fa-link"></i></div>
                            <div class="circle"><i class="fas fa-search"></i></div>
                        </div>
                        <h4>{{ work.name }}</h4>
                        <p>{{ work.type }}</p>
                    </div> -->
                </div>
            </div>
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