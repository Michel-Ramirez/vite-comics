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
    <footer>
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
    </footer>
</template>

<style lang="scss" scoped>
footer {
    height: 100px;
    background-color: #303030;
}

.wrapper {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

button {
    padding: 10px;
    border: 1px solid #0282F9;
    background-color: #303030;
    color: white;
}

.socials span {
    font-size: 1.5rem;
    color: #0282F9;
}

.socials,
ul {
    display: flex;
}

li {
    margin: 0 10px;
}
</style>