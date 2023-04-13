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
                <li><a href="#">Pages</a>


                    <div class="dropdown">
                        <i class="fa-solid fa-chevron-down"></i>
                        <div class="dropdown-content">
                            <a href="#">Services</a>
                            <a href="#">Our work flow</a>
                            <a href="#">Video thumbnail type</a>
                        </div>
                    </div>

                </li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contacts</a></li>
                <li><a href="#">Gallery</a></li>
                <li><a href="#">Shop</a>

                    <div class="dropdown">
                        <i class="fa-solid fa-chevron-down"></i>
                        <div class="dropdown-content">
                            <a href="#">Shop 1</a>
                            <a href="#">Shop 2</a>
                            <a href="#">Shop 3</a>
                            <a href="#">Shop 4</a>
                            <a href="#">Shop 5</a>
                        </div>
                    </div>
                </li>
            </ul>
        </div>


        <div id="nav-right">
            <div id="nav-right-search">
                <a href="#"><img src="../../public/image (23).svg" alt="Search icon"></a>
            </div>

            <div id="nav-right-icons">
                <a href="#"><img src="../../public/image (9).svg" alt="Search icon"></a>
                <a href="#"><img src="../../public/image (10).svg" alt="Search icon"></a>
                <a href="#"><img src="../../public/image (11).svg" alt="Search icon"></a>
                <a href="#"><img src="../../public/image (12).svg" alt="Search icon"></a>
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
    padding: 2em;


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
                font-weight: bold;
            }
        }

        .dropdown {
            position: relative;
            display: inline-block;
            padding-left: .3em;
            cursor: pointer;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: black;
            min-width: 180px;
            z-index: 1;
            left: -50px;
        }

        .dropdown-content a {
            color: white;
            padding: 10px 15px;
            text-decoration: none;
            display: block;
        }

        .dropdown-content a:hover {
            background-color: lightgray
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }
    }

    #nav-right {
        display: flex;
        gap: 1em;

        #nav-right-search {
            display: flex;
            align-items: center;
            padding-right: 1em;
            border-right: 1px solid lightgrey;

            img {
                height: 18px;
            }
        }

        #nav-right-icons {
            display: flex;
            align-items: center;
            gap: .5em;

            img {
                height: 18px;
            }

            a {
                color: black;
            }
        }
    }
}
</style>