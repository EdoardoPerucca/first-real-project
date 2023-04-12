<script>

import { store } from "../store.js";

export default {

    name: "FooterApp",

    data() {
        return {
            store,

            cards: [
                {
                    title: 'Contact info',
                    text: ["Product Support", "Checkout"],
                },
                {
                    title: 'Information',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis omnis porro harum itaque velit sit deserunt nobis laudantium minima. Nostrum molestiae ipsa architecto odit. Quidem voluptate ducimus dignissimos aliquid minus.',
                },
                {
                    title: 'Useful Links',
                    text: "Design is our playground, while we create an awesome experience, we loke having fun. No animals",
                },
                {
                    title: 'Newsletter',
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
    <div id="footer-background">

        <div id="container-1000px">

            <div id="footer-list">

                <div v-for="card in cards" class="footer-single-cards">
                    <ul>
                        <li>{{ card.title }}</li>
                        <li>{{ card.text[""] }}</li>
                    </ul>
                </div>

            </div>

        </div>

    </div>
</template>

<style scoped lang="scss">
#footer-background {
    background-color: black;
    color: white;

    #container-1000px {
        max-width: 1000px;
        height: 100%;
        width: 100%;
        margin: auto;
        padding-top: 50px;

        #footer-list {
            display: flex;
            justify-content: space-between;

            .footer-single-cards {
                display: flex;
                width: 200px;
                height: 200px;
                border: 1px solid red;
            }
        }
    }

}
</style>