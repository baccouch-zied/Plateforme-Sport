<template>
    <div class="flexableimage__wrapper">
        <swiper
            :speed="1000"
            :loop="true"
            :space-between="30"
            :navigation="swiperOptions.navigation"
            :breakpoints="swiperOptions.breakpoints"
        >
            <swiper-slide v-for="slide in sliders" :key="slide.id">
                <div class="flexale-image">
                    <div class="thumb">
                        <img :src="slide.image" alt="image">
                    </div>
                </div>
            </swiper-slide>
        </swiper>

        <!-- Add Arrows -->
        <button class="swiper-btn swiper-btn-prev">
            <i class="fas fa-angle-left"></i>
        </button>
        <button class="swiper-btn swiper-btn-next">
            <i class="fas fa-angle-right"></i>
        </button>
    </div>
</template>

<script>
    import SwiperCore, { Navigation } from 'swiper/core'
    import { Swiper, SwiperSlide } from 'swiper/vue'
    SwiperCore.use([Navigation])

    export default {
        components: {
            Swiper,
            SwiperSlide
        },
        data () {
            return {
                swiperOptions: {
                    navigation: {
                        nextEl: '.swiper-btn-next',
                        prevEl: '.swiper-btn-prev'
                    },
                    // Responsive breakpoints
                    breakpoints: {
                        992:{
                            slidesPerView: 2,
                            centeredSlides: true,
                        },

                        768:{
                            centeredSlides: false,
                        },

                        576:{
                            slidesPerView : 2,
                            centeredSlides: false,
                        },
                        300:{
                            slidesPerView : 1,
                            centeredSlides: false,
                        }
                    }
                },
                sliders: [
                    {
                        id: 1,
                        image: "/img/flexable-image-slide/flexale-1/flexable-lg--image-1.jpg"
                    },
                    {
                        id: 2,
                        image: "/img/flexable-image-slide/flexale-1/flexable-lg--image-2.jpg"
                    },
                    {
                        id: 3,
                        image: "/img/flexable-image-slide/flexale-1/flexable-lg--image-3.jpg"
                    },
                    {
                        id: 4,
                        image: "/img/flexable-image-slide/flexale-1/flexable-lg--image-4.jpg"
                    },
                    {
                        id: 5,
                        image: "/img/flexable-image-slide/flexale-1/flexable-lg--image-5.jpg"
                    }
                ]
            }
        }
    };
</script>