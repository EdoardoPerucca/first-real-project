<script>

import { store } from "../store.js";

export default {

    name: "BrandIdentity",

    data() {
        return {
            store,

            cards: [
                {
                    image: '03.png',
                },
                {
                    image: '04.png',
                },
                {
                    image: '05.png',
                },
                {
                    image: '01.png',
                },
                {
                    image: '02.png',
                },
            ]
        }
    },

    components: {
    },

}
</script>

<template>
    <div id="background">

        <div id="container-1000px">

            <div id="single-Cards" v-for="card in cards">
                <img v-bind:src="card.image" alt="Icons">
            </div>

        </div>
    </div>
</template>

<style scoped lang="scss">
#background {
    width: 100%;
    height: 170px;
    background: url(../../public/Parallax-01.jpg);
    background-size: cover;
    background-position-y: center;
    color: white;

    #container-1000px {
        display: flex;
        align-items: center;
        justify-content: center;
        max-width: 1000px;
        height: 100%;
        width: 100%;
        margin: auto;

        #single-Cards {
            display: flex;
            justify-content: center;
            width: 100%;

            img {
                width: 120px;
            }

        }

    }
}
</style>