<script>

import { store } from "../store.js";

import CinemaStudioApp from "./CinemaStudioApp.vue";
import PeliculaStudioApp from "./PeliculaStudioApp.vue";
import AboutUsApp from "./AboutUsApp.vue";
import YourWatchlistApp from "./YourWatchlistApp.vue";
import CompanyNumbersApp from "./CompanyNumbersApp.vue";
import MeetTheTeam from "./MeetTheTeam.vue";
import Review from "./Review.vue";
import LatestNews from "./LatestNews.vue";
import BrandIdentity from "./BrandIdentity.vue";
import FormApp from "./FormApp.vue";

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
        LatestNews,
        BrandIdentity,
        FormApp,
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

        <LatestNews></LatestNews>

        <BrandIdentity></BrandIdentity>

        <FormApp></FormApp>

    </div>
</template>

<style scoped lang="scss"></style>