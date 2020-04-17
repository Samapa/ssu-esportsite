<template>
  <div>
    <Header></Header>
    <Slider id="news"></Slider>
    
      <TitleBlock>Matches</TitleBlock>
      <Matches></Matches>
      
      <Players id="team" style="margin-top: 40px"></Players>
      <TitleBlock id="content">Content</TitleBlock>
      <Content></Content>
      <Sponsors id="sponsors"></Sponsors>
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
import Header from '~/components/Header.vue'

export default {
  components: {
    Logo,
    Slider,
    TitleBlock,
    Matches,
    Players,
    Content,
    Sponsors,
    SiteFooter,
    Header
  }
}
</script>

<style>

</style>
