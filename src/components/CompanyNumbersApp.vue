<script>

import { store } from "../store.js";

export default {

    name: "CompanyNumbersApp",

    data() {
        return {
            store,

            cards: [
                {
                    number: 158,
                    text: 'Satisfied clients',
                },
                {
                    number: 3,
                    text: 'Our projects',
                },
                {
                    number: 1.906,
                    text: 'Cup of coffee',
                },
                {
                    number: 2,
                    text: 'Our awards',
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

            <div id="Numbers-Cards">
                <div class="Numbers-single-Card" v-for="card in cards">
                    <div class="Single-Card-Number">{{ card.number }}</div>
                    <div class="Single-Card-Text">{{ card.text }}</div>
                </div>
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

        #Numbers-Cards {
            display: flex;
            width: 100%;

            .Numbers-single-Card {
                display: flex;
                flex-direction: column;
                align-items: center;
                width: calc(100% / 4);

                .Single-Card-Number {
                    font-weight: bold;
                    font-size: 2em;
                }

                .Single-Card-Text {
                    text-transform: uppercase;
                    font-size: 10px;
                    font-weight: bold;
                }
            }
        }

    }
}
</style>