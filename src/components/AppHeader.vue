<script>
export default {
    data() {
        return {
            items: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header class="wrapper">
        <div class="logo">
            <figure>
                <img src="../../public/img/dc-logo.png" alt="Logo DC">
            </figure>
        </div>
        <div class="menu">
            <ul>
                <li v-for="item in   items ">
                    <a :href="item.url" :class="{ active: item.current }">{{ item.text }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 120px;
    width: 100%;
    display: flex;
    justify-content: space-between;
}

figure {
    height: 100%;
    display: flex;
    align-items: center;
}

img {
    height: 70px;
}

ul {
    display: flex;
    height: 100%;
    align-items: center;

    li {
        margin: 0 10px;
        cursor: pointer;
    }
}

a {
    padding: 47px 0;

}

.active {
    border-bottom: 4px solid #0282F9;
}
</style>