<template>
    <div class="main-container">
        <Header @togglenav="navOpen = !navOpen" @toggleSearch="searchOpen = !searchOpen" :isMobile="resizeForMobile"/>
        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />
        <Banner :isMobile="resizeForMobile"/>
        <OurMission/>
        <FeatureStartUp :isMobile="resizeForMobile"/>
        <Portfolio addClass="poss_relative"/>
        <CallToAction/>
        <Testimonial/>
        <ContactUs/>
        <Footer/>
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
    import CallToAction from "@/components/CallToAction.vue"
    import Testimonial from "@/components/Testimonial.vue"
    import Footer from "@/components/Footer.vue"
    // import StartUpStratagy from "@/components/sections/StartUpStratagy"
    // import PortfolioItemFilter from "@/components/sections/PortfolioItemFilter"




    export default {
        setup () {
            const navOpen = ref(false)
            const searchOpen = ref(false)
            const resizeForMobile = ref(null)

            onMounted( () => {
                window.addEventListener('resize', isMobile)
                isMobile()
            })
            onUnmounted(() => {
                window.removeEventListener('resize', isMobile)
            })

            const isMobile = () => {
                const width = window.innerWidth

                console.log(width);
                if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
                    resizeForMobile.value = true;
                } else if (width < 1200) {
                    resizeForMobile.value = true;
                } else {
                    resizeForMobile.value = false;
                }
            }

            return {
                navOpen,
                searchOpen,
                resizeForMobile,
            }
        },

    };
</script>


<style lang="scss">
    body {
        color: $body-color;
        font-weight: 500;
    }


</style>index
