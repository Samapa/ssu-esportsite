<template>
  <div>
      <div class="mobileTop">
        <a id="mobileLogo">
            <img src="img/logoMobile.svg" alt="SSU Logo" />
        </a>
        <a id="open">
            <img src="img/open.svg" alt="Open Icon" v-on:click="active = false" />
        </a>
      </div>
    <div class="SiteNav" :class="{hidden: active}">
      <ul class="NavContainer">
        <li class="logoNav">
          <div>
            <a href="#" id="logoImage">
              <img src="img/logo.svg" alt="SSU Logo" />
            </a>
            <a id="close">
              <img src="img/close.svg" alt="Close Icon" v-on:click="active = true" />
            </a>
          </div>
        </li>
        <li>
          <a href="#team">Team</a>
        </li>
        <li>
          <a href="#news">News</a>
        </li>
        <li >
          <a href="#content">Content</a>
        </li>
        <li>
          <a>Staff</a>
        </li>
        <li>
          <a href="#sponsors">Sponsors</a>
        </li>
        <li>
          <div class="socials">
            <a href="https://www.facebook.com/SSUORGANISATION" target="_blank">
              <img src="img/Facebook-01.svg" alt="Facebook Logo" id="SocialIcon" />
            </a>
            <a href="https://twitter.com/SSUORGANISATION" target="_blank">
              <img src="img/Twitter-01.svg" alt="Twitter Logo" id="SocialIcon" />
            </a>
            <a href="https://www.youtube.com/channel/UCjaAz0tgJk_Q3_VTvr7XddQ" target="_blank">
              <img src="img/Youtube-01.svg" alt="Youtube Logo" id="SocialIcon" />
            </a>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
   data() {
       return{
           active: true
       }
   }
}
</script>

<style scoped>
#SocialIcon {
  width: 20px;
}

@media only screen and (max-width: 420px) {
  .logoNav img {
    width: 40px;
  }

  #logoImage {
    display: none;
  }

  #mobileLogo {
      position: fixed;
      left: 0;
      width: 30px;
      margin: 15px;
  }

  .mobileTop {
      position: fixed;
      top: 0;
      width: 100%;
      height: 60px;
      background-color: #011321;
      z-index: 2;
  }

  #open {
      position: fixed;
      right: 0;
      width: 30px;
      margin: 15px;
  }

  

  #close {
    align-self: flex-end;
  }

  .SiteNav {
    background: #011321;
    position: fixed;
    width: 75%;
    height: 100%;
    z-index: 2;
    right: 0;
    transform: translateX(0px);
    transition: ease-in 0.3s;
  }

  .hidden {
    transform: translateX(500px);
    transition: ease-in 0.6s;
  }

  .NavContainer {
    flex-direction: column;
    display: flex;
    padding: 0;
  }

  ul {
    list-style: none;
  }

  ul li {
    border-bottom: solid 1px #ce922a;
    padding: 15px;
  }

  ul li > a {
    color: #fff;
    display: inline-block;
    text-transform: uppercase;
    font-size: 14px;
    text-decoration: none;
  }
}

@media only screen and (min-width: 421px) {

    .mobileTop {
        display: none;
    }

  .SiteNav {
    background: #011321;
    position: fixed;
    width: 100%;
    z-index: 2;
  }

  #close {
    display: none;
  }

  .socials img {
    width: 40px;
  }

  .NavContainer {
    width: 1000px;
    margin: auto;
    flex-direction: row;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0;
  }

  ul {
    list-style: none;
  }

  .logoNav img {
    width: 40px;
  }

  .logoNav {
    background-color: var(--highlight-one);
    padding: 15px;
  }

  ul li > a {
    color: white;
    padding: 26px;
    display: inline-block;
    text-transform: uppercase;
    font-size: 14px;
    transition: ease 0.2s;
    transform: translateY(0px);
    text-decoration: none;
  }

  ul li > a:hover {
    background-color: white;
    color: #011321;
    box-shadow: inset 0px 4px #ce922a;
    cursor: pointer;
    transition: ease 0.5s;
    transform: translateY(5px);
  }
}
</style>