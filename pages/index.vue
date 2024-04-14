<template>
    <div class="main-container">
        <Header @togglenav="navOpen = !navOpen" @toggleSearch="searchOpen = !searchOpen" :isMobile="isMobile()"/>
        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
        <Banner :isMobile="isMobile()"/>
        <OurMission/>
        <FeatureStartUp :isMobile="isMobile()"/>
        <Portfolio addClass="ptb-md--80 ptb-sm--80 poss_relative"/>
        <ContactUs/>
        <!-- <EffectiveSolution /> -->
        <!-- <StartUpStratagy /> -->
        <!-- <PortfolioItemFilter /> -->
        <!-- <NewsletterCta /> -->
        <!-- <FooterTwo /> -->
    </div>
</template>


<script>
    import Header from "@/components/Header.vue"
    import OffCanvasMobileMenu from "~/components/OffCanvasMobileMenu.vue"
    import Banner from "@/components/Banner.vue"
    import FeatureStartUp from "@/components/FeatureStartUp.vue"
    import OurMission from "@/components/OurMission.vue"
    import ContactUs from "@/components/ContactUs.vue"
    import Portfolio from "@/components/Portfolio.vue"
    // import StartUpStratagy from "@/components/sections/StartUpStratagy"
    // import PortfolioItemFilter from "@/components/sections/PortfolioItemFilter"

    export default {
        components: {
            Header,
            OffCanvasMobileMenu,
            Banner,
            OurMission,
            FeatureStartUp,
            Portfolio,
            ContactUs,
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
            document.body.classList.add('template-font-1', 'bg_color--16')
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
