<script>
import footerTop from './footerTop.vue';
import footerBottom from './footerBottom.vue';
export default {
    data() {
        return {
            linksComics: [
                {
                    text: 'Characters',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    visited: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'News',
                    url: '#',
                    visited: false,
                },

            ],
            linksShop: [
                {
                    text: 'Shop DC',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#',
                    visited: false,
                },
            ],
            linksDC: [
                {
                    text: 'Terms Of Use',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Ad Choices',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Advertising',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Jobs',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Subscritions',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Talent Workshops',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'CPSC Certificates',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Ratings',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Shop Help',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'Contact Us',
                    url: '#',
                    visited: false,
                },
            ],
            linksSite: [
                {
                    text: 'DC',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'MAD Magazine',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'DC Kids',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'DC universe',
                    url: '#',
                    visited: false,
                },
                {
                    text: 'DC Power Visa',
                    url: '#',
                    visited: false,
                },
            ]
        }
    },
    components: {
        footerBottom,
        footerTop,
    }
}
</script>

<template>
    <footer>
        <footerTop />
        <div class="main-footer">
            <div class="wrapper">
                <div class="nav-site">
                    <div class="wrapper-col">
                        <div class="col-left">
                            <h4>DC COMICS</h4>
                            <ul>
                                <li v-for="link in linksComics">
                                    <a :href="link.url" :class="{ visited: link.visited }"> {{ link.text }}</a>
                                </li>
                            </ul>

                            <h4>SHOP</h4>
                            <ul>
                                <li v-for="link in linksShop" :class="{ visited: visited }">
                                    <a :href="link.url" :class="{ visited: visited }">{{ link.text }}</a>
                                </li>
                            </ul>
                        </div>
                        <div class="col-center">
                            <h4>DC</h4>
                            <ul>
                                <li v-for="link in linksDC">
                                    <a :href="link.url" :class="{ visited: visited }">{{ link.text }}</a>
                                </li>
                            </ul>
                        </div>
                        <div class="col-right">
                            <h4>SITE</h4>
                            <ul>
                                <li v-for="link in linksSite">
                                    <a :href="link.url" :class="{ visited: visited }">{{ link.text }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="logo-bg"></div>
            </div>
        </div>
        <footerBottom />
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/vars' as *;


.main-footer {
    height: 500px;
    background-image: url('/img/footer-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;
}

.wrapper {
    display: flex;
    justify-content: space-between;
    height: 100%;
}

.wrapper-col {
    display: flex;
}

.nav-site {
    height: 100%;
    width: 40%;
    display: flex;
    align-items: center;
}

.logo-bg {
    width: 60%;
    background-image: url('/img/dc-logo-bg.png');
    background-repeat: no-repeat;
    background-position: left;
    background-size: cover;
}

.col-center {
    margin: 0 30px;
}

h4 {
    color: $white;
    font-size: 1.2rem;
}

ul {
    padding-inline-start: 0;
}

a {
    color: $gray;
    font-size: 0.8rem;
}

.visited {
    color: $dark-blue;
}
</style>