<template>
<div class="container flex">
    <div class="contentTile" v-for="(tile, index) in tiles" :key="index" :style="{backgroundImage: `url('${tile.image}')`}">
        <div></div>
        <div class="contentButton">
        </div>
        <div class="contentInfo">
            <h3>{{tile.content}}</h3>
            <p>{{tile.category}}</p>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            tiles: [
                {
                    content: 'Inner Workings',
                    category: 'YouTube',
                    link: '',
                    image: 'img/hero-01.png',
                },
                 {
                    content: 'Enz is live!',
                    category: 'Twitch',
                    link: '',
                    image: 'img/hero-04.png',
                },
                 {
                    content: 'Inner Workings',
                    category: 'YouTube',
                    link: '',
                    image: 'img/hero-03.png',
                }
            ]
        } 
    }
    
}
</script>

<style scoped>

    .container {
        margin-bottom: 100px;
    }

    .contentTile {
        flex: 1;
        max-width: 33%;
        flex-direction: column;
        min-height: 450px;
        border-radius: 10px;
        overflow: hidden;
        background-size: cover;
        background-position: center center;
        display: flex;
        justify-content: space-between;
        transition: ease 0.2s;
        transform: translateY(0px);
    }

    .contentTile:hover {
        transform: translateY(4px);
        transition: ease 0.2s;
        cursor: pointer;
    }

    .contentTile:not(:last-of-type) {
        margin-right: 20px;
    }

    .contentButton img {
        height: 100px;
    }

    .contentButton a {
        display: block;
        width: 100%;
        text-align: center;
        padding: 15px;
        color: white;
        text-transform: uppercase;
        text-decoration: none;
        font-weight: bold;
        font-size: 20px;
        transition: ease 0.5s;
    }

    .contentButton a:hover {
        color: var(--highlight-one);
        transition: ease 0.2s;
    }

    .contentInfo h3 {
        padding: 20px 20px 0 20px;
        color: white;
        text-transform: uppercase;
    }

    .contentInfo p {
        padding-left: 20px;
        text-transform: uppercase;
        color: white;

    }

    .contentInfo p:last-of-type {
        padding-bottom: 20px;
    }

    @media only screen and (max-width: 420px) { 
        .flex {
            flex-direction: column;
        }

        .contentTile {
            max-width: 100%;
            margin-bottom: 20px;
        }

        .contentTile:not(:last-of-type) {
        margin-right: 0px;
    }
    }

</style>