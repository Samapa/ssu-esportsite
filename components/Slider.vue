<template>
  <div>
      <div class="slider">
        
        <img class="fade" :src="banner[currentSlide].image">
          <div class="slide-container">
                  <img src="/img/logo.svg" alt="ssu-logo" class="logo"/>
              <h3>{{banner[currentSlide].category}}</h3>
              <h2>{{banner[currentSlide].title}}</h2>
              <a :href="banner[currentSlide].url">Read More</a>
              <!-- <div @click="(currentSlide + 1) == banner.length ? currentSlide = 0 : currentSlide++">
                  next slide
              </div> -->
              <div class="wrapper">
                  <div v-for="(item, index) in banner" :key="index" @click="currentSlide = index" :class="{selected: currentSlide == index}">
                     <p>{{item.description}}</p>
                  </div>
              </div>
          </div>
          
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
    currentSlide: 0,
      banner: [
        {
          category: "esports",
          title: "SSU Esports win AEM Sydney",
          image: "https://drive.google.com/uc?export=download&id=1quZpS5UE23QmUPAJLcGVGP_-8DgugEuA",
          description: "SSU win against Corvadae at AEM Sydney 2018",
          url: "/news"
        },
        {
          category: "esports",
          title: "SSU Esports win AEM Perth",
          image: "https://drive.google.com/uc?export=download&id=1ubG3aVFuznne_l3CiQat2huV9cBGRfU5",
          description: "SSU win against Corvadae at AEM Sydney 2018",
          url: "/news"
        },
        {
          category: "esports",
          title: "SSU Esports win AEM Melbourne",
          image: "https://drive.google.com/uc?export=download&id=0B1gtNUDwB5fSOWcyd25WQTNaVVU",
          description: "SSU win against Corvadae at AEM Sydney 2018",
          url: "/news"
        },
        {
          category: "esports",
          title: "SSU Esports win AEM Brisbane",
          image: "https://drive.google.com/uc?export=download&id=1TUbSJdcWbq9acGp3M1dYdfJqtmMZMDG0",
          description: "SSU win against Corvadae at AEM Sydney 2018",
          url: "/news"
        }
      ]
    };
  }
};
</script>

<style scoped>
@media only screen and (max-width: 420px) {
    .logo {
    width: 70px;
    height: 70px;
    margin-bottom: 35px;
}

.slide-container {
    display: flex;
    width: 100%;
    flex-direction: column;
    align-items: baseline;
    color: white;
    position: absolute;
    bottom: 40px;
    padding: 20px;
    

  }

  .slide-container a {
      color: white;
      text-transform: capitalize;
      background-color: #ce922a;
      padding: 5px 25px;
      border-radius: 5px;
      margin: 10px 0;
      border: solid 0px;
      text-decoration: none;
      font-weight: bold;
      transition: ease 0.5s;
      
  }

  .slide-container a:hover {
      color: #ce922a;
      background-color: white;
      transition: ease 0.5s;
  }

  .slide-container h2 {
      color: white;
      text-transform: capitalize;
      font-weight: bold;
      font-size: 30px;
  }

  .slide-container h3 {
      color: white;
      text-transform: uppercase;
      font-weight: 300;
      
  }

  .slider > img {
      height: 500px;
      width: 100%;
      position: absolute;
      z-index: -1;
      object-fit: cover;
      filter: brightness(0.5);
  }

  .wrapper {
    display: flex;
    margin-top: 50px;
    width: 100%;
    align-self: center;
    
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
    font-size: 0px;
}

  .slider {
      position: relative;
    width: 100%;
    height: 500px;
  }

.fade {
    animation: fade 2s ease;
}

@keyframes fade {
    from {
        opacity: 0%;
    }
    to {
        opacity: 100%;
    }
}

}

@media only screen and (min-width: 421px) {

.logo {
    width: 70px;
    height: 70px;
    margin-bottom: 35px;
}

.wrapper {
    display: flex;
    margin-top: 50px;
}

.wrapper div {
    width: 150px;
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
    flex-direction: column;
    align-items: baseline;
    width: 1000px;
    margin: auto;

  }

  .slider > img {
      position: absolute;
      top: 0;
      left: 0;
      filter: brightness(0.5);
        height: 500px;
        width: 100%;
      object-fit: cover;
      z-index: -1;  
  }

  .slider > img::before {
      background: linear-gradient(to right, rgba(0,0,0,0), rgba(0,0,0,1));
      content: '';
  }


    .slide-container a {
      color: white;
      text-transform: capitalize;
      background-color: #ce922a;
      padding: 10px 50px;
      border-radius: 5px;
      margin: 10px 0;
      border: solid 0px;
      text-decoration: none;
      font-weight: bold;
      transition: ease 0.5s;
      
  }

  .slide-container a:hover {
      color: #ce922a;
      background-color: white;
      transition: ease 0.5s;
  }

  .slide-container h2 {
      color: white;
      text-transform: capitalize;
      font-weight: bold;
      font-size: 30px;
  }

  .slide-container h3 {
      color: white;
      text-transform: uppercase;
      font-weight: 300;
      
  }

  .slider {
      position: relative;
    width: 100%;
    height: 500px;
    display: flex;
  }

.fade {
    animation: fade 2s ease;
}

@keyframes fade {
    from {
        opacity: 0%;
    }
    to {
        opacity: 100%;
    }
}

}
</style>