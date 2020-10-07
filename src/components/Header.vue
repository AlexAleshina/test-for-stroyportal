<template>
<div>
    <div class="main">
        <img alt="logo" src="../assets/logo.svg" class="logo">
        <div class="catalog">
            <img src="../assets/menu.svg" alt="menu-catalog">
            <span>Каталог</span>
        </div>
        <div>
            <autocomplete :search="search" base-class="search" placeholder="Хочу найти..."></autocomplete>
        </div>
        <div class="list">
            <img src="../assets/list.svg" alt="list">
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
@media (min-width: 1080px) and (max-width: 12450px) {
    .main {
        padding-right: 57px;
        justify-content: space-around;

        .logo {
            width: 200px;
            margin-left: 85px;
        }

        .catalog {
            min-width: 116px;
            height: 40px;
            margin-left: 12px;
            margin-right: 12px;
        }

        .list {
            min-width: 109px;
            height: 38px;
            margin-left: 12px;
            margin-right: 12px;
        }

        .round {
            border-radius: 50%;
            height: 40px;
            line-height: 40px;
            margin-left: 12px;
            margin-right: 12px;
        }
    }
}

@media (max-width: 1080px) {
    .main {
        flex-direction: column;
        justify-content: center;
        align-items: stretch;

        .logo {
            width: 150px;
            margin: 15px 25px;
        }
        .catalog {
            order:1;
            height: 50px;
            margin: 15px;
        }
        .list {
            height: 50px;
            margin: 15px;
        }
        .round {
            border-radius: 4px;
            height: 50px;
            line-height: 50px;
            margin: 15px;
        }
    }
}

 .main {
        @import 'search-style.scss';

        border-bottom: 1px solid #ECEFF1;
        display: flex;
        padding-top: 18px;
        padding-bottom: 18px;

        .catalog {
            background-color: #FED83D;
            border-radius: 4px;
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
                height: 20px;
                padding-right: 10.5px;
            }

        }

        .catalog:hover {
            background-color: #FED10D;
        }

        .list {
            border: 1px solid #ECEFF1;
            border-radius: 4px;
            background-color: #FAFBFC;
            color: #050F19;
            display: flex;
            align-items: center;
            justify-content: center;

            img {
                width: 80px;
                height: 26px;
            }
        }

        .list:hover {
            background-color: #FAFBB9;
        }

        .round {
            background-color: #9B51E0;
            min-width: 40px;
            color: #FFFFFF;
            text-align: center;
        }

        .round:hover {
            background-color: #9B71E0;
        }
    }
</style>
