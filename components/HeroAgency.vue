<template>
    <div class="home-creative-agency" :style="{ backgroundImage: `url('/img/slider/agency.jpg')` }">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="hero-content">
                        <div class="video-btn-2">
                            <a href="https://www.youtube.com/watch?v=edWaDpmqjTI" target="_blank">
                                <div class="play__btn">
                                    <div class="icon-gradient color-pink">
                                            <div class="video-icon"></div>
                                    </div>
                                </div>
                            </a>
                        </div>
                        <h1 class="hero-title">Galaxy <span>Talents</span></h1>
                        <img src="/img/slider/wavy-icon.png" alt="wave icon">
                        <h6>Galaxy Agency, un leader dans le monde des agents et des achats de joueurs, unifiant les sports pour le succès.</h6>
                    </div>
                </div>
            </div>
        </div>
        <div class="hero-social">
            <ul class="social-icon icon-border-rounded icon-size-medium social-vertical text-center">
                <li class="facebook">
                    <a href="https://www.facebook.com/" class="link" aria-label="Facebook">
                        <i class="fab fa-facebook"></i>
                    </a>
                </li>
                <li class="twitter">
                    <a href="https://twitter.com/explore" class="link" aria-label="Twitter">
                        <i class="fab fa-twitter"></i>
                    </a>
                </li>
                <li class="instagram">
                    <a href="https://www.instagram.com/" class="link" aria-label="Instagram">
                        <i class="fab fa-instagram"></i>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss">
    .home-creative-agency {
        height: 100vh;
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        display: flex; 
        align-items: center;
        text-align: center;
        // res
        @media #{$sm-layout}{
            height: 600px;
        }
        .hero-title {
            font-size: 120px;
            font-weight: 700;
            color: $white;
            font-family: $secondary-font;
            span {
                font-family: $playfair-font;
                font-style: italic;
            }
            // res
            @media #{$lg-layout}{
                font-size: 80px;
            }
            @media #{$md-layout}{
                font-size: 70px;
            }
            @media #{$sm-layout}{
                font-size: 55px;
            }
            @media #{$large-mobile}{
                font-size: 40px;
            }
        }
        h6 {
            color: $white;
            font-size: 18px;
            font-weight: 600;
            max-width: 570px;
            line-height: 1.6;
            margin: 30px auto 0;
            font-family: $secondary-font !important;
        }
        .hero-mail {
            position: absolute;
            left: 0;
            // res
            @media #{$sm-layout}{
                left: -60px;
            }
            @media #{$small-mobile}{
                display: none;
            }
            span {
                color: $white;
                display: block;
                font-size: 15px;
                font-weight: 500;
                font-family: $secondary-font;
                transform: matrix3d(0, -1, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
            }
        }
        .hero-social {
            position: absolute;
            right: 0;
            // res
            @media #{$small-mobile}{
                display: none;
            }
        }
    }
</style>