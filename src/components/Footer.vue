<template>
    <footer>
        <div class="container">
            <div class="wrapper row">
                <!-- Company -->
                <div class="company col-3">
                    <img src="../assets/img/construction_logo.png" alt="" />
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
                            <img :src="require('../assets/img/' + tweet.profilepic)" alt="" class="profilepic"/>
                        </div>

                        <div class="right-side">
                            <div class="tweet-head">
                                <div class="name">
                                    <h6>{{ tweet.username }}</h6>
                                    <div>@{{ tweet.username }}</div>
                                </div>
                                <img :src="require('../assets/img/' + tweet.logo)" alt="" class="logo"/>
                            </div>

                            <p>{{ tweet.text }}</p>
                            <img :src="require('../assets/img/' + tweet.img)" alt="" class="img-tweet" />
                            
                            <div class="tweet-bottom">
                                <div class="left-bottom">
                                    <img :src="require('../assets/img/' + tweet.like)" alt="" class="like" />
                                    <img :src="require('../assets/img/' + tweet.share)" alt="" class="share" />
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