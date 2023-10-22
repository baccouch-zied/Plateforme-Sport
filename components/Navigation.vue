<template>
    <nav class="page_nav">
        <ul class="mainmenu">
            <li class="lavel-1 with--drop slide--megamenu">
                <nuxt-link to="/">
                    <span>Accueil</span>
                </nuxt-link>
            </li>

            <li class="lavel-1 with--drop slide--megamenu">
                <nuxt-link to="/a-propos">
                    <span>A Propos</span>
                </nuxt-link>
            </li>

            <li class="lavel-1 with--drop slide--megamenu">
                <nuxt-link to="/services">
                    <span>Services</span>
                </nuxt-link>
            </li>

            <li class="lavel-1 with--drop slide--megamenu">
                <nuxt-link to="/abonnement">
                    <span>Abonnement</span>
                </nuxt-link>
            </li>

            <li class="lavel-1 with--drop slide--megamenu">
                <nuxt-link to="/contact">
                    <span>Contact</span>
                </nuxt-link>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
    .mega__list {
        display: flex;
        li {
            flex-basis: 25%;
        }
    }
</style>