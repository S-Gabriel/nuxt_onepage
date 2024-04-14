<template>
    <div class="brook-testimonial-area pt--80 pt-md--80 pt-sm--80">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="brook-section-title text-center mb--80 mb_sm--40">
                        <h3 class="heading heading-h3 font-large">What our clients think about us</h3>
                        <div class="thumb mt--35 mt_sm--20">
                            <img src="/img/service/icon-box/wavy-icon.png" alt="Multipurpose">
                        </div>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <div class="brook-element-carousel">
                        <swiper
                            :space-between="30"
                            :speed="1000"
                            :loop="false"
                            :breakpoints="swiperOptions.breakpoints"
                            :pagination="swiperOptions.pagination"
                            :modules="modules"
                            :autoplay="swiperOptions.autoplay"
                        >
                            <swiper-slide class="testimonial testimonial_style--2"
                                v-for="testimonial in data.testimonials" :key="testimonial.id">
                                <TestimonialCard :testimonial="testimonial"/>
                            </swiper-slide>
                        </swiper>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
    import data from '../../data/testimonial.json'
    import { Autoplay } from 'swiper/modules';
    import { Swiper, SwiperSlide } from 'swiper/vue'
    import TestimonialCard from '@/components/TestimonialCard.vue'

    export default {
        components: {
            Swiper,
            SwiperSlide
        },
        data () {
            return {
                swiperOptions: {
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true,
                    },
                    breakpoints: {
                        992:{
                            slidesPerView : 3
                        },
                        768:{
                            slidesPerView : 2
                        },
                        300:{
                            slidesPerView : 1
                        }
                    },
                    autoplay: {
                        delay: 5000,
                        disableOnInteraction: false,
                        pauseOnMouseEnter: true
                    },
                },
                data,
                modules: [ Autoplay],
            }
        }
    }
</script>
