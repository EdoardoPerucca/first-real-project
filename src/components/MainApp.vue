<script>

import { store } from "../store.js";

import CinemaStudioApp from "./CinemaStudioApp.vue";
import PeliculaStudioApp from "./PeliculaStudioApp.vue";

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
    },

}
</script>

<template>
    <div id="cinema-studio">
        <CinemaStudioApp></CinemaStudioApp>

        <PeliculaStudioApp></PeliculaStudioApp>

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