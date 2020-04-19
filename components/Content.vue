<template>
  <div class="container flex">
    <div class="contentTile" v-for="(tile, index) in tiles" :key="index">
    
        <img :src="tile.image" />
        <div></div>
        <a :href="tile.link" target="_blank">
        <div class="contentInfo">
        <img :src="tile.platform" />
          <h3>{{tile.content}}</h3>
          <p>{{tile.category}}</p>
        </div>
        </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tiles: [
        
        {
          content: "ENZ",
          category: "Twitch Streamer",
          link: "https://twitch.tv/enz2h",
          platform: 'img/TwitchLogo-01.svg',
          image: "img/enz2h.jpeg"
        },
        {
          content: "FAZZ",
          category: "Twitch Streamer",
          link: "https://www.twitch.tv/idkfazz/",
          platform: 'img/TwitchLogo-01.svg',
          image: "img/fazz.png"
        },
        {
          content: "Inner Workings",
          category: "YouTube Video",
          link: "https://www.youtube.com/watch?v=677m8Tyyaww",
           platform: 'img/YouTubeLogo-01.svg',
          image: "img/content-01.png"
        }
      ]
    };
  }
};
</script>

<style scoped>
.container {
  margin-bottom: 100px;
}

.flex {
    flex-wrap: wrap;
}

a {
    text-decoration: none;
}

.contentTile {
  flex: 1;
  max-width: 33%;
  min-width: 30%;
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
  margin: 10px 20px 10px 0;
  
}

.contentTile > img {
  height: 100%;
  width: 100%;
  position: absolute;
  z-index: -1;
  object-fit: cover;
  filter: brightness(0.5);
}

.contentTile:hover {
  transform: translateY(4px);
  transition: ease 0.2s;

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

.contentInfo {
    padding-left: 20px;
}

.contentInfo h3 {
  padding: 20px 20px 0 0;
  color: white;
  text-transform: uppercase;
}

.contentInfo p {
  
  text-transform: uppercase;
  color: white;
}

.contentInfo img {
    width: 50px;
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
    margin-right: 0px;
  }

}
</style>