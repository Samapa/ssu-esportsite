<template>
    <div>
        <Header></Header>
        <Sponsors style="padding-top: 40px"></Sponsors>
        <SiteFooter class="footerSticky"></SiteFooter>
    </div>
</template>
<script>
import Header from '~/components/Header.vue'
import Sponsors from '~/components/Sponsors.vue'
import SiteFooter from '~/components/SiteFooter.vue'

export default {
    components: {
        Header,
        Sponsors,
        SiteFooter,
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