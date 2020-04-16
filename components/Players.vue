<template>
     <div>
        <div class="slider">
         <TitleBlock style="color: #ffffff;">Players</TitleBlock>
        <img src="img/background-04.png" />
          <div class="slide-container">
              <img class="fade" :src="players[currentPlayer].image">
              <div>
                <h3>{{players[currentPlayer].fname}} <span class="lastname">{{players[currentPlayer].lname}}</span></h3>
                <h2>{{players[currentPlayer].ingamename}}</h2>
                <!-- <div @click="(currentPlayer + 1) == player.length ? currentPlayer = 0 : currentPlayer++">
                    next slide
                </div> -->
            </div>
              
          </div>

          <div class="wrapper">
                  <div v-for="(player, index) in players" :key="index" @click="currentPlayer = index" :class="{selected: currentPlayer == index}">
                     <p>{{player.description}}</p>
                  </div>
              </div>
          
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
        currentPlayer: 0,
        players: [
           {
                fname: 'Brad',
                lname: 'Manchild',
                ingamename: 'enz',
                url: '',
                image: 'img/players/player-01.png',
                description: 'Captain'
            },
             {
                fname: 'Kevin',
                lname: 'Johnston',
                ingamename: 'KlOwNie',
                url: '',
                image: 'img/players/player-02.png',
                description: 'IGL'
            }
            ,
            {
                fname: 'Chris',
                lname: 'Fenech',
                ingamename: 'thrila',
               url: '',
                image: 'img/players/player-03.png',
                description: 'Entry'
            }
            ,
            {
                fname: 'Cody',
                lname: 'Hancock',
                ingamename: 'crypt1c',
                url: '',
                image: 'img/players/player-04.png',
                description: 'Support'
            }
            ,
            {
                fname: 'Aaron ',
                lname: 'Bretherton',
                ingamename: 'FAZZ',
                url: '',
                image: 'img/players/player-05.png',
                description: 'Awper'
            }
        ]
        }
    }
}
</script>

<style scoped>

@media only screen and (max-width: 420px) {

.slide-container {
    display: flex;
    width: 100%;
    flex-direction: column;
    align-items: center;
    color: white;
    text-align: center;
    align-self: center

  }

  .slide-container h2 {
      -webkit-text-fill-color: transparent !important;
      -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: #fff;
      font-size: 50px;
      line-height: 0.7;
  }

  .slide-container h3 {
      color: white;
      text-transform: uppercase;
      font-weight: bold;
      font-size: 20px;
      
  }

  .lastname {
      color: var(--highlight-one);
      font-size: 25px;
  }

  .slide-container img {
      width: 250px;
      margin: 20px 0px;
  }

 .slider > img {
      height: 750px;
      width: 100%;
      position: absolute;
      z-index: -1;
      object-fit: cover;
      filter: brightness(0.5);
  }

  .wrapper {
    display: flex;
    width: 350px;
    align-self: center;
    margin: auto;
    
}

.wrapper div {
    width: 100%;
    margin: 0 7px;
    align-self: flex-end;
    transition: ease 0.2s;
    box-shadow: inset 0px 2px white;
    padding-top: 15px;
    transition: all 0.2s ease;
}

.wrapper div.selected {
    box-shadow: inset 0px 4px #ce922a;
    transition: all 0.2s ease;
}

.wrapper p {
    font-size: 14px;
    color: white;
    text-align: center;
}

  .slider {
    position: relative;
    width: 100%;
    height: 750px;
    flex-direction: column;
    display: flex
  }
}

@media only screen and (min-width: 421px) {

.wrapper {
    display: flex;
    justify-content: center;
    width: 1000px;
    margin: auto;
}

.wrapper p {
    width: 100px;
}

 .slider > img {
      position: absolute;
      top: 0;
      left: 0;
      filter: brightness(0.5);
        height: 850px;
        width: 100%;
      object-fit: cover;
      z-index: -1;  
  }

.wrapper div {
    margin-right: 15px;
    align-self: flex-end;
    transition: ease 0.2s;
    color: white;
    box-shadow: inset 0px 2px white;
    padding-top: 15px;
    transition: all 0.2s ease;
}

.wrapper div.selected {
    box-shadow: inset 0px 4px #ce922a;
    transition: all 0.2s ease;
}

.wrapper div:hover {
    cursor: pointer;
    transform: translateY(4px);
    transition: ease 0.2s;
}

  .slide-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 1000px;
    margin: auto;

  }

  .slide-container img {
      height: 500px;
  }

    .slide-container a {
      color: white;
      text-transform: capitalize;
      background-color: transparent;
      border: solid 1px rgba(255, 255, 255,0.4);
      padding: 10px 50px;
      border-radius: 5px;
      margin: 10px 0;
      text-decoration: none;
      font-weight: bold;
      transition: ease 0.5s;
      
  }

  .slide-container a:hover {
      background-color: #ce922a;
      transition: ease 0.5s;
      border: solid 1px #ce922a;
  }

  .slide-container h2 {
      -webkit-text-fill-color: transparent !important;
      -webkit-text-stroke-width: 2px;
    -webkit-text-stroke-color: #fff;
      font-size: 130px;
      line-height: 0.7;
  }

  .slide-container h3 {
      color: white;
      text-transform: uppercase;
      font-weight: bold;
      font-size: 30px;
      
  }

  .lastname {
      color: var(--highlight-one);
      font-size: 50px;
  }

  .slider {
    position: relative;
    width: 100%;
    height: 850px;
    display: flex;
    flex-direction: column;
    margin-top: 40px;
  }

}
</style>