<script>

import { store } from "../store.js";

export default {

    name: "FormApp",

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
    <div id="container-1000px">

        <div id="square-left">
            <h5>Collaborate</h5>
            <h2>
                Want to work with us?
                <br>
                Leave us a message!
            </h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias quam, nostrum eligendi at facere accusamus
                deleniti quis doloremque modi vel, soluta, doloribus assumenda mollitia quos praesentium rerum fuga dolor?
                Aliquid.</p>
        </div>

        <div id="square-right">
            <form action="" method="get">
                <div class="form-inner">
                    <input type="text" name="name" id="name" placeholder="Your Name" required>
                    <input type="email" name="email" id="email" placeholder="Your email" required>
                    <input type="number" name="number" id="phone-number" placeholder="Mobile number" required>
                    <input type="number" name="number" id="pin-number" placeholder="You Pincode" required>

                    <div id="form-message">
                        <input type="text" name="message" id="message" placeholder="Enter your message">
                    </div>
                </div>

                <div id="button">
                    <input id="button-inner" type="submit" value="Submit now">
                </div>
            </form>
        </div>

    </div>
</template>

<style scoped lang="scss">
#container-1000px {
    display: flex;
    justify-content: space-between;
    max-width: 1000px;
    height: 100%;
    width: 100%;
    margin: auto;
    padding-bottom: 4em;
    padding-top: 50px;
    gap: 40px;

    #square-left {
        width: 50%;

        h2 {
            text-transform: uppercase;
            margin-top: 1em;
            margin-bottom: 1em;
            font-weight: bold;
        }
    }

    #square-right {
        width: 50%;

        form {

            .form-inner {
                display: flex;
                flex-flow: row wrap;
                gap: 25px;
                justify-content: space-between;
                margin-bottom: 1.5em;


                input {
                    background-color: #f2f2f2;
                    border: none;
                    padding: .7em;
                    width: calc(100% / 2 - (20px * 1));

                }

                #form-message {
                    width: 100%;

                    #message {
                        width: 100%;
                        height: 100px;
                    }
                }
            }


            #button {
                width: 100%;

                #button-inner {
                    color: white;
                    background-color: black;
                    border: none;
                    width: 100%;
                    padding: .5em;
                    text-transform: uppercase;
                }
            }

        }
    }


}
</style>