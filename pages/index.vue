<template>
  <div>
    
    <Slider></Slider>
    
      <TitleBlock>Matches</TitleBlock>
      <Matches></Matches>
      
      <Players></Players>
      <TitleBlock>Content</TitleBlock>
      <Content></Content>
      <Sponsors></Sponsors>
      <SiteFooter></SiteFooter>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Slider from '~/components/Slider.vue'
import TitleBlock from '~/components/Title.vue'
import Matches from '~/components/Matches.vue'
import Players from '~/components/Players.vue'
import Content from '~/components/Content.vue'
import Sponsors from '~/components/Sponsors.vue'
import SiteFooter from '~/components/SiteFooter.vue'

export default {
  components: {
    Logo,
    Slider,
    TitleBlock,
    Matches,
    Players,
    Content,
    Sponsors,
    SiteFooter
  }
}
</script>

<style>

:root {
  --highlight-one: #ce922a
}

* {
  box-sizing: border-box;
}

body {
  background-color: #f6faf9;
}

.flex {
  display: flex;
}

@media only screen and (max-width: 420px) {
  .container {
    padding: 20px;
  }

}


@media only screen and (min-width: 421px) {
  .container {
    width: 1000px;
    margin:auto;
  }

}

</style>
