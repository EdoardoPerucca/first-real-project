<script>

import { store } from "../store.js";

export default {

    name: "PeliculaStudioApp",

    data() {
        return {
            store,

            cards: [
                {
                    image: 'image (14).svg',
                    title: 'Array of equipment',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                },
                {
                    image: 'image (16).svg',
                    title: 'New technologies',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                },
                {
                    image: 'image (18).svg',
                    title: 'Versitile actors',
                    text: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
                },
                {
                    image: 'image (15).svg',
                    title: 'Top directors',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                },
                {
                    image: 'image (17).svg',
                    title: "Minute editing",
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                },
                {
                    image: 'image (19).svg',
                    title: "Versitile actors",
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                }
            ],
        }
    },

    components: {
    },

}
</script>

<template>
    <div id="container-1000px">

        <div id="Pelicula-Studio-Title">
            <h4>Pelicula Studio</h4>
            <h2>This is what we do</h2>
        </div>

        <div id="Pelicula-Studio-Cards">
            <div class="Pelicula-single-Card" v-for="card in cards">
                <img v-bind:src="card.image" alt="">
                <div class="Pelicula-single-card-text">
                    <h5>{{ card.title }}</h5>
                    <p>{{ card.text }}</p>
                </div>
            </div>
        </div>


    </div>
</template>

<style scoped lang="scss">
#container-1000px {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 1000px;
    height: 100%;
    width: 100%;
    margin: auto;
    padding-bottom: 4em;

    #Pelicula-Studio-Title {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 3em;
        padding-bottom: 2em;
        text-transform: uppercase;

        h4 {
            font-size: .7em;
        }

        h2 {
            font-size: 2em;
        }
    }

    #Pelicula-Studio-Cards {
        display: flex;
        flex-flow: row wrap;
        justify-content: space-between;
        width: 100%;
        gap: 50px;

        .Pelicula-single-Card {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1em;
            width: calc(100% / 3 - (50px * 2));


            img {
                max-height: 50px;
            }

            .Pelicula-single-card-text {
                display: flex;
                flex-direction: column;
                text-align: center;
                gap: .5em;

                h5 {
                    text-transform: uppercase;
                    font-weight: bold;
                }

                p {
                    color: #8f8f92;
                    font-size: 13px;
                }
            }

        }

    }

}
</style>