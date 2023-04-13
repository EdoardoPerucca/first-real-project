<script>

import { store } from "../store.js";

export default {

    name: "MeetTheTeam",

    data() {
        return {
            store,

            cards: [
                {
                    image: 'Team-01.jpg',
                    title: 'Fabricio Guerra',
                    text: 'Main Director',
                },
                {
                    image: 'Team-02.jpg',
                    title: 'Umberto Pagoda',
                    text: 'Main Writer',
                },
                {
                    image: 'Team-03.jpg',
                    title: 'Gloria Riccasso',
                    text: "Main Producer",
                },
                {
                    image: 'Team-04.jpg',
                    title: 'Lio Napoin',
                    text: 'Cameramen',
                },
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
            <h4>The Pericuros</h4>
            <h2>Meet the team</h2>
        </div>

        <div id="Pelicula-Studio-Cards">
            <div class="Pelicula-single-Card" v-for="card in cards">
                <img v-bind:src="card.image" alt="Photo">
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
        padding-top: 4em;
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
        gap: 10px;

        .Pelicula-single-Card {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1em;
            width: calc(100% / 4 - (10px * 3));


            img {
                max-height: 250px;
            }

            img:hover {
                opacity: .5;
                cursor: pointer;
            }

            .Pelicula-single-card-text {
                display: flex;
                flex-direction: column;
                text-align: center;

                h5 {
                    text-transform: uppercase;
                    font-weight: bold;
                }

                p {
                    font-size: 12px;
                }
            }

        }

    }

}
</style>