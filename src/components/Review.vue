<script>

import { store } from "../store.js";

export default {

    name: "Review",

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
    <div id="review-background">

        <div id="container-1000px">
            <div id="review-inner">
                <div class="text">
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloribus harum ea cumque voluptatem beatae
                        quae necessitatibus enim veritatis odit quam. Eos doloremque debitis qui, illo eligendi incidunt
                        corrupti placeat blanditiis.</p>
                </div>
                <div class="review-subject">
                    <i class="fa-solid fa-quote-left"></i>
                    <img src="../../public/01.jpg" alt="John Doe">
                    <div class="review-subject-text">
                        <div class="review-subject-name">John Doe</div>
                        <div class="review-subject-position">Designer</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
#review-background {
    width: 100%;
    height: 425px;
    background: url(../../public/Parallax-02.jpg);
    background-size: cover;

    #container-1000px {
        display: flex;
        justify-content: center;
        max-width: 1000px;
        height: 100%;
        margin: auto;
        color: white;

        #review-inner {
            display: flex;
            flex-direction: column;
            justify-content: center;
            text-align: center;
            max-width: 500px;
            gap: 20px;
            height: 100%;
            position: relative;

            .fa-quote-left {
                position: absolute;
                top: 15%;
                left: 50%;
                font-size: 3em;
                translate: -50%;
            }

            .review-subject {
                display: flex;
                justify-content: center;
                gap: 1em;

                img {
                    border-radius: 50%;
                }

                .review-subject-text {

                    .review-subject-name {
                        text-transform: uppercase;
                    }

                    .review-subject-position {
                        display: flex;
                        font-size: 12px;
                        align-items: flex-start;
                    }
                }
            }
        }
    }
}
</style>