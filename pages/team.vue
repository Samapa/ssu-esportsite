<template>
    <div>
        <Header></Header>
        <Players style="padding-top: 40px"></Players>

            <TitleBlock>Matches</TitleBlock>
            <Matches></Matches>

        <Sponsors style="margin-top: 40px"></Sponsors>
        <SiteFooter></SiteFooter>
    </div>
</template>
<script>
import Header from '~/components/Header.vue'
import Players from '~/components/Players.vue'
import Sponsors from '~/components/Sponsors.vue'
import SiteFooter from '~/components/SiteFooter.vue'
import Matches from '~/components/Matches.vue'
import TitleBlock from '~/components/Title.vue'

export default {
    components: {
        Header,
        Players,
        Sponsors,
        SiteFooter,
        Matches,
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