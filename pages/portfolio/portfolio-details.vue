<template>
    <div class="main-container">

        <HeaderBlack @togglenav="navOpen = !navOpen" @toggleSearch="searchOpen = !searchOpen" />

        <OffCanvasMobileMenu :class="{'show-mobile-menu' : navOpen}" @togglenav="navOpen = !navOpen" />

        <SearchPopup :class="{'search-popup-open' : searchOpen}" @toggleSearch="searchOpen = !searchOpen" />

        <div class="brook-portfolio-details bg_color--1">
            <div class="container">
                <div class="row pt--100 pt_md--5 pt_sm--5 pb--80">

                    <!-- Portfolio Left -->
                    <div class="col-lg-4 col-12 order-2 order-lg-1 mt_md--40 mt_sm--40" id="is_stuck_inner">
                        <div class="portfolio-left bk-portfolio-details">
                            <div class="portfolio-main-info">
                                <h3 class="heading heading-h3 line-height-1-42">Smart Sound System</h3>
                                <div class="portfolio-content mt--75 mb--75 mt_md--40 mb_md--40 mt_sm--40 mb_sm--40">
                                    <h6 class="heading heading-h6">ABOUT THE PROJECT</h6>
                                    <div class="desc mt--20">
                                        <p class="bk_pra">Not only are comics available in printed form, but they’re also available digitally. Printed, on the web, or on an app? Where do you start? If you have a hard time choosing what to read and  where to read it, you’re not alone, because the choices are limitless. With print and web and digital options, we now have so many comic books.</p>
                                    </div>
                                </div>
                                <!-- Start Details List -->
                                <div class="portfolio-details-list">
                                    <div class="details-list">
                                        <label>Date</label>
                                        <span>28 Sep 2007</span>
                                    </div>

                                    <div class="details-list">
                                        <label>Client</label>
                                        <span>HighGrove Partners</span>
                                    </div>

                                    <div class="details-list">
                                        <label>Categories</label>
                                        <span>
                                            <nuxt-link to="/">
                                                Digital
                                            </nuxt-link>
                                        </span>
                                    </div>

                                    <div class="details-list">
                                        <label>Awards</label>
                                        <span>2018 Revolution Designs</span>
                                    </div>
                                </div>
                                <!-- End Details List -->
                                <!-- Start Portfolio Share -->
                                <div class="portfolio-share pt--70 pt_md--40 pt_sm--40">
                                    <h6 class="heading heading-h6">SHARE</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- Portfolio Right -->

                    <div class="col-lg-8 col-12 order-1 order-lg-2">
                        <div class="portfolio-right portfolio-details-gallery text-center text-lg-end">
                            <!-- Start Portfolio Image -->
                            <div class="portfolio-image mb--50">
                                <img src="/img/portfolio/big-image/gallery-1.jpg" alt="portfolio">
                            </div>
                            <!-- End Portfolio Image -->

                            <!-- Start Portfolio Image -->
                            <div class="portfolio-image mb--50">
                                <img src="/img/portfolio/big-image/gallery-2.jpg" alt="portfolio">
                            </div>
                            <!-- End Portfolio Image -->
                        </div>
                    </div>
                </div>
            </div>

            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <!-- Portfolio Nav List -->
                        <div class="portfolio-nav-list pt--50 pb--150 pb_md--80 pb_sm--60 pt_md--5 pt_sm--5">
                            <div class="portfolio-page prev">
                                <div class="inner">
                                    <nuxt-link to="/portfolio/portfolio-grid-wide">
                                        <p>Prev</p>
                                        <h3 class="heading heading-h3">Awe-inspiring <br> Projects</h3>
                                    </nuxt-link>
                                </div>
                            </div>
                            <div class="portfolio-page next mt_sm--30">
                                <div class="inner">
                                    <nuxt-link to="/portfolio/portfolio-grid-wide">
                                        <p>Next</p>
                                        <h3 class="heading heading-h3">B-sharp High-end <br> Audio</h3>
                                    </nuxt-link>
                                </div>
                            </div>
                        </div>
                        <!-- Portfolio Nav List -->
                    </div>
                </div>
            </div>
        </div>

        <FooterTwo />

    </div>
</template>

<script>
    import data from '../../data/portfolio.json';

    export default {
        components: {
            HeaderBlack: () => import('@/components/HeaderBlack'),
            OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
            SearchPopup: () => import('@/components/SearchPopup'),
            FooterTwo: () => import('@/components/FooterTwo'),
        },
        
        data () {
            return {
                data,
                navOpen: false,
                searchOpen: false,
            }
        },

        mounted () {
            document.body.classList.add('template-color-1', 'template-font-1')
        },

        head() {
            return {
                title: 'Portfolio Details'
            }
        },
    };
</script>