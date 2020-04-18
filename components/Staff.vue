<template>
    <div>
        <div class="container flex">
            <div class="staffTile" v-for="(staffMember, index) in staff" :key="index" :style="{backgroundImage: `url('${staffMember.image}')`}">
               <div class="staffInfo">
                    <h3>{{staffMember.role}}</h3>
                    <p>{{staffMember.name}}</p>
                    <a :href="staffMember.steam" target="_blank">
                        <img src="img/SteamLogo-01.svg" alt="Steam Logo" />
                    </a>
                    <a :href="staffMember.twitter" target="_blank">
                        <img src="img/TwitterLogo-01.svg" alt="Twitter Logo" />
                    </a>
                    <a :href="staffMember.youtube" target="_blank">
                        <img src="img/YouTubeLogo-01.svg" alt="YouTube Logo" />
                    </a>
                    <a :href="'mailto:' + staffMember.email" target="_blank">
                        <img src="img/EmailIcon-01.svg" alt="Email Logo" />
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            staff: [
                {
                    name: 'Samuel Palmer',
                    role: 'Owner',
                    ign: 'Samapa',
                    steam: 'https://steamcommunity.com/id/Samapa',
                    email: 'samuel@samuelpalmer.info',
                    image: 'img/staffplaceholder-01.svg',
                    twitter: 'https://twitter.com/EsSamapa',
                    youtube: 'https://www.youtube.com/channel/UCU-3JxNP3xHtFP-fRsXPWOg'
                }
            ]
        }
    }
}
</script>

<style scoped>
.staffTile {
        flex: 1;
        max-width: 33%;
        flex-direction: column;
        min-height: 450px;
        border-radius: 10px;
        overflow: hidden;
        background-size: cover;
        background-position: center center;
        display: flex;
        justify-content: space-between;
        transition: ease 0.2s;
        transform: translateY(0px);
    }

     .staffTile:hover {
        transform: translateY(4px);
        transition: ease 0.2s;
    }

    .staffTile:not(:last-of-type) {
        margin-right: 20px;
    }

     .staffTile h3 {
        padding: 20px 20px 0 0;
        color: white;
        text-transform: uppercase;
    }

    .staffTile p {
        text-transform: uppercase;
        color: white;

    }

    .staffTile p:last-of-type {
        padding-bottom: 20px;
    }

    .staffTile .staffInfo a {
        color: white;
        text-transform: uppercase;
        text-decoration: none;
    }

    .staffTile img {
        width: 35px;
    }
    
    .staffInfo {
        padding: 20px
    }

@media only screen and (max-width: 420px) { 
        .flex {
            flex-direction: column;
        }

        .staffTile {
            max-width: 100%;
            margin-bottom: 20px;
        }

        .staffTile:not(:last-of-type) {
        margin-right: 0px;
    }
    }

</style>