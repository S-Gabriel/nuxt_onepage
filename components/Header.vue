<template>
    <header class="br_header header-default black-logo--version haeder-fixed-width header-mega-menu clearfix" :class="{'vue-fixed-header--isFixed': isSticky}">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <div class="header__wrapper mr--0">
                        <div class="flex-20 header-left">
                            <nuxt-link to="/">
                                <img src="/img/logo/brook-black.png" alt="Brook Logo" class="w-50">
                                <h5 v-if="!isMobile" class="heading heading-h5 font-20 text-purple mt-2 pb-2">
                                    <span class="fa fa-heart"></span>
                                    Hello, we are brook studio
                                </h5>
                            </nuxt-link>
                        </div>
                        <div class="mainmenu-wrapper d-none d-lg-block">
                            <Navigation />
                        </div>
                        <div class="header-right">
                            <div class="d-flex align-items-center justify-content-end">
                                <div class="d-flex contact-us py-1">
                                    <a class="brook-btn bk-btn-gradient-pink btn-rounded space-between"
                                        :class="isMobile ? 'btn-xs-size' : 'btn-sd-size'"
                                        href="#contactUs">
                                        Contact Us
                                    </a>
                                </div>
                            </div>
                            <div class="manu-hamber popup-mobile-click d-block d-lg-none black-version d-block d-xl-none" @click="$emit('togglenav')">
                                <div>
                                    <i></i>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    import Navigation from '@/components/Navigation.vue';

    export default {
        components: {
            Navigation
        },
        props: ['addClass', 'isMobile'],
        data(){
            return {
                isSticky: false,
            }
        },
        mounted(){
            window.addEventListener('scroll', () => {
                let scrollPos = window.scrollY
                if(scrollPos >= 200){
                    this.isSticky = true
                } else {
                    this.isSticky = false
                }
            })
        },
    };
</script>

<style lang="scss" scoped>
    .vue-fixed-header--isFixed {
        top: 0;
        left: 0;
        width: 100%;
        z-index: 999;
        position: fixed !important;
        background-color: #fff;
        box-shadow: 0 0 8px 1px rgba(0, 0, 0, 0.2);
        animation: 900ms cubic-bezier(0.2, 1, 0.22, 1) 0s normal none 1 running fadeInDown;
    }
    .header-default {
        top: 0;
        left: 0;
        width: 100%;
        z-index: 999;
        position: fixed;
    }

</style>
