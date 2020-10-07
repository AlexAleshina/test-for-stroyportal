<template>
<nav>
    <div class="geo">
        <img alt="geo" src="../assets/geo.svg" class="img-geo">
        <span class="geo-text">Волгоградская область</span>
    </div>
    <div class="menu">
        <span class="menu-item">Тендеры</span>
        <span class="menu-item">База подрядчиков</span>
        <span class="menu-item">Другие сервисы</span>
        <img class="menu-img" alt="arrowdown.svg" src="../assets/arrowdown.svg">
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
@media (min-width: 1080px) and (max-width: 12450px) {
    nav {
        padding-right: 57px;
        height: 32px;

        .geo {
            margin-left: 87px;
        }

        .menu {
            .menu-item {
                margin: 12px;
            }
        }
    }
}

@media (min-width: 500px) and (max-width: 1080px) {
    nav {
        height: 32px;

        .geo {
            margin-left: 20px;
        }

        .menu {
            margin-right: 20px;
        }
    }
}

@media (max-width: 500px) {
    nav {
        .geo {
            margin-left: 20px;

            .geo-text {
                margin-right: 10px;
            }
        }

        .menu {
            margin-right: 20px;
            display: flex;
            flex-direction: column;

            img {
                display: none;
            }
        }
    }
}

nav {
    background-color: #FAFBFC;
    font-size: 12px;
    color: #708598;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .geo {
        display: flex;
        align-items: center;

        img {
            width: 12px;
            padding-right: 8px;
        }
    }

    .menu {

        .menu-item {
            margin: 5px;
        }

        .menu-img {
            width: 9px;
            height: 9px;
        }

        .menu-item:hover {
            color: #000;
        }
    }
}
</style>
