<script>

import { store } from "../store.js";

export default {

    name: "HeaderApp",

    data() {
        return {
            store,
        }
    },

    components: {
    },

}
</script>

<template>
    <div id="nav-main">

        <div id="nav-left">
            <img src="../../logo.svg" alt="logo">

        </div>


        <div id="nav-center">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Pages</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contacts</a></li>
                <li><a href="#">Gallery</a></li>
                <li><a href="#">Shop</a></li>
            </ul>
        </div>


        <div id="nav-right">
            <div id="nav-right-search">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>

            <div id="nav-right-icons">
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-youtube"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
#nav-main {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 50px;
    padding: 1em;


    #nav-left {
        img {
            width: 150px;
        }
    }

    #nav-center {

        ul {
            display: flex;
            gap: 2em;
            text-transform: uppercase;
            font-size: .8em;

            a {
                color: black;
                font-size: 12px;
            }
        }
    }

    #nav-right {
        display: flex;
        gap: 1em;

        #nav-right-icons {
            display: flex;
            gap: .5em;

            a {
                color: black;
            }
        }
    }
}
</style>