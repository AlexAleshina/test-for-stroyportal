<template>
<nav>
    <div class="geo">
        <img alt="geo" src="../assets/geo.png" class="img-geo">
        <span class="geo-text">Волгоградская область</span>
    </div>
    <div class="menu">
        <span class="menu-item">Тендеры</span>
        <span class="menu-item">База подрядчиков</span>
        <span class="menu-item">Другие сервисы</span>
        <img alt="arrowdown.svg" src="../assets/arrowdown.svg">
    </div>

</nav>
</template>

<script>
export default {
    name: 'Navbar'

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>
nav {
    background-color: #FAFBFC;
    height: 32px;
    font-size: 12px;
    color: #708598;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 57px;

    .geo {
        margin-left: 87px;
        display: flex;
        align-items: center;

        img {
            width: 12px;
            padding-right: 8px;
        }
    }

    .menu {
        .menu-item {
            padding-right: 12px;
        }

        .menu-item:hover {
            color: #000;
        }

        img {
            margin-left: 6.5px;
            width: 18px;
            height: 9px;
        }
    }
}
</style>
