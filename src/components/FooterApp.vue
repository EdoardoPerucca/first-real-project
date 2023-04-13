<script>

import { store } from "../store.js";

export default {

    name: "FooterApp",

    data() {
        return {
            store,

            cards: [

                {
                    title: 'Information',
                    links: [
                        'Product Support',
                        'Checkout',
                        'Report Abuse',
                        'Redeem Voucher',
                        'Order Status',
                    ]
                },
                {
                    title: 'Useful Links',
                    links: [
                        'Policies & Rules',
                        'Privacy Policy',
                        'License Policy',
                        'My Account',
                        'Locality',
                    ]
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

                <div class="footer-single-cards">

                    <h4>Contact Info</h4>
                    <div class="contact-info">
                        <i class="fa-solid fa-location-dot"></i>
                        <p>2/45 Tower Street, NewYork USA</p>
                    </div>
                    <div class="contact-info">
                        <i class="fa-sharp fa-regular fa-phone"></i>
                        <p>Call Us On 08008401010</p>
                    </div>
                    <div class="contact-info">
                        <i class="fa-regular fa-envelope"></i>
                        <p>Demo@Example.com</p>
                    </div>

                </div>

                <div v-for="card in cards" class="footer-single-cards">
                    <strong>
                        <h4>{{ card.title }}</h4>
                    </strong>
                    <ul>
                        <li v-for="link in card.links">{{ link }}</li>
                    </ul>

                </div>

                <div class="footer-single-cards">

                    <div id="newsletter">
                        <h4>Newsletter</h4>
                        <p>Subscribe to receive inspiration, <br> Ideas & News in your inbox</p>
                        <input type="text" placeholder="Enter Your Email">
                        <button>Subscribe</button>
                    </div>

                </div>

            </div>

            <hr>

            <div id="copyright">
                <i class="fa-regular fa-copyright"></i>
                2023 All rights reserved. Developed By TemplateMela
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
                flex-direction: column;
                width: 200px;

                h4 {
                    text-transform: uppercase;
                    padding-bottom: 1em;
                }

                .contact-info {
                    display: flex;
                    align-items: center;
                    gap: 10px;
                    font-size: 13px;
                    text-transform: capitalize;
                    color: #c2c3c7;
                }

                li {
                    line-height: 2em;
                    font-size: 13px;
                    color: #c2c3c7;
                }

                #newsletter {
                    font-size: 13px;
                    line-height: 1.5em;

                    p {
                        color: #c2c3c7;
                    }

                    input {
                        margin-top: 1em;
                        margin-bottom: 1em;
                        padding: .8em;
                        background-color: #1c1c1c;
                        border: none;
                    }

                    button {
                        padding: 1em 2.5em;
                        text-transform: uppercase;
                        font-weight: bold;
                        border: none;
                    }
                }

            }
        }

        hr {
            margin-top: 5em;
            margin-bottom: 1.5em;
            color: #c2c3c7;
        }

        #copyright {
            text-align: center;
            padding-bottom: 1em;
            font-size: 13px;
            text-transform: capitalize;
            color: #c2c3c7;
            font-weight: bold;
        }
    }

}
</style>