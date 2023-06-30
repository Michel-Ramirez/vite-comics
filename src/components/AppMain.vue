<script>
</script>

<template>
    <div class="main-content">
        <div class="wrapper">
            <h1> --- Content goes here --- </h1>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/vars' as *;

.main-content {
    height: 150px;
    background-color: $black;
}

h1 {
    color: $white;
}

.wrapper {
    display: flex;
    height: 100%;
    align-items: center;
}
</style>