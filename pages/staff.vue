<template>
    <div>
        <Header></Header>
        <img src="img/banner-03.png" class="banner" alt="banner"/>
        <TitleBlock>Staff</TitleBlock>
        <Staff></Staff>
        <Sponsors style="margin-top: 40px;"></Sponsors>
        <SiteFooter></SiteFooter>
    </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Sponsors from '~/components/Sponsors.vue'
import SiteFooter from '~/components/SiteFooter.vue'
import Staff from '~/components/Staff.vue'
import TitleBlock from '~/components/Title.vue'

export default {
    components: {
        Header,
        Sponsors,
        SiteFooter,
        Staff,
        TitleBlock
    }
    
}
</script>

<style scoped>

</style>