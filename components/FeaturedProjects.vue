<template>
    <div class="bk-portfolio-area creative-portfolio section-pb-100">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="section-title--between wow move-up">
                        <div class="title">
                            <h3 class="theme-creative"> Athlètes des <span>Sports collectifs</span></h3>
                        </div>
                        <div class="section-btn mt_mobile--30">
                            <nuxt-link to="/" class="button-text">
                                <span>View all projects</span>
                                <i class="fa fa-arrow-right"></i>
                            </nuxt-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="portfolio-wrapper mt--40 wow move-up">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="porfolio-swip-horizontal" style="overflow: hidden;">
                            <swiper
                                :slides-per-view= 'auto'
                                :space-between="30"
                                :speed="1000"
                                :loop="false"
                                :pagination="swiperOptions.pagination"
                            >
                                <swiper-slide class="portfolio portfolio_style--2 mt--30" v-for="portfolio in data.portfolioFeaturd" :key="portfolio.i">
                                    <div class="thumb">
                                        <img :src="portfolio.image" :alt="portfolio.alt">
                                    </div>
                                    <div class="portfolio-overlay"></div>
                                    <div class="port-overlay-info">
                                        <div class="content">
                                            <h3 class="port-title">{{ portfolio.title }}</h3>
                                            <div class="category">{{ portfolio.category }}</div>
                                        </div>
                                    </div>
                                </swiper-slide>
                            </swiper>
                            <!-- Add Pagination -->
                            <div class="swiper-pagination"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import data from '../data/portfolio.json';

    import SwiperCore, { Pagination } from 'swiper/core'
    import { Swiper, SwiperSlide } from 'swiper/vue'
    SwiperCore.use([Pagination])

    export default {
        components: {
            Swiper,
            SwiperSlide
        },
        data () {
            return {
                data,
                swiperOptions: {
                    pagination: {
                        el: '.swiper-pagination',
                        type: 'custom',

                        renderCustom: function (e, t, i) {
                            var a = (100 / i) * t;
                            var n = t.toString(),
                                s = i.toString();
                            return '<div class="fraction"><span class="current">' + (n = n.padStart(2, "0")) + '</span><span class="separator"> / </span><span class="total">' + (s = s.padStart(2, "0")) + "</span></div>" + '<div class="progressbar"><div class="filled" data-width="' + a + '" style="width: ' + a + "%" + ' "></div></div>'
                        },
                    }
                }
            }
        }
    };
</script>