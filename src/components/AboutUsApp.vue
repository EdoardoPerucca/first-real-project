<script>

import { store } from "../store.js";

export default {

    name: "AboutUsApp",

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

        <div id="container-1000px">
            <div id="cinema-studio-inner">
                <div id="about-us">
                    About us
                </div>
                <div id="cinema-studio-title">
                    <h2>High quality cinematics</h2>
                </div>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti quisquam deleniti quam reprehenderit ea
                    tenetur dolores necessitatibus ipsum quia tempora, aperiam nostrum accusamus qui, ut quibusdam in
                    tempore odit mollitia</p>
                <button class="button-white">Read More</button>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
#cinema-studio {
    width: 100%;
    height: 425px;
    background: url(../../public/About-Us.jpg);
    background-size: cover;

    #container-1000px {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        max-width: 1000px;
        height: 100%;
        margin: auto;
        color: white;
        text-transform: uppercase;
        font-weight: bold;

        #cinema-studio-inner {
            max-width: 50%;

            #about-us {
                font-size: 10px;
            }

            h2 {
                font-size: 1.8em;
                padding-top: .5em;
            }

            p {
                font-size: .7em;
                padding-top: 2em;
                padding-bottom: 2em;
                color: #f2f2f2;
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