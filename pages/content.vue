<template>
    <div>
        <Header></Header>
        <img src="img/banner-02.png" class="banner" alt="banner"/>
        <TitleBlock style="padding-top: 50px">Content</TitleBlock>
        <Content></Content>

        <Sponsors style="margin-top: 40px"></Sponsors>
        <SiteFooter></SiteFooter>
    </div>
</template>
<script>
import Header from '~/components/Header.vue'
import Content from '~/components/Content.vue'
import Sponsors from '~/components/Sponsors.vue'
import SiteFooter from '~/components/SiteFooter.vue'
import TitleBlock from '~/components/Title.vue'

export default {
    components: {
        Header,
        Content,
        Sponsors,
        SiteFooter,
        TitleBlock
    }
}
</script>
<style scoped>

.container {
    margin: auto;
}

div {
    padding: 0;
    margin: 0;
}

.slider {
    margin-top: 0;
}

@media only screen and (max-width: 420px) {
  .container {
    padding: 20px;
  }

}


</style>