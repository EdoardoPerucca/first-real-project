<script>

import { store } from "../store.js";

export default {

    name: "CinemaStudioApp",

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
    <div id="cinema-studio">

        <img class="arrow-left" src="../../public/left-arrow.svg" alt="Arrow left">

        <div id="container-1000px">
            <div id="cinema-studio-inner">
                <div>
                    cinema studio
                </div>
                <div id="cinema-studio-title">
                    action and inspire people
                </div>
                <button class="button-white">Read More</button>
            </div>

        </div>

        <img class="arrow-right" src="../../public/right-arrow.svg" alt="Arrow right">

    </div>
</template>

<style scoped lang="scss">
#cinema-studio {
    width: 100%;
    height: 425px;
    background: rgba(0, 0, 0, 0.7, ) url(../../public/blog02.jpg);
    background-blend-mode: darken;
    position: relative;

    .arrow-left {
        max-height: 35px;
        max-width: 35px;
        background-color: #636161;
        position: absolute;
        left: 20px;
        padding: 10px;
        top: 50%;
        transform: translatey(-50%);
        cursor: pointer;

    }

    .arrow-right {
        max-height: 35px;
        max-width: 35px;
        background-color: #636161;
        position: absolute;
        right: 20px;
        padding: 10px;
        top: 50%;
        transform: translatey(-50%);
        cursor: pointer;

    }


    #container-1000px {
        display: flex;
        flex-direction: column;
        justify-content: center;
        max-width: 1000px;
        height: 100%;
        margin: auto;
        color: white;
        text-transform: uppercase;
        font-weight: bold;



        #cinema-studio-inner {
            max-width: 400px;

            #cinema-studio-title {
                font-size: 2.5em;
            }

            .button-white {
                padding: .5em 1.4em;
                text-transform: uppercase;
                margin-top: 1em;
                border: none;
                cursor: pointer;
            }
        }

    }
}
</style>