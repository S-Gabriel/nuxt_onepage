<template>
    <div class="bk-portfolio-with-caption-area" :class="addClass">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="brook-section-title text-center pt--60 mb--60">
                        <h3 class="h3 theme-color">PORTFOLIOS</h3>
                        <div class="bkseparator--40"></div>
                        <h1 class="h1 theme-color-2">Collection of the greatest works.</h1>
                    </div>
                </div>
            </div>
            <div class="row mtn--30">
                <div class="col-lg-4 col-sm-6 mt--30 h-40" v-for="portfolio in data.portfolioItems.slice(0, 3)" :key="portfolio.id">
                    <PortfolioItemCaptionBottom :portfolio="portfolio" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import data from '../../data/portfolio.json'
    import PortfolioItemCaptionBottom from '@/components/PortfolioItemCaptionBottom.vue'

    export default {
        props: ["addClass",],

        components: {
            PortfolioItemCaptionBottom,
        },

        data () {
            return {
                data
            }
        }
    };
</script>
