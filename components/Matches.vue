<template>
<div class="container flex">
    <div class="matchTile" v-for="(tile, index) in tiles" :key="index">
        <div class="mapCard" :style="{backgroundImage: `url('${maps[tile.map]}')`}"></div>
        <div class="matchInfo">
            <h3>SSU vs {{tile.vs}}</h3>
            <p>📅 {{tile.date}}</p>
            <p>{{tile.map}}</p>
        </div>
        <div class="matchButton">
            <a :href="tile.link" target="_blank">View Match</a>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            maps: {
                mirage: 'https://static.hltv.org/images/galleries/1693-medium/1370663191.8834.jpeg',
                cobble: 'https://i.ytimg.com/vi/TxIFspGUlaQ/maxresdefault.jpg',
                inferno: 'https://vignette.wikia.nocookie.net/cswikia/images/f/f0/Inferno.jpg/revision/latest?cb=20161014013320',
                TBA: 'img/map-tba-01.png'
            },
            tiles: [
                {
                    match: '',
                    date: '16/10/2020',
                    vs: 'MARKandLARRY',
                    link: 'https://play.esea.net/match/15918825',
                    map: 'inferno'
                },
                {
                    match: '',
                    date: 'TBA',
                    vs: 'TBA',
                    link: '',
                    map: 'TBA'
                },
                {
                    match: '',
                    date: 'TBA',
                    vs: 'TBA',
                    link: '',
                    map: 'TBA'
                }
            ]
        } 
    }
    
}
</script>

<style scoped>

.matchTile {
    flex-direction: row;
}

    .matchTile {
        flex: 1;
        max-width: 33%;
        background-color: white;
        border-radius: 10px;
        overflow: hidden;
    }

    .matchTile:not(:last-of-type) {
        margin-right: 20px;
    }

    .mapCard {
        background-size: cover;
        height: 250px;
        background-position: center center;
    }

    .matchButton a {
        display: block;
        width: 100%;
        background-color: var(--highlight-one);
        text-align: center;
        padding: 15px;
        color: white;
        text-transform: uppercase;
        text-decoration: none;
        font-weight: bold;
        font-size: 20px;
        transition: ease 0.5s;
    }

    .matchButton a:hover {
        color: #ffffff;
        background-color: #011321;
        transition: ease 0.2s;
    }

    .matchInfo h3 {
        padding: 20px 10px 20px 20px;
    }

    .matchInfo p {
        padding: 10px 20px;
        text-transform: capitalize;
    }

    .matchInfo p:last-of-type {
        padding-bottom: 20px;
    }

    @media only screen and (max-width: 420px) { 
        .flex {
            flex-direction: column;
        }

        .matchTile {
            max-width: 100%;
            margin-bottom: 20px;
        }

        .matchTile:not(:last-of-type) {
        margin-right: 0px;
    }
    }

</style>