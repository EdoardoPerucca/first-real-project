<script>

import { store } from "../store.js";

export default {

    name: "YourWatchlistApp",

    data() {
        return {
            store,

            cards: [
                {
                    image: 'Gallery-01.jpg',
                    title: 'Seventeenth summer',
                    text: 'Commercial, Music Video',
                },
                {
                    image: 'Gallery-02.jpg',
                    title: 'A message to space',
                    text: 'Short film',
                },
                {
                    image: 'Gallery-03.jpg',
                    title: 'The most beautiful thing',
                    text: "Music Video",
                },
                {
                    image: 'Gallery-04.jpg',
                    title: 'Permission to speak',
                    text: 'Documentary',
                },
                {
                    image: 'Gallery-05.jpg',
                    title: "Explore our space",
                    text: 'Film noir',
                },
                {
                    image: 'Gallery-06.jpg',
                    title: "Film production",
                    text: 'Blaxploitation',
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
            <h4>Your Watchlist</h4>
            <h2>Best hits movies</h2>
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
            font-size: 10px;
        }
    }

    #Pelicula-Studio-Cards {
        display: flex;
        flex-flow: row wrap;
        justify-content: space-between;
        width: 100%;
        gap: 20px;

        .Pelicula-single-Card {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1em;
            width: calc(100% / 3 - (20px * 2));

            img {
                max-width: 250px;
            }

            img:hover {
                opacity: .5;
                cursor: pointer;

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
                    font-weight: bold;
                    font-size: 12px;
                }
            }

        }

    }

}
</style>