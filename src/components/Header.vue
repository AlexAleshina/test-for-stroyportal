<template>
<div>
    <div class="main">
        <img alt="logo" src="../assets/logo.svg" class="logo">
        <div class="catalog">
            <img src="../assets/menu.svg" alt="menu-catalog">
            <span>Каталог</span>
        </div>
        <div>
            <!--<input type="text" placeholder="Хочу найти...">-->
            <autocomplete :search="search" base-class="search" placeholder="Хочу найти..."></autocomplete>
        </div>
        <div class="list">
            <img src="../assets/list.png" alt="list">
            <span>Список</span>
        </div>
        <div class="round">A</div>
    </div>
</div>
</template>

<script>
import countries from './countries.json'
export default {
    name: 'Header',
    methods: {
        search(input) {
            if (input.length < 1) {
                return []
            }
            return countries.filter(country => {
                return country.toLowerCase()
                    .startsWith(input.toLowerCase())
            })
        }
    }
}
</script>

<style lang="scss">

.main {
    @import 'search-style.scss';

    display: flex;
    border-bottom: 1px solid #ECEFF1;
    padding-right: 57px;
    display: flex;
    justify-content: center;
    padding-top: 18px;
    padding-bottom: 18px;

    .logo {
        width: 170px;
        margin-left: 87px;
    }

    .catalog {
        min-width: 116px;
        height: 40px;
        background-color: #FED83D;
        border-radius: 4px;
        margin-left: 12px;
        margin-right: 12px;
        display: flex;
        align-items: center;
        justify-content: center;

        span {
            color: #050F19;
            font-weight: 600;
            font-size: 14px;
        }

        img {
            width: 15px;
            height: 10px;
            padding-right: 10.5px;
        }

    }

    .catalog:hover {
        background-color: #FED10D;
    }

    .list {
        min-width: 106px;
        height: 35px;
        border: 1px solid #ECEFF1;
        border-radius: 4px;
        background-color: #FAFBFC;
        color: #050F19;
        font-size: 14px;
        font-weight: 600;
        margin-left: 12px;
        margin-right: 12px;
        display: flex;
        align-items: center;
        justify-content: center;

        img {
            width: 16px;
            height: 20px;
            padding-right: 12px;
        }
    }

    .list:hover {
        background-color: #FAFBB9;
    }

    .round {
        background-color: #9B51E0;
        border-radius: 50%;
        min-width: 40px;
        height: 40px;
        color: #FFFFFF;
        text-align: center;
        line-height: 40px;
        margin-left: 12px;
        margin-right: 12px;
    }

    .round:hover {
        background-color: #9B71E0;
    }
}
</style>
