<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <div class="wrapper row">

                    <!-- Company -->
                    <div class="company col-3">
                        <img src="../assets/img/footer-logo.png" alt="Logo" />
                        <p>
                            We are specialists in the constructions of unique and exclusive
                            properties. Our work Inspires. We pride ourselves on delivering
                            outstanding quality and design for leading clients across the world
                        </p>
                        <button><a href="#">LEARN MORE</a></button>
                    </div>

                    <!-- Tweets -->
                    <div class="tweets col-3">
                        <h3>LATEST TWEETS</h3>
                        <div v-for="(tweet, indexT) in tweets" :key="indexT" class="tweetcard">

                            <div class="left-side">
                                <img :src="require('../assets/img/' + tweet.profilepic)" alt="Profile picture" class="profilepic"/>
                            </div>

                            <div class="right-side">
                                <div class="tweet-head">
                                    <div class="name">
                                        <div class="user">{{ tweet.user }}</div>
                                        <div class="username">@{{ tweet.username }}</div>
                                    </div>
                                    <img :src="require('../assets/img/' + tweet.logo)" alt="Twitter logo" class="logo"/>
                                </div>

                                <p>{{ tweet.text }}</p>
                                <img :src="require('../assets/img/' + tweet.img)" alt="Tweet img" class="img-tweet" />

                                <div class="tweet-bottom">
                                    <div class="left-bottom">
                                        <img :src="require('../assets/img/' + tweet.like)" alt="Like btn" class="like" />
                                        <img :src="require('../assets/img/' + tweet.share)" alt="Share btn" class="share" />
                                    </div>
                                    <div class="data">{{ tweet.date }}</div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Contacts -->
                    <div class="contacts col-3">
                        <h3>CONTACT US TODAY</h3>
                        <ul>
                            <li v-for="(contact, indexC) in contacts" :key="indexC">
                                <i :class="contact.class"></i>
                                <a :href="contact.url">{{ contact.text }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- Find us -->
                    <div class="map col-3">
                        <h3>FIND US</h3>
                        <img src="../assets/img/construction_map_pin.png" alt="Map">
                    </div>
                </div>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="container wrapper">
                <div class="copyright">
                    <span>Copyright 2022 Avada theme by <strong>Theme Fusion</strong>&nbsp;&nbsp;  |  &nbsp;&nbsp;All rights reserved&nbsp;&nbsp;  |
                    &nbsp;&nbsp;Powered by <strong>Salvatore Meli</strong></span>
                </div>
                <div class="socials">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        tweets: Array,
        contacts: Array
    }
}
</script>

<style scoped lang="scss">
    @import '../style/footer';
</style>