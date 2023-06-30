<script>
export default {
    data() {
        return {
            items: [
                {
                    text: 'DIGITAL COMICS',
                    url: '#',
                    img: '/img/buy-comics-digital-comics.png',
                },
                {
                    text: 'DC MERCHANDISE',
                    url: '#',
                    img: '/img/buy-comics-merchandise.png',
                },
                {
                    text: 'SUBSCRIPTION',
                    url: '#',
                    img: '/img/buy-comics-shop-locator.png',
                },
                {
                    text: 'COMICS SHOP LACATOR',
                    url: '#',
                    img: '/img/buy-comics-subscriptions.png',
                },
                {
                    text: 'DC POWER VISA',
                    url: '#',
                    img: '/img/buy-dc-power-visa.svg',
                },
            ]
        }
    }
}
</script>

<template>
    <div class="head-footer">
        <ul class="wrapper">
            <li v-for="item in items">
                <img :src="item.img" :alt="item.text">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
.head-footer {
    height: 150px;
    background-color: #0282F9;
}

img {
    height: 50px;
    padding-right: 10px;
}

ul li:last-child img {
    height: 40px;
}

li a {
    color: white;
}

ul {
    display: flex;
    height: 100%;
    justify-content: space-between;
    align-items: center;
    padding-inline-start: 0;
}
</style>