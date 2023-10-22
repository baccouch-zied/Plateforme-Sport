<template>
    <div class="brook-whatdo-area ptb--100 ptb-md--80 ptb-sm--60 bg_color--1">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="bk-title--default text-center">
                        <h6 class="heading heading-h6 theme-color">Ce que nous faisons</h6>
                        <div class="bkseparator--30"></div>
                        <h3 class="heading heading-h3">Votre Chemin Vers la Victoire</h3>
                    </div>
                </div>
            </div>
            <div class="row mt--40">
                <div class="col-lg-6">
                    <div class="video-with-thumb text-center mt--40">
                        <div class="thumb">
                            <img src="/img/about/galaxy.jpg" alt="video images">
                        </div>
                        <client-only>
                            <silent-box :image="videos[0]">
                                <template v-slot:silentbox-item>
                                    <div class="video-btn position--center">
                                        <div class="play__btn">
                                            <div class="video-icon second-icon"></div>
                                        </div>
                                    </div>
                                </template>
                            </silent-box>
                        </client-only>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="radial-progress-single progress-flex mt--40">
                        <div class="contant pl--30 pl_mobile--5">
                            <h5 class="heading heading-h5">Ce quoi ?</h5>
                            <p class="bk_pra mt--30">
Galaxy Talents est une agence spécialisée dans la gestion et la valorisation des potentiels des sportifs professionnels. Nous intégrons une plateforme innovante qui propose des services visant à aider les athlètes à promouvoir et maximiser leurs compétences, à gérer efficacement leur carrière et à faciliter les transferts, le tout avec une remarquable efficacité. Nos clients incluent des athlètes de sports collectifs tels que le football, le handball et le basketball, ainsi que des sports individuels comme le tennis, l'équitation, le cyclisme et la natation. De plus, une partie importante de notre agence se concentre sur l'amélioration de l'image de nos clients et la conclusion de contrats de partenariat avec des sponsors, y compris des marques et des boutiques, afin d'optimiser leurs opportunités.</p>
                        </div>
                    </div>

                    <!-- Start Single Progress -->
                    <div class="radial-progress-single progress-flex mt--40">
                        <div class="contant pl--30 pl_mobile--5">
                            <h5 class="heading heading-h5">Gestion de carrière</h5><br>
                            <h5 class="heading heading-h5">Promotion et visibilité</h5><br>
                            <h5 class="heading heading-h5">Amélioration de l'image de marque</h5>
                        </div>
                    </div>
                    <!-- End Single Progress -->
                    <!-- End Single Progress -->
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                videos: [
                    {
                        src: 'https://www.youtube.com/watch?v=9No-FiEInLA',
                        thumbnail: ""
                    }
                ],
            }
        }
    };
</script>