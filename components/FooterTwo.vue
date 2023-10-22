<template>
    <footer class="page-footer bg_color--3 pl--150 pr--150 pl_lg--30 pr_lg--30 pl_md--30 pr_md--30 pl_sm--5 pr_sm--5">
        <!-- Start Footer Top Area -->
        <div class="bk-footer-inner pt--150 pb--30 pt_sm--100">
            <div class="container">
                <div class="row">
                    <div class="col-lg-4 col-sm-6">
                        <div class="footer-widget text-var--2">
                            <div class="logo">
                                <nuxt-link to="">
                                    <img src="/img/logo/galaxy-2.png" alt="brand logo">
                                </nuxt-link>
                            </div>
                            <div class="footer-inner">
                                <p>Galaxy Talents, une agence spécialisée dans l'élaboration de carrières sportives, vous offre les moyens de libérer votre plein potentiel et de briller sur la scène sportive mondiale.</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-2 col-sm-6 mt_mobile--40">
                        <div class="footer-widget text-var--2 menu--about">
                            <h2 class="widgettitle">Liens</h2>
                            <div class="footer-menu">
                                <ul class="ft-menu-list bk-hover">
                                    <li>
                                        <nuxt-link to="/about-us-01">A Propos</nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/team-grid">Services</nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/career">Abonnement</nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/services-classic">Contact</nuxt-link>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-3 col-sm-6 mt_md--40 mt_sm--40">
                        <div class="footer-widget text-var--2 menu--contact">
                            <h2 class="widgettitle">Contact</h2>
                            <div class="footer-address">
                                <div class="bk-hover">
                                    <p>Route de djerba Zarzis</p>
                                    <p>
                                        <a href="mailto:info@yourdomain.com">galaxyTalents@gmail.com </a>
                                    </p>
                                    <p>
                                        <a href="tel:0123456789">0123456789</a>
                                    </p>
                                </div>
                                <div class="social-share social--transparent text-white">
                                    <a href="https://www.facebook.com/" target="_blank">
                                        <i class="fab fa-facebook"></i>
                                    </a>
                                    <a href="https://twitter.com/" target="_blank">
                                        <i class="fab fa-twitter"></i>
                                    </a>
                                    <a href="https://www.instagram.com/" target="_blank">
                                        <i class="fab fa-instagram"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-3 col-sm-6 mt_md--40 mt_sm--40">
                        <div class="footer-widget text-var--2 menu--instagram">
                            <h2 class="widgettitle">Instagram</h2>
                            <div class="ft-instagram-list">
                                <div class="instagram-grid-wrap">
                                    <div class="item-grid grid-style--1" v-for="instagram in instagramPosts" :key="instagram.id">
                                        <div class="thumb">
                                            <nuxt-link to="">
                                                <img :src="instagram.image" alt="instagram image">
                                            </nuxt-link>
                                            <div class="item-info">
                                                <div class="inner">
                                                    <nuxt-link to="">
                                                        <i class="fas fa-heart"></i>
                                                        {{ instagram.like }}
                                                    </nuxt-link>
                                                    <nuxt-link to="">
                                                        <i class="fas fa-comment-dots"></i>
                                                        {{ instagram.comment }}
                                                    </nuxt-link>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Start Footer Top Area -->

        <!-- Start Copyright Area -->
        <div class="copyright ptb--50 text-var-2">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-md-8">
                        <div class="copyright-right text-md-end text-center">
                            <p>&copy; 2023 <b>Galaxy Talents</b> Made with <i class="fa fa-heart text-danger"></i> by <a href="https://hasthemes.com/"><b>WxdTechnology</b></a></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- End Copyright Area -->
    </footer>
</template>

<script>
    export default {
        data () {
            return {
                instagramPosts: [
                    {
                        "id": 1,
                        "image": "/img/instagram/instagram-1.jpg",
                        "like": "1K",
                        "comment": "8"
                    },
                    {
                        "id": 2,
                        "image": "/img/instagram/instagram-2.jpg",
                        "like": "6K",
                        "comment": "9"
                    },
                    {
                        "id": 3,
                        "image": "/img/instagram/instagram-3.jpg",
                        "like": "3K",
                        "comment": "4"
                    },
                    {
                        "id": 4,
                        "image": "/img/instagram/instagram-4.jpg",
                        "like": "1K",
                        "comment": "3"
                    },
                    {
                        "id": 5,
                        "image": "/img/instagram/instagram-5.jpg",
                        "like": "2K",
                        "comment": "7"
                    },
                    {
                        "id": 6,
                        "image": "/img/instagram/instagram-6.jpg",
                        "like": "1K",
                        "comment": "8"
                    }
                ]
            }
        }
    };
</script>