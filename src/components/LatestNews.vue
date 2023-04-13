<script>

import { store } from "../store.js";

export default {

    name: "LatestNews",

    data() {
        return {
            store,

            cards: [
                {
                    image: 'blog07.jpg',
                    date: 'November 06, 2021 By Admin',
                    title: 'Recap your latest company event',
                    text: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog01.jpg',
                    date: 'May 27, 2022 By Admin',
                    title: 'How to edit a film score to serve',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis omnis porro harum itaque velit sit deserunt nobis laudantium minima. Nostrum molestiae ipsa architecto odit. Quidem voluptate ducimus dignissimos aliquid minus.',
                },
                {
                    image: 'blog02.jpg',
                    date: 'May 07, 2022 By Admin',
                    title: 'Are you ready to make it awesome',
                    text: "Design is our playground, while we create an awesome experience, we loke having fun. No animals",
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
            <h4>Latest News</h4>
            <h2>Articles updated daily</h2>
        </div>

        <div id="Pelicula-Studio-Cards">
            <div class="Pelicula-single-Card" v-for="card in cards">
                <img v-bind:src="card.image" alt="">
                <div class="Pelicula-single-card-text">
                    <div>{{ card.date }}</div>
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
    padding-top: 2em;

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
        gap: 10px;

        .Pelicula-single-Card {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1em;
            width: calc(100% / 3 - (10px * 2));
            overflow: hidden;


            img {
                max-width: 300px;

            }

            img:hover {
                opacity: .5;
                cursor: pointer;
            }

            .Pelicula-single-card-text {
                display: flex;
                flex-direction: column;
                text-align: start;

                h5 {
                    text-transform: uppercase;
                    font-weight: bold;
                    padding-top: 1em;
                    padding-bottom: 1em;
                }

                p {
                    font-size: 12px;
                    color: #8f8f92;
                }
            }

        }

    }

}
</style>