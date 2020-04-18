<template>
    <div>
        <Header></Header>
        <img src="img/banner-03.png" class="banner" alt="banner"/>
        <div class="ComingSoon">
            <h2>Coming Soon</h2>
        </div>
        <Sponsors></Sponsors>
        <SiteFooter></SiteFooter>
    </div>
</template>

<script>
import Header from '~/components/Header.vue'
import SiteFooter from '~/components/SiteFooter.vue'
import Sponsors from '~/components/Sponsors.vue'

export default {
    components: {
        Header,
        Sponsors,
        SiteFooter
    }
}
</script>

<style scoped>
    .ComingSoon h2{
        align-self: center;
        font-size: 3em;
    }

    .ComingSoon {
        height: 50vh;
        width: 1000px;
        margin: auto;
        display: flex;
    }

    @media only screen and (max-width: 420px) {
  .ComingSoon {
    width: 100%;
    margin: 0;
    justify-content: space-around;
  }
  .ComingSoon h2{
        align-self: center;
        font-size: 2em;
       
    }
    }
</style>