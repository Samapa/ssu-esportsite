<template>
    <div class="blue-bg flex">
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

@media only screen and (max-width: 420px) {
    .sponsors {
        flex-direction: column;
        align-items: center;
    }
}


</style>