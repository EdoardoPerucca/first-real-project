<script>

import { store } from "../store.js";

import CinemaStudioApp from "./CinemaStudioApp.vue";
import PeliculaStudioApp from "./PeliculaStudioApp.vue";
import AboutUsApp from "./AboutUsApp.vue";
import YourWatchlistApp from "./YourWatchlistApp.vue";
import CompanyNumbersApp from "./CompanyNumbersApp.vue";
import MeetTheTeam from "./MeetTheTeam.vue";
import Review from "./Review.vue";

export default {

    name: "MainApp",

    data() {
        return {
            store,
        }
    },

    components: {
        CinemaStudioApp,
        PeliculaStudioApp,
        AboutUsApp,
        YourWatchlistApp,
        CompanyNumbersApp,
        MeetTheTeam,
        Review,
    },

}
</script>

<template>
    <div id="cinema-studio">
        <CinemaStudioApp></CinemaStudioApp>

        <PeliculaStudioApp></PeliculaStudioApp>

        <AboutUsApp></AboutUsApp>

        <YourWatchlistApp></YourWatchlistApp>

        <CompanyNumbersApp></CompanyNumbersApp>

        <MeetTheTeam></MeetTheTeam>

        <Review></Review>

    </div>
</template>

<style scoped lang="scss">
/*
#cinema-studio {
    width: 100%;
    height: 425px;
    background-image: url(../../public/blog02.jpg);

    .cinema-studio-inner-text {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        color: white;
    }
}
*/
</style>