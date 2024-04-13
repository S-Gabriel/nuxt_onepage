<template>
    <div class="main-container">
        <HeaderBlack @togglenav="navOpen = !navOpen" @toggleSearch="searchOpen = !searchOpen" :isMobile="isMobile()"/>
        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
        <HeroStartUp :isMobile="isMobile()"/>
        <MusicianIconBox/>
        <FeatureStartUp :isMobile="isMobile()"/>
        <ContactUs/>
        <!-- <EffectiveSolution /> -->
        <!-- <StartUpStratagy /> -->
        <!-- <PortfolioItemFilter /> -->
        <!-- <NewsletterCta /> -->
        <!-- <FooterTwo /> -->
    </div>
</template>


<script>
    import HeaderBlack from "@/components/HeaderBlack.vue"
    import HeroStartUp from "@/components/HeroStartUp.vue"

    import FeatureStartUp from "@/components/FeatureStartUp.vue"
    import WhatWeDo from "@/components/WhatWeDo.vue"
    import MusicianIconBox from "@/components/MusicianIconBox.vue"
    import ContactUs from "@/components/ContactUs.vue"
    // import StartUpStratagy from "@/components/sections/StartUpStratagy"
    // import PortfolioItemFilter from "@/components/sections/PortfolioItemFilter"

    export default {
        components: {
            HeaderBlack,
            // FeatureStartUp,
            // StartUpStratagy,
            // PortfolioItemFilter
        },

        data() {
            return {
                width: document.documentElement.clientWidth,
                height: document.documentElement.clientHeight,
                navOpen: false,
                searchOpen: false
            }
        },
        methods: {
            isMobile() {
                this.width = document.documentElement.clientWidth;
                this.height = document.documentElement.clientHeight;

                if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
                    return true;
                } else if (this.width < 1200) {
                    return true;
                } else {
                    return false;
                }
            }
        },
        mounted () {
            window.addEventListener('resize', this.isMobile);
            document.body.classList.add('template-color-5', 'template-font-1', 'bg_color--16')
        },
        unmounted() {
            window.removeEventListener('resize', this.isMobile);
        },
    };
</script>


<style lang="scss">
    body {
        color: $body-color;
        font-weight: 500;
    }


</style>
