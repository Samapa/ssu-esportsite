<template>
  <div>
    
    <Slider></Slider>
    <div class="container">
      <TitleBlock>Matches</TitleBlock>
      <Matches></Matches>
      <TitleBlock>Players</TitleBlock>
      <TitleBlock>Content</TitleBlock>
    </div>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Slider from '~/components/Slider.vue'
import TitleBlock from '~/components/Title.vue'
import Matches from '~/components/Matches.vue'

export default {
  components: {
    Logo,
    Slider,
    TitleBlock,
    Matches
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
