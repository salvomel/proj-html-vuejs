<template>
    <header class="container">
        <div class="header-wrapper">
            <div class="logo">
                <img src="../assets/img/construction_logo.png" alt="Logo">
            </div>

            <nav>
                <ul class="menu">
                    <li v-for="(link, index) in links" :key="index" :class="{current: link.current}">
                        <a :href="link.url">{{link.text}}</a>
                    </li>
                    <li>
                        <a class="my-btn" href="#">get quote</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        links: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/header';
</style>

