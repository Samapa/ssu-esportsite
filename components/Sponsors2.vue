<template>
    <div class="blue-bg flex">
        <img src="img/banner-05.png" class="banner" alt="banner"/>
        <TitleBlock style="color: white">Sponsors</TitleBlock>
        <div class="container">
            <ul class="sponsors">
                <li v-for="(sponsor, index) in sponsors" :key="index">
                    <a>
                        <img :src="sponsor.image" />
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import TitleBlock from '~/components/Title.vue'

export default {
    components: {
        TitleBlock
    },
    data() {
        return {
            sponsors: [
                {
                    image: '',
                }
            ]
        }
    }
}
</script>

<style scoped>

    .banner {
        object-position: center center;
    }

    .blue-bg {
        background-color: #011321;
        flex-direction: column;
    }

    ul {
        display: flex;
        padding: 0;
        list-style: none;
        
    }

    ul li {
        margin-right: 20px;
        
    }

    ul li img {
        width: 150px;
    }

    .sponsors {
        flex-direction: column;
    }

@media only screen and (max-width: 420px) {
    .sponsors {
        flex-direction: column;
        align-items: center;
    }
}


</style>