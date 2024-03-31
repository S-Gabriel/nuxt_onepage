<template>
    <div class="main-container">
        <HeaderBlack @togglenav="navOpen = !navOpen" @toggleSearch="searchOpen = !searchOpen" />
        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
        <HeroStartUp />
        <FeatureStartUp />
        <WhatWeDo />
        <EffectiveSolution />
        <StartUpStratagy />
        <PortfolioItemFilter />
        <NewsletterCta />
        <FooterTwo />
    </div>
</template>


<script>
    import HeaderBlack from "@/components/HeaderBlack.vue"
    import HeroStartUp from "@/components/HeroStartUp.vue"

    import FeatureStartUp from "@/components/FeatureStartUp"
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
                navOpen: false,
                searchOpen: false
            }
        },

        mounted () {
            document.body.classList.add('template-color-5', 'template-font-1')
        }
    };
</script>


<style lang="scss">
    body {
        color: $body-color;
        font-weight: 500;
    }


</style>
