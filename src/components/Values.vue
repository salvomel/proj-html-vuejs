<template>
    <section>
        <div class="container">
            <h3>Our core values</h3>
            <p class="sub-text">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                Eum obcaecati ex quas, non veritatis provident soluta iure fuga, culpa molestias, debitis optio vel ipsa.
            </p>
            <!-- Card -->
            <div class="values">
                <div v-for="(value, index) in values" :key="index" class="single-card">
                    <div :class="value.color" class="icon icon-hover">
                        <i :class="value.class"></i>
                    </div>
                    <h4>{{ value.title }}</h4>
                    <p>{{ value.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Values',
    props: {
        values: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/values';
</style>