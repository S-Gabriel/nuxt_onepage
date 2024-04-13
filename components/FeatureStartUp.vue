<template>
    <div class="brook-service-area  pt-3">
        <div class="row align-items-center gradient-background">
            <div class="col-xl-7">
                <div class="row startupservice-wrapper mtn--40">
                    <div class="col-lg-6 mt--40" v-for="feature in data.features" :key="feature.id">
                        <FeatureItemStyle :feature="feature" />
                    </div>
                </div>
            </div>
            <div v-if="!isMobile" class="col-xl-5 client-succeed d-flex justify-content-center">
                <img src="/img/features_background.png" alt="We help out clients">
            </div>
        </div>
    </div>
</template>

<script>
    import data from '../../data/features.json';
    import FeatureItemStyle from "@/components/FeatureItemStyle.vue"

    export default {
        components: {
            FeatureItemStyle,
        },

        props: ['isMobile'],

        data () {
            return {
                data
            }
        }
    };
</script>

<style lang="scss">
    .gradient-background {
        background: rgb(2,0,36);
        background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(15,6,113,1) 27%, rgba(253,121,112,1) 100%);
    }

    .client-succeed img {
        width: 100%;
        height: 100%;
    }

</style>
