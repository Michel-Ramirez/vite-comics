<script>
export default {
    data() {
        return {
            items: [
                {
                    text: 'Facebook',
                    url: '#',
                    img: '/img/footer-facebook.png',
                },
                {
                    text: 'Periscope',
                    url: '#',
                    img: '/img/footer-periscope.png',
                },
                {
                    text: 'Pinterest',
                    url: '#',
                    img: '/img/footer-pinterest.png',
                },
                {
                    text: 'Twitter',
                    url: '#',
                    img: '/img/footer-twitter.png',
                },
                {
                    text: 'Youtube',
                    url: '#',
                    img: '/img/footer-youtube.png',
                },
            ]
        }
    }
}
</script>

<template>
    <div class="bottom-footer">
        <div class="wrapper">
            <button>SING-UP NOW!</button>
            <div class="socials">
                <span>FOLLOW US</span>
                <ul>
                    <li v-for="item in items">
                        <a :href="item.url">
                            <img :src="item.img" :alt="item.text">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/vars' as *;

.bottom-footer {
    height: 100px;
    background-color: $deep-gray;
}

.wrapper {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

button {
    padding: 10px;
    border: 1px solid $light-blue;
    background-color: $deep-gray;
    color: $white;
}

.socials span {
    font-size: 1.5rem;
    color: $light-blue;
}

.socials,
ul {
    display: flex;
}

li {
    margin: 0 10px;
}
</style>